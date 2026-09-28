# Formal Languages and Compilers — Lab Exercises

Scanners and parsers written with **JFlex** (lexical analysis) and **Java CUP** (LALR(1) parsing) for the *Formal Languages and Compilers* course at Politecnico di Torino.

| Folder | Topic |
|---|---|
| `es1-1` | JFlex basics: recognizing file paths and URLs |
| `es1-2` | URL validation with regular expressions |
| `es1-3` | C source to HTML converter (syntax highlighting) |
| `es2-1` | Scanner for a subset of C |
| `es2-2` | HTML scanner: headings, tables, comments |
| `es3-1` | First CUP parser for a subset of C |
| `es3-2` | Parser for a library catalogue (authors, books, loans) |
| `es3-3` | Grammar for C declarations and statements |
| `es4-1` | Parser for a Prolog-like logic language |
| `es4-2` | Syntax error handling and recovery with the `error` symbol |
| `es5` | Calculator for scalars and vectors with a symbol table |
| `es6` | Reduced-C compiler emitting intermediate code |
| `es7-2` | Type checking of C declarations (pointers, arrays) |
| `exClass-4b` | Restaurant bill calculator with semantic actions |

## Build and run

Requires a JDK, [JFlex](https://jflex.de/) and [Java CUP](http://www2.cs.tum.edu/projects/cup/) on the classpath (tested with JFlex 1.7.0 and CUP 0.11b).

```bash
cd es5
make                  # jflex + cup + javac
java Main example.txt
make clean
```

Folders without a `Makefile` (`es1-*`, `es2-*`) contain only a scanner:

```bash
jflex scanner.jflex && javac *.java && java Yylex input.html
```

## Credits

Driver files (`Main.java`) and some skeletons were provided by the course staff and keep their original author headers. Grammars, scanners and semantic actions are my solutions to the exercises.
