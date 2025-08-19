# 📚 Libft (42) — Custom C Standard Library  

**Implementation of 45 C standard library functions and additional utilities with robust memory management and linked list support.**

![banner](https://raw.githubusercontent.com/placeholder/placeholder/main/assets/libft-banner.png)

---

## 📖 Overview  

* **Language:** C (C99)  
* **Functions:** 45 re-implemented from scratch  
* **Categories:** Memory manipulation, strings, conversions, linked lists, I/O  
* **Highlights:** Robust memory handling, optimized algorithms, no memory leaks  
* **Goal:** Master C fundamentals, memory management, and data structures  

---

## 🧠 Why **Libft**?  

Libft is the **foundational project at 42**. Its purpose is to rebuild core parts of the C standard library and extend them with extra utilities.  

This project allowed me to:  
* Understand the **internal behavior** of the C standard library  
* Learn **manual memory management** (stack, heap, malloc/free)  
* Implement **efficient, safe algorithms**  
* Develop **debugging and testing skills**  
* Create a **personal library** for future projects  

👉 Re-implementing each function from scratch gave me low-level mastery of C and solid preparation for advanced projects.  

---

## ⚙️ Project Architecture  

libft/
├── src/ # Source code organized by categories
├── inc/ # Header files
├── Makefile # Build system
└── tests/ # Test suite

markdown
Copiar
Editar

---

## 📋 Function Categories  

### 🔤 Character Functions (7)  
`ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint`, `ft_toupper`, `ft_tolower`  

### 📝 String Functions (16)  
`ft_strlen`, `ft_strchr`, `ft_strrchr`, `ft_strncmp`, `ft_strnstr`, `ft_strlcpy`, `ft_strlcat`, `ft_strdup`, `ft_substr`, `ft_strjoin`, `ft_strtrim`, `ft_split`, `ft_strmapi`, `ft_striteri`  

### 🧠 Memory Functions (7)  
`ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`, `ft_calloc`  

### 🔢 Conversion Functions (2)  
`ft_atoi`, `ft_itoa`  

### 📤 Output Functions (4)  
`ft_putchar_fd`, `ft_putstr_fd`, `ft_putendl_fd`, `ft_putnbr_fd`  

### 🧾 Bonus — Linked List Functions (9)  
`ft_lstnew`, `ft_lstadd_front`, `ft_lstsize`, `ft_lstlast`, `ft_lstadd_back`, `ft_lstdelone`, `ft_lstclear`, `ft_lstiter`, `ft_lstmap`  

---

## 🚀 Usage  

```bash
# Build the library
make

# Build with bonus functions
make bonus

# Clean object files
make clean

# Clean everything and rebuild
make fclean && make
Using in your code:

c
Copiar
Editar
#include "libft.h"

int main(void) {
    char *str = ft_strdup("Hello, Libft!");
    ft_putendl_fd(str, 1);
    free(str);
    return 0;
}
🧠 Key Design Decisions
✅ Robust Memory Management
All malloc calls are checked

Exact size calculations

Memory freed on errors

Null-termination always guaranteed

⚡ Optimized Algorithms
Efficient and minimal implementations

Code reuse where possible

Reduced costly operations

🛡️ Edge Case Handling
Safe behavior with NULL parameters

Proper handling of zero sizes

Prevention of overflow/underflow

Compatibility with standard library behavior

🔗 Linked List System
Generic structure for any content type

Full set of manipulation functions

Automatic memory handling

Consistent and easy-to-use API

🔍 Testing & Quality
✅ 0 memory leaks (verified with Valgrind)

✅ 100% compliant with 42 School Norm

✅ Extensive testing with edge cases

✅ Well-documented and optimized code

🧵 Possible Future Improvements
Add more string manipulation functions

Implement safer variants of existing ones

Support wide characters

Add advanced data structures (trees, hash maps)

Build a complete unit test suite

🔐 License
MIT — free to use, modify, and distribute.

<p align="center"> <em>Developed as part of the 42 School Curriculum — 2024</em> </p> ```
