# Name
NAME 			= minishell

# Compiler and flags
CC 				= cc
CFLAGS 			= -Wall -Wextra -Werror
#LDFLAGS 		= -fsanitize=address  -fsanitize=address -g
INCLUDES 		= -I./includes -I./libft/includes
RM 				= rm -f

# LIBFT
LIBFT	 		= ./libft/libft.a

# Source files by directory
MAN_DIR 		=


# Source path

MAN_SRCS		=	main.c $(MAN_DIR)

# Object files by directory

#MAN_OBJS = $(MAN_SRCS:.c=.o)
#BON_OBJS = $(BON_SRCS:.c=.o)

# Marker files to track which version is built
#mandatory : .mandatory
#bonus : .bonus

all: mandatory

$(LIBFT):
	$(MAKE) -C ./libft

mandatory : .mandatory
.mandatory: $(LIBFT) $(MAN_SRCS)
	$(CC) $(CFLAGS) $(INCLUDES) $(MAN_SRCS) $(LIBFT) -o $(NAME)
	@touch .mandatory

clean:
	$(MAKE) -C ./libft clean
	$(RM) .mandatory

fclean: clean
	$(MAKE) -C ./libft fclean
	$(RM) $(NAME) .mandatory

re: fclean all

.PHONY: all clean fclean re
