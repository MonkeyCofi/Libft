NAME = ../libft.a

SRCS_DIR = srcs

OBJS_DIR = objs

SRCS = 	$(addprefix $(SRCS_DIR)/, ft_printf.c ft_print_char.c ft_print_str.c ft_print_addr.c \
		ft_parse_string.c ft_is_specifier.c ft_putstr.c \
		ft_print_nbr.c ft_itoa_ubase.c ft_putchar_n.c ft_print_hexa.c)

OBJS = $(SRCS:$(SRCS_DIR)/%.c=$(OBJS_DIR)/%.o)

CFLAGS = -Wall -Wextra -Werror -I./

CC := gcc

all: $(NAME)

$(NAME): $(OBJS)
	ar -rc $(NAME) $(OBJS)

$(OBJS_DIR)/%.o: $(SRCS_DIR)/%.c
	$(CC) $(CFLAGS) -c $< -o $@

bonus: all

clean:
	rm -f $(OBJS)

fclean: clean
	rm -f libftprintf.a

re: fclean all
