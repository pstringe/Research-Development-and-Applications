---
creation date:		2023-07-12 11:13
modification date:	2023-07-12 11:13
title: 				Notes related to the foundation library C
tags:
---
[2023-07-12](2023-07-12.md)
* when running f_strsplit we get a segmentation fault
* currently we zero out `cur` before appending it to the result array. We want append a copy before zero-ing it out
```C
char **g(const char *str, char delim, char *cur, char **res, int i, int len) {
    if (i == len) {
        return (res);
    } else if (cur[i] != delim) {
        return g(str, delim, f_strncat(cur, (str + i), f_strlen((char*)(str + i))), res, i + 1, len);
    }
    return g(str, delim, f_bzero(cur, f_strlen(cur)), f_array_append(res, cur), i + 1, len);
}
```

* we still experience a segmentation fault after making the change
* bad acess occurs when we attempt to read the first value of our result array in f_array_len of f_array_append
* We seem to hit a null address immediately
* We didn't allocate memory because it's not obvious how many pointer we need before iterating the string.
* The simple solution is to itterate the input string and count the occurences of the delimiter then allocate that number of pointers + 1; 
* To resize our allocation each time is more redundant than doing one pass with the string
* We've written a method to count the delimeters and used that number to allocate memory.
* The segfault is gone but we still don't see the sucess message
* It looks like we forgot to increment the iterator
* We incremented the iterator, now we have a new segmenation fault. 
* our segfault occurs on line 44 in f_strlen called from strcmp
* we seem to be passing a NULL
* the index of the result array is 1
* we seem to have copied the whole string into the first index
* When we take take the length to determine the number of bytes to copy, we get it from the current index to the end.
* We need to get it up to the deli-meter
```
return g(str, delim, f_strncat(cur, (str + i), (f_strchr(str, delim) - (str + i))), res, i + 1, len);
```
* the segfault is gone but our tests do not resolve. 
* We forgot to increment the iterator
* We've incremented the iterator, now we have another segfault
* We have a null passed to f_strlen
* f_strlen is called from f_strcmp
* f_strcmp is called from the test passing res[i]
* i is 0
* res is not null
* on the res allocation we should add another pointer and set it to null
* f_strncat returns expected value
* instead of incrementing our index by one, we can increment it by the number of bytes that were copied
* we have a bad access in f_strlen
* we pass the string, "This"
* according to the error, the function itself is unavailable
* we'll recomile and see if that helps
* 
---
[1^]:: [Develop Foundation library C](Develop%20Foundation%20library%20C.md)
[2^]:: [Tasks related to foundation library](Tasks%20related%20to%20foundation%20library.md)
