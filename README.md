# Monkey Language Interpreter in Go

**A tree-walking interpreter implementation following Thorsten Ball's ["Writing an Interpreter in Go"](https://interpreterbook.com/)**

![Go Version](https://img.shields.io/badge/Go-1.20%2B-blue)

## Features
- **C-like syntax** with familiar operators (`+`, `-`, `*`, `/`, `==`, `!=`)
- **First-class functions** and higher-order functions
- **Closures** with lexical scoping
- **Primitive data types**: integers, booleans, strings
- **Composite types**: arrays and hash maps
- **REPL environment** for interactive evaluation
- **Error handling** with meaningful messages
- **Test-driven development** approach

## Getting Started

### Prerequisites
- Go 1.20+ installed
- Basic understanding of compiler concepts

### Installation
```bash
git clone https://github.com/debitCredit/monkey-go.git
cd monkey-go
go build -o monkey
```

### Using the REPL
```bash
./monkey
```

Example REPL session:
```monkey
> let greet = fn(name) { "Hello " + name + "!" };
> greet("Developer");
"Hello Developer!"
```

## Language Examples

### Variable Binding
```monkey
let pi = 3.14159;
let isMonkeyAwesome = true;
```

### Function Definition
```monkey
let fibonacci = fn(n) {
    if (n <= 1) {
        return n;
    } else {
        fibonacci(n-1) + fibonacci(n-2);
    }
};
```

### Hash Maps
```monkey
let user = {
    "name": "Monkey Developer",
    "age": 42,
    "languages": ["Go", "JavaScript", "Python"]
};
```

## Project Structure
```
.
├── lexer/           # Tokenization implementation
├── parser/          # Pratt parsing implementation
├── ast/             # Abstract Syntax Tree nodes
├── object/          # Runtime object system
├── evaluator/       # Tree-walking evaluation logic
├── repl/            # Read-Eval-Print Loop
└── main.go          # Entry point
```

## Learning Resources
This project follows concepts from:
- ["Writing an Interpreter in Go" by Thorsten Ball](https://interpreterbook.com/)
- [Monkey Language Specification](https://interpreterbook.com/#the-monkey-language)

## Development Roadmap
- [x] Lexical analysis
- [ ] Pratt parser implementation
- [ ] Basic evaluation
- [ ] Garbage collection
- [ ] Bytecode compiler
- [ ] Standard library functions

## Contributing
Pull requests welcome! Please ensure:
- Go fmt compliance
- Accompanying test coverage
- Clear commit messages
