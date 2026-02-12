# get_nextline
This project has been created as part of the 42 curriculum by lurenaul

## Description

The **get_nextline** project is a C programming function that reads a line from a file descriptor. This function is designed to return one line at a time from a text file or standard input, handling multiple file descriptors simultaneously and managing memory efficiently.

The main goal is to understand static variables, dynamic memory allocation, and file manipulation in C, while creating a reusable utility function that will be helpful in future 42 projects.

### Key Features
- Reads one line at a time from any valid file descriptor
- Handles multiple file descriptors without losing track of reading position
- Efficient buffer management with configurable BUFFER_SIZE
- Proper memory management with no leaks

### 42 Resources
- 42 Norm documentation
- get_next_line subject PDF (available on your 42 intranet)

### AI Usage
AI tools were **not used** in the development of this project to ensure full understanding of:
- Static variable behavior and lifetime
- File descriptor management and the read() system call
- Dynamic memory allocation strategies
- Buffer management techniques
- Edge case handling (EOF, errors, varying buffer sizes)

*If AI was used for any specific task, specify here which parts and for what purpose (e.g., debugging specific edge cases, understanding man pages, etc.)*

## Technical Choices

- **Buffer Size**: Configurable via compilation flag to test different performance scenarios
- **Static Variables**: Used to maintain reading state between function calls
- **Memory Management**: All allocated memory is properly freed; valgrind clean with no leaks
- **Error Handling**: Returns NULL on error or EOF; robust against invalid file descriptors

## Project Files

- `get_next_line.c` - Main function implementation
- `get_next_line_utils.c` - Helper functions (ft_strlen, ft_strchr, ft_strjoin, etc.)
- `get_next_line.h` - Header file with function prototypes and includes

## Testing

Test with various scenarios:
- Different BUFFER_SIZE values (1, 42, 1024, 10000)
- Multiple file descriptors simultaneously
- Large files and empty files
- Files with and without final newline
- Standard input (stdin)

## Author
lurenaul
