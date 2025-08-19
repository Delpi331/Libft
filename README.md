Libft (42) — Biblioteca Estándar de C Personalizada
Implementación completa de 45 funciones estándar de C y utilidades adicionales con gestión robusta de memoria y estructuras de datos.

https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white
https://img.shields.io/badge/42-School-blue?style=for-the-badge
https://img.shields.io/badge/License-MIT-green?style=for-the-badge
https://img.shields.io/badge/45-Functions-orange?style=for-the-badge

📚 Resumen
Lenguaje: C (C99)

Total funciones: 45 implementaciones desde cero

Categorías: Manipulación de memoria, strings, conversiones, listas enlazadas, I/O

Características: Gestión robusta de memoria, código optimizado, sin leaks

Objetivo: Dominar fundamentos de C, gestión de memoria y estructuras de datos

🧠 ¿Por qué implementar Libft?
Libft es el proyecto fundamental de 42 que sienta las bases para:

Comprender el funcionamiento interno de las librerías estándar

Dominar la gestión manual de memoria en C

Implementar algoritmos eficientes desde cero

Desarrollar habilidades de debugging y testing

Prepararse para proyectos más complejos

👉 Implementar cada función desde cero me permitió entender los detalles internos de las operaciones más comunes en C, lo que es crucial para escribir código eficiente y seguro.

⚙️ Arquitectura del Proyecto
text
libft/
├── src/                 # Código fuente organizado por categorías
├── inc/                 # Archivos de cabecera
├── Makefile            # Sistema de compilación
└── tests/              # Suite de pruebas
📋 Análisis Detallado de las 45 Funciones
🔤 Funciones de Caracteres (7)
ft_isalpha.c
c
int ft_isalpha(int c);
Verifica si un carácter es alfabético (A-Z, a-z). Implementación eficiente mediante comparaciones de rango.

ft_isdigit.c
c
int ft_isdigit(int c);
Determina si un carácter es un dígito decimal (0-9). Simple pero esencial para validación de entrada.

ft_isalnum.c
c
int ft_isalnum(int c);
Combina isalpha e isdigit para verificar caracteres alfanuméricos.

ft_isascii.c
c
int ft_isascii(int c);
Verifica si un valor está en el rango ASCII estándar (0-127).

ft_isprint.c
c
int ft_isprint(int c);
Determina si un carácter es imprimible (incluye espacio pero excluye caracteres de control).

ft_toupper.c
c
int ft_toupper(int c);
Convierte minúsculas a mayúsculas mediante manipulación aritmética ASCII.

ft_tolower.c
c
int ft_tolower(int c);
Convierte mayúsculas a minúsculas, complemento de toupper.

📝 Funciones de Strings (16)
ft_strlen.c
c
size_t ft_strlen(const char *s);
Calcula la longitud de una string. Implementación optimizada con bucle simple.

ft_strchr.c
c
char *ft_strchr(const char *s, int c);
Busca la primera aparición de un carácter en una string.

ft_strrchr.c
c
char *ft_strrchr(const char *s, int c);
Encuentra la última aparición de un carácter, recorriendo la string desde el final.

ft_strncmp.c
c
int ft_strncmp(const char *s1, const char *s2, size_t n);
Compara dos strings con límite de caracteres, esencial para operaciones seguras.

ft_strnstr.c
c
char *ft_strnstr(const char *big, const char *little, size_t len);
Busca una substring con límite de longitud, implementando algoritmo de búsqueda naive.

ft_strlcpy.c
c
size_t ft_strlcpy(char *dst, const char *src, size_t size);
Copia string con garantía de terminación nula, más segura que strncpy.

ft_strlcat.c
c
size_t ft_strlcat(char *dst, const char *src, size_t size);
Concatena strings con verificación de límites de buffer.

ft_strdup.c
c
char *ft_strdup(const char *s);
Duplica una string con asignación dinámica de memoria.

ft_substr.c
c
char *ft_substr(char const *s, unsigned int start, size_t len);
Extrae una substring con gestión robusta de casos edge.

ft_strjoin.c
c
char *ft_strjoin(char const *s1, char const *s2);
Concatena dos strings en nueva memoria asignada.

ft_strtrim.c
c
char *ft_strtrim(char const *s1, char const *set);
Elimina caracteres especificados del inicio y final de una string.

ft_split.c
c
char **ft_split(char const *s, char c);
Divide una string en un array de substrings usando un delimitador.

ft_strmapi.c
c
char *ft_strmapi(char const *s, char (*f)(unsigned int, char));
Aplica una función a cada carácter de una string, creando un nuevo resultado.

ft_striteri.c
c
void ft_striteri(char *s, void (*f)(unsigned int, char *));
Aplica una función a cada carácter con acceso al índice.

🧠 Funciones de Memoria (7)
ft_memset.c
c
void *ft_memset(void *s, int c, size_t n);
Llena un bloque de memoria con un valor específico.

ft_bzero.c
c
void ft_bzero(void *s, size_t n);
Establece un bloque de memoria a cero, esencial para inicialización.

ft_memcpy.c
c
void *ft_memcpy(void *dest, const void *src, size_t n);
Copia un bloque de memoria, asumiendo que no hay solapamiento.

ft_memmove.c
c
void *ft_memmove(void *dest, const void *src, size_t n);
Copia memoria manejando correctamente posibles solapamientos.

ft_memchr.c
c
void *ft_memchr(const void *s, int c, size_t n);
Busca un byte en un bloque de memoria.

ft_memcmp.c
c
int ft_memcmp(const void *s1, const void *s2, size_t n);
Compara dos bloques de memoria.

ft_calloc.c
c
void *ft_calloc(size_t nmemb, size_t size);
Asigna memoria para un array y la inicializa a cero.

🔢 Funciones de Conversión (2)
ft_atoi.c
c
int ft_atoi(const char *nptr);
Convierte string a entero con manejo de espacios, signos y detección de overflow.

ft_itoa.c
c
char *ft_itoa(int n);
Convierte entero a string, manejando todos los casos edge incluyendo INT_MIN.

📤 Funciones de Output (4)
ft_putchar_fd.c
c
void ft_putchar_fd(char c, int fd);
Escribe un carácter en un file descriptor específico.

ft_putstr_fd.c
c
void ft_putstr_fd(char *s, int fd);
Escribe una string en un file descriptor.

ft_putendl_fd.c
c
void ft_putendl_fd(char *s, int fd);
Escribe una string seguida de un newline.

ft_putnbr_fd.c
c
void ft_putnbr_fd(int n, int fd);
Escribe un número entero en un file descriptor.

🧾 Funciones Bonus - Listas Enlazadas (9)
ft_lstnew_bonus.c
c
t_list *ft_lstnew(void *content);
Crea un nuevo nodo de lista enlazada.

ft_lstadd_front_bonus.c
c
void ft_lstadd_front(t_list **lst, t_list *new);
Añade un nodo al principio de la lista.

ft_lstsize_bonus.c
c
int ft_lstsize(t_list *lst);
Cuenta el número de nodos en una lista.

ft_lstlast_bonus.c
c
t_list *ft_lstlast(t_list *lst);
Encuentra el último nodo de una lista.

ft_lstadd_back_bonus.c
c
void ft_lstadd_back(t_list **lst, t_list *new);
Añade un nodo al final de la lista.

ft_lstdelone_bonus.c
c
void ft_lstdelone(t_list *lst, void (*del)(void *));
Elimina y libera un nodo individual.

ft_lstclear_bonus.c
c
void ft_lstclear(t_list **lst, void (*del)(void *));
Elimina y libera todos los nodos de una lista.

ft_lstiter_bonus.c
c
void ft_lstiter(t_list *lst, void (*f)(void *));
Aplica una función a cada elemento de la lista.

ft_lstmap_bonus.c
c
t_list *ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *));
Crea una nueva lista aplicando una función a cada elemento.

🚀 Uso
bash
# Compilar la biblioteca
make

# Compilar con funciones bonus
make bonus

# Limpiar archivos objeto
make clean

# Limpiar todo y recompilar
make fclean && make

# Usar en tu código
#include "libft.h"

int main(void) {
    char *str = ft_strdup("Hello, Libft!");
    ft_putendl_fd(str, 1);
    free(str);
    return 0;
}
🧠 Decisiones de Diseño Clave
Gestión de Memoria Robusta
Todas las funciones que asignan memoria:

Verifican el retorno de malloc

Calculan tamaños exactos necesarios

Liberan memoria en caso de error

Garantizan terminación nula donde es necesario

Optimización de Algoritmos
Implementaciones eficientes para cada caso de uso

Reutilización de código entre funciones

Minimización de operaciones costosas

Manejo de Edge Cases
Comportamiento definido para parámetros NULL

Manejo correcto de sizes cero

Prevención de overflow y underflow

Compatibilidad con comportamientos estándar

Sistema de Listas Enlazadas
Estructura de datos genérica para contenido de cualquier tipo

Funciones completas de manipulación

Gestión automática de memoria

Interfaz consistente y fácil de usar

🔍 Testing y Calidad
0 memory leaks verificados con Valgrind

100% normativa de 42 School

Test exhaustivo con casos edge

Código documentado y comentado

Optimizado para rendimiento y portabilidad

🧵 Posibles Mejoras Futuras
Añadir más funciones de manipulación de strings

Implementar versiones seguras adicionales

Añadir soporte para wide characters

Implementar más estructuras de datos (árboles, hash maps)

Crear suite de pruebas unitarias completa

🔐 Licencia
MIT - Libre para uso y modificación.

*Desarrollado como parte del currículo de 42 School - 2024*
