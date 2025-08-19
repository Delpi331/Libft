# 📚 Libft (42) — Biblioteca Estándar de C Personalizada

📌 Badges:

[![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)]()
[![42 School](https://img.shields.io/badge/42-School-blue?style=for-the-badge)]()
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)]()
[![45 Functions](https://img.shields.io/badge/45-Functions-orange?style=for-the-badge)]()

---

## 📖 Resumen

**Libft** es el proyecto fundamental de **42 School**, que consiste en la **implementación personalizada de 45 funciones** de la biblioteca estándar de C, junto con utilidades adicionales.  
Esta librería sirve como base sólida para futuros proyectos, ya que permite comprender en profundidad **gestión de memoria, strings, I/O y listas enlazadas**.

- **Lenguaje:** C (C99)  
- **Funciones:** 45 en total  
- **Categorías:** Manipulación de memoria, strings, conversiones, listas enlazadas, I/O  
- **Características:** Gestión robusta de memoria, código optimizado, sin memory leaks

---

## 🧠 ¿Por qué implementar Libft?

Crear Libft desde cero permitió:  

- Comprender el **funcionamiento interno** de las librerías estándar de C  
- Dominar la **gestión manual de memoria** (stack vs heap, malloc/free)  
- Escribir **algoritmos eficientes y seguros**  
- Desarrollar habilidades de **debugging y testing**  
- Construir una **base confiable** para proyectos más complejos  

---

## ⚙️ Arquitectura del Proyecto

libft/
├── src/ # Código fuente organizado por categorías
├── inc/ # Archivos de cabecera
├── Makefile # Sistema de compilación
└── tests/ # Suite de pruebas

yaml
Copiar
Editar

---

# 📋 Funciones Detalladas

Cada función incluye: descripción, explicación técnica, manejo de memoria, ejemplos y notas de diseño.

---

## 🔤 Funciones de Caracteres (7)

### 🔹 ft_isalpha.c
**Función:** Verifica si un carácter es alfabético (A-Z, a-z).  

**Explicación técnica:**  
- Compara el valor ASCII del carácter con los rangos de mayúsculas y minúsculas.  
- No requiere memoria dinámica.  

**Ejemplo:**
```c
#include "libft.h"
#include <stdio.h>

int main() {
    printf("%d\n", ft_isalpha('A')); // 1
    printf("%d\n", ft_isalpha('1')); // 0
}
```
Notas: Implementación simple, rápida y segura.

🔹 ft_isdigit.c
Función: Comprueba si un carácter es un dígito (0-9).

Explicación técnica:

Comparación de rango ASCII.

Útil para validación de entradas numéricas.

Ejemplo:

```c
ft_isdigit('5'); // 1
ft_isdigit('a'); // 0
```

🔹 ft_isalnum.c
Función: Comprueba si un carácter es alfanumérico.

Explicación técnica:

Combina ft_isalpha y ft_isdigit.

Ejemplo:

```c
ft_isalnum('A'); // 1
ft_isalnum('7'); // 1
ft_isalnum('%'); // 0
```

🔹 ft_isascii.c
Función: Verifica si un valor está en el rango ASCII (0-127).

Explicación técnica:

Garantiza compatibilidad con funciones de C que esperan valores ASCII.

Ejemplo:

```c
ft_isascii(128); // 0
ft_isascii(65);  // 1
```
🔹 ft_isprint.c
Función: Comprueba si un carácter es imprimible.

Explicación técnica:

Incluye espacio pero excluye caracteres de control (0-31, 127).

🔹 ft_toupper.c
Función: Convierte minúsculas a mayúsculas.

Explicación técnica:

Manipulación aritmética de ASCII (c - 32 si está en rango 'a'-'z').

🔹 ft_tolower.c
Función: Convierte mayúsculas a minúsculas.

Explicación técnica:

Complemento de ft_toupper.

📝 Funciones de Strings (16)
🔹 ft_strlen.c
Función: Calcula la longitud de una cadena.

Explicación técnica:

Recorre la cadena hasta encontrar \0.

No requiere memoria dinámica.

Ejemplo:

```c
ft_strlen("Hola"); // 4
```
Notas: Seguro con cadenas vacías.

🔹 ft_strchr.c
Función: Busca la primera aparición de un carácter.

Explicación técnica:

Recorre la cadena y devuelve puntero al primer match.

Memoria: No reserva memoria adicional.

🔹 ft_strrchr.c
Función: Busca la última aparición de un carácter.

Explicación técnica:

Recorre toda la cadena para devolver el último match.

🔹 ft_strncmp.c
Función: Compara dos cadenas hasta n caracteres.

Explicación técnica:

Evita leer memoria fuera de rango.

🔹 ft_strnstr.c
Función: Busca una substring dentro de un límite de longitud.

Explicación técnica:

Algoritmo naive de búsqueda.

Retorna puntero al inicio de la substring o NULL.

🔹 ft_strlcpy.c
Función: Copia string asegurando terminación nula.

Explicación técnica:

Evita overflows.

🔹 ft_strlcat.c
Función: Concatena strings asegurando buffer.

🔹 ft_strdup.c
Función: Duplica una cadena en memoria dinámica.

Explicación técnica:

Reserva memoria con malloc.

Copia carácter por carácter y termina en \0.

Usuario debe usar free.

Ejemplo:

```c
char *copy = ft_strdup("Hola");
free(copy);
```
🔹 ft_substr.c
Función: Extrae una substring.

Explicación técnica:

Maneja límites de inicio y longitud.

Reserva memoria dinámica.

🔹 ft_strjoin.c
Función: Concatena dos strings en nueva memoria.

Explicación técnica:

Calcula longitud total y reserva memoria.

Copia las dos cadenas y añade terminador nulo.

🔹 ft_strtrim.c
Función: Elimina caracteres al inicio y final de un string.

Explicación técnica:

Itera desde ambos extremos.

Reserva nueva memoria.

🔹 ft_split.c
Función: Divide un string por un delimitador en un array de strings.

Explicación técnica:

Cuenta palabras, reserva memoria para cada una.

Incluye terminador NULL al final del array.

🔹 ft_strmapi.c
Función: Aplica función a cada carácter y retorna nuevo string.

Explicación técnica:

Reserva memoria para string nuevo.

No altera original.

🔹 ft_striteri.c
Función: Aplica función a cada carácter in-place con índice.

🧠 Funciones de Memoria (7)
🔹 ft_memset.c
Función: Rellena un bloque de memoria con un valor.

🔹 ft_bzero.c
Función: Inicializa memoria a cero.

🔹 ft_memcpy.c
Función: Copia memoria (sin solapamiento).

🔹 ft_memmove.c
Función: Copia memoria manejando solapamiento.

🔹 ft_memchr.c
Función: Busca un byte en un bloque de memoria.

🔹 ft_memcmp.c
Función: Compara bloques de memoria.

🔹 ft_calloc.c
Función: Reserva memoria para un array y lo inicializa a cero.

🔢 Funciones de Conversión (2)
🔹 ft_atoi.c
Función: Convierte string a entero.

🔹 ft_itoa.c
Función: Convierte entero a string (maneja INT_MIN).

📤 Funciones de Output (4)
🔹 ft_putchar_fd.c
🔹 ft_putstr_fd.c
🔹 ft_putendl_fd.c
🔹 ft_putnbr_fd.c
Escriben en file descriptor, útiles para output controlado.

🧾 Funciones Bonus — Listas Enlazadas (9)
🔹 ft_lstnew.c
🔹 ft_lstadd_front.c
🔹 ft_lstsize.c
🔹 ft_lstlast.c
🔹 ft_lstadd_back.c
🔹 ft_lstdelone.c
🔹 ft_lstclear.c
🔹 ft_lstiter.c
🔹 ft_lstmap.c
Implementación genérica de listas

Gestión automática de memoria

Funciones completas de manipulación

🚀 Uso
bash
Copiar
Editar
make
make bonus
make clean
make fclean && make
Ejemplo:

```c
#include "libft.h"

int main() {
    char *str = ft_strdup("¡Hola, Libft!");
    ft_putendl_fd(str, 1);
    free(str);
    return 0;
}
```

🧠 Decisiones de Diseño
Robustez de memoria

Optimización de algoritmos

Manejo de edge cases

Listas enlazadas genéricas y seguras

🔍 Testing y Calidad
Sin leaks (Valgrind)

Cumple normativa 42

Pruebas exhaustivas

Código comentado y optimizado

🧵 Mejoras Futuras
Más funciones de strings

Soporte wide characters

Nuevas estructuras (árboles, hash maps)

Suite de pruebas completa

🔐 Licencia
MIT — Libre para uso y modificación.
Desarrollado como parte del currículo de 42 School - 2024
