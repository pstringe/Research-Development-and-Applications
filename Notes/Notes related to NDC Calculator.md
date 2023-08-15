---
creation date:		2023-08-06 01:02
modification date:	2023-08-06 01:02
title: 				Notes related to NDC Calculator
tags:
---
* We use an I flag for each include in the makefile.
* We specify the library directory with -L
* -lx links library libx.a 
* We will design this such that the code and information can be reused in Prop Analysis. It is essential to implement prop-analysis to establish our hyper-technical vocabulary. To avoid undue reticulation and assert greater control over our representation
* The first version will use integers to refresh our technical prowess.
* The second version will use a number theory so we can be as reductive as possible on our NDC architecture, easing the load on the reticulated spaces. 
* I hate the fact that I have to do this again but I'm going to do it. And I'll be even faster and more powerful than I was the last time I did this. 
* I don't care about the monetary, I will restore my engineering prowess and become the most influential intellect in menial space. 
* Regarding my work I will produce commentary on my methods that way I don't loose everything if I'm retarded.

---
Notes on makefile
```
CC = gcc
NAME = calc
LIBF = foundation.a
FUNCS = main \

SRCS := $(patsubst %, %.c, $(FUNCS))

OBJS := $(patsubst %.c, %.o, $(SRCS))

CFLAGS = -Wall -Werror -Wextra

all : $(NAME)

$(NAME): $(OBJS)
	gcc -c $(patsubst %, %.c, $(NAME))
	gcc -o $(NAME) $(OBJS) tests.c -L. $(NAME)

$(OBJS): $(SRCS)
	$(CC) $(CFLAGS) -c $(SRCS)

clean :
	rm -f *.o
fclean : clean
	rm -f $(NAME)
re : fclean all
```

* We have 4 "static" variables
	1. CC : the compiler command
	2. NAME : calc 
	3. LIBF: library file
	4. FUNCS: represents the 
	6. SRCS := $(patsubst %, %.c, $(FUNCS)) : modifies each value in FUNCS to include the .c file extention
	7. OBJS := $(patsubst %.c, %.o, $(SRCS)) : modifies each value in FUNCS to include the .o file extension
	8. CFLAGS = -Wall -Werror -Wextra

* We have 6 rules
```Makefile
all : $(NAME)
```
Responsible for generating the main file the name of which is assigned to NAME

```
$(NAME): $(OBJS)
	gcc -c $(patsubst %, %.c, $(NAME))
	gcc -o $(NAME) $(OBJS) tests.c -L. $(NAME)
```
The fist line of this rule is responsible for compiling the object files.

The second line is responsible for linking the object files and the compiled library

```
$(OBJS): $(SRCS)
	$(CC) $(CFLAGS) -c $(SRCS)
```

*Questions/Concerns* (We want to think about what we are doing here. When we express a plurality over a generation of successions)
* This makefile is at the root and we want to compile a library that has its own Makefile in a deeper directory 

[[2023-08-08]]
Here is the makefile for kift:
```
CC = gcc
NAME = KIFT
CLIENT = client
SERVER = server
INCD = ./includes/

LIB = libft.a

LIBD = $(INCD)libft/
SINC = $(INCD)

SSRCD = ./srcs/server/
CSRCD = ./srcs/client/

SSRCS = server\
		server_methods\
		prompt\
		listening\
		users\
		history\
		entry\
		alarm/alarm\
		bright_or_dim_screen/command_lightsup\
		bright_or_dim_screen/command_lightsdown\
		command_music\
		command_weather\
		command_sms\
		command_email\
		command_search\
		command_history\
		command_quit\
		command_team\
		help

MSRCS = server\
		multiserver\
		history\
		entry\
		command_history\
		command_quit

CSRCS = client\
		mic

SOBJS = $(patsubst $(SSRCD)%, %.o, $(SSRCS))
COBJS = $(patsubst $(CSRCD)%, %.o, $(CSRCS))

CFLAGS = -Wall -Werror -Wextra
DFLAGS = -g
SFLAGS = -fsanitize=address -fno-omit-frame-pointer
PFLAGS = -DMODELDIR=\"`pkg-config --variable=modeldir pocketsphinx`\" \
		 `pkg-config --cflags --libs pocketsphinx sphinxbase`

all: $(NAME)

$(NAME): $(SERVER) $(CLIENT)

$(SERVER) : $(INCD)$(LIB)
	$(CC) $(CFLAGS) -o $(SERVER) $(patsubst %, $(SSRCD)%.c, $(SSRCS)) \
	-L$(LIBD) -lft -lcurl -I $(INCD) -I $(LIBD)

$(CLIENT) : $(INCD)$(LIB)
	$(CC) $(CFLAGS) -o $(CLIENT) $(patsubst %, $(CSRCD)%.c, $(CSRCS)) \
	-L$(LIBD) -lft -I $(LIBD) -I $(INCD) $(PFLAGS)

debug-multiserver-client : fclean $(INCD)$(LIB) 
	$(CC) $(CFLAGS) $(DFLAGS) -o $(SERVER) $(patsubst %, $(SSRCD)%.c, $(MSRCS)) -L$(LIBD) -lft -I $(INCD)  -I $(LIBD)
	$(CC) $(CFLAGS) $(DFLAGS) -o $(CLIENT) $(patsubst %, $(CSRCD)%.c, $(CSRCS)) -L$(LIBD) -lft -I $(LIBD) -I $(INCD) $(PFLAGS)

debug-multiserver: fclean $(INCD)$(LIB)
	$(CC) $(CFLAGS) $(DFLAGS) -o $(SERVER) $(patsubst %, $(SSRCD)%.c, $(MSRCS)) \
	-L$(LIBD) -lft -I $(INCD)  -I $(LIBD)

debug-server: fclean $(INCD)$(LIB)
	$(CC) $(CFLAGS) $(DFLAGS) -o $(SERVER) $(patsubst %, $(SSRCD)%.c, $(SSRCS)) \
	-L$(LIBD) -lft -lcurl -I $(INCD)  -I $(LIBD)

debug-client: fclean $(INCD)$(LIB)
	$(CC) $(CFLAGS) $(DFLAGS) -o $(CLIENT) $(patsubst %, $(CSRCD)%.c, $(CSRCS)) \
	-L$(LIBD) -lft -I $(LIBD) -I $(INCD) $(PFLAGS)

sanitize-server: fclean $(INCD)$(LIB)
	$(CC) $(CFLAGS) $(SFLAGS) -o $(SERVER) $(patsubst %, $(SSRCD)%.c, $(SSRCS)) \
	-L$(LIBD) -lft -lcurl -I $(LIBD)  -I $(INCD)

sanitize-client: fclean $(INCD)$(LIB)
	$(CC) $(CFLAGS) $(SFLAGS) -o $(CLIENT) $(patsubst %, $(CSRCD)%.c, $(CSRCS)) \
	-L$(LIBD) -lft -I $(LIBD) -I$(INCD) $(PFLAGS)

debug: debug-server debug-client
sanitize: sanitize-server sanitize-client

setup:
	brew tap watsonbox/cmu-sphinx
	brew install --HEAD watsonbox/cmu-sphinx/cmu-sphinxbase
	brew install --HEAD watsonbox/cmu-sphinx/cmu-sphinxtrain
	brew install --HEAD watsonbox/cmu-sphinx/cmu-pocketsphinx

$(INCD)$(LIB):
	make -C $(INCD)libft

clean:
	make -C $(INCD)libft clean
	rm -rf *.o
	#rm -Rrf *.dSYM

fclean: clean
	make -C $(INCD)libft fclean
	rm -rf $(SERVER) $(CLIENT)

re: fclean
	make
```

* The makefile for kift is more complex.
* We will identify the means by which it compiles libft for the main project
* the all rule is dependent on the name rule
* the name rule is dependent on the server rule and the client rule
* We examine the server rule:
```
$(SERVER) : $(INCD)$(LIB)
	$(CC) $(CFLAGS) -o $(SERVER) $(patsubst %, $(SSRCD)%.c, $(SSRCS)) \
	-L$(LIBD) -lft -lcurl -I $(INCD) -I $(LIBD)
```
* https://www.gnu.org/software/make/manual/make.html#Libraries_002fSearch
* According to these docs, the `-lft` flag is responsible for initiating the directory search for the `libft.a` file.
* We want to remember what the `-I` flag is for. 
* First examine the directories it references.
* The variables after the `I` flags reference the directories of the client srcs and server srcs
* `-L`  seems to reference the directory of the library
* It seems our makefile will at least need the `L` flag, a variable for the library directory, a name change of the library and a `-lfoundation` flag to reference it. 

[[2023-08-10]]
* 

---
[1^]:: [[NDC Calculator Sim]]
[2^]:: [[Tasks related to NDC Calculator]]
[3^]:: [[Notes related to NDC Calculator]]
