##
## EPITECH PROJECT, 2021
## TekStruct
## File description:
## Makefile
##

SRC =

BUILD_DIR = build
OBJ = $(SRC:%.c=$(BUILD_DIR)/%.o)
CFLAGS = -I include/

OUTPUT = lib_my_csfml.a

all: $(OUTPUT)

$(BUILD_DIR)/%.o: %.c
	@mkdir -p $(@D)
	@echo "  CC       $<"
	@$(CC) $(CFLAGS) -c $< -o $@

$(OUTPUT): $(OBJ)
	ar rc $(OUTPUT) $(OBJ)
	cp $(OUTPUT) ../exec
	cp include/my_csfml.h ../hlib

clean:
	rm -f $(OBJ)

fclean: clean
	rm -f $(OUTPUT)
	rm -f ../exec/$(OUTPUT)
	rm -f ../hlib/my_csfml.h

re: fclean all

.PHONY: all clean fclean re