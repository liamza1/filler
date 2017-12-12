# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lstreak <marvin@42.fr>                     +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2017/11/30 09:03:10 by lstreak           #+#    #+#              #
#    Updated: 2017/12/07 17:57:28 by lstreak          ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = resources/players/lstreak.filler

SRCS += src/main.c 
SRCS +=	src/utils.c 
SRCS +=	src/utils_2.c 
SRCS +=	src/parse_n_lex.c 
SRCS +=	src/algo.c 
SRCS +=	src/algo_2.c 

FLAGS = -Wall -Werror -Wextra -I./inc/filler.h

OBJ = $(SRCS:.c=.o)

all: $(NAME)

$(NAME): $(OBJ)
	make -C libft
	gcc -o $(NAME) $(FLAGS) $(OBJ) libft/libft.a
	echo "Filler done"

clean:
	make clean -C libft
	rm -f $(OBJ)

fclean: clean
	make fclean -C libft
	rm -f $(NAME)

re: fclean all
