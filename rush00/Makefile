# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: vgladush <vgladush@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/10/07 12:29:41 by vgladush          #+#    #+#              #
#    Updated: 2018/10/07 12:46:10 by vgladush         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME	=	ft_retro
CMPL	=	clang++
FLGS	=	-std=c++98 -Wall -Wextra -Werror
DIRC	=	./
FUNC	=	main.cpp Enemy.cpp Bullet.cpp Asteroids.cpp Ship.cpp Game.cpp Stars.cpp Position.cpp
OBJC	=	$(FUNC:.cpp=.o)
OBJS	=	$(addprefix $(DIRC), $(OBJC))

all: $(NAME)

$(NAME): $(OBJS)
	@$(CMPL)  -lncurses -o $(NAME) $(OBJC)
	@echo "\x1B[0;32m$(NAME) ready\x1B[0m"

$(DIRC)%.o: $(DIRC)%.cpp
	@$(CMPL) $(FLGS) -o $@ -c $<

clean:
	@rm -f $(OBJS)
	@echo "\x1B[1;31mobjects $(NAME) deleted\x1B[0m"

fclean: clean
	@rm -f $(NAME)
	@echo "\x1B[1;31m$(NAME) deleted\x1B[0m"

re: fclean all
