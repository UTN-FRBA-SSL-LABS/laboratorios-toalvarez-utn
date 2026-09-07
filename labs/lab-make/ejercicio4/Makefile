# Nombre del ejecutable final
PROGRAMA := programa

# Compilador y flags
CC     := gcc
CFLAGS := -Wall

# TODO 1: Definí la variable SRCS listando todos los archivos .c del proyecto
SRCS := main.c operaciones.c

# TODO 2: Definí la variable OBJS a partir de SRCS
OBJS := $(SRCS:.c=.o)

# Regla principal
all: $(PROGRAMA)

# Regla para linkear los objetos y generar el ejecutable
# TODO 3: Completá el comando de linkeo
$(PROGRAMA): $(OBJS)
	$(CC) $^ -o $(PROGRAMA)

# TODO 4: Escribí la regla de patrón para compilar cada .c en su .o
%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

# Regla para limpiar archivos generados
clean:
	rm -f $(PROGRAMA) $(OBJS)

# TODO 5: Declarar los targets que NO son archivos usando .PHONY
.PHONY: all clean
