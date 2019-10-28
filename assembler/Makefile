# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: blanna <marvin@42.fr>                      +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/09/30 13:46:41 by blanna            #+#    #+#              #
#    Updated: 2019/09/30 13:46:43 by blanna           ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = asm

SRC = srcs/asm.c \
srcs/into_bytecode.c \
srcs/create_file.c \
srcs/free.c \
srcs/init_data.c \
srcs/lexical_check.c \
srcs/champ_data.c \
srcs/process.c \
srcs/syntax_check.c \
srcs/support.c

OBJ = asm.o \
into_bytecode.o \
create_file.o \
free.o \
init_data.o \
lexical_check.o \
champ_data.o \
process.o \
syntax_check.o \
support.o

FLAGS = -Wall -Wextra -Werror
LIBRF = ../libft/libft.a

all: $(NAME)

$(NAME):
		@make re -C ../libft/ 
		@gcc -g -c $(SRC)
		@gcc $(LIBRF) $(FLAGS) $(OBJ) -o $(NAME)

clean:
		@make clean -C ../libft/
		@rm -f $(OBJ)

fclean: clean
		@make fclean -C ../libft/
		@rm -f $(NAME)

re: fclean all
