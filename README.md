GobiesVM
=====

[![Build Status](https://travis-ci.org/brucehsu/GobiesVM.svg?branch=master)](https://travis-ci.org/brucehsu/GobiesVM)
[![License](https://img.shields.io/badge/license-MIT-green.svg?style=flat)](https://github.com/brucehsu/GobiesVM/blob/master/LICENSE)

A Ruby VM written in Go aims to exploit parallelism via Software Transactional Memory.

# Build
```
git clone https://github.com/brucehsu/GobiesVM.git
cd GobiesVM
make goenv
source goenv
make
```

The executable will be placed inside ``bin/``.

# Usage
```
gobiesvm [OPTIONS] RBFILE

Options:
  -ast: Print abstract syntax tree structure
  -bench=[0]: Benchmark script execution speed (without parsing stage)
  -bytecode: Print comprehensive bytecode instructions
  -log: Log transaction status
```

# What is supported
- Object manipulations (creation, method calling)
- Variable assignment
- Integer
- Float
- String (single-quoted)
- Basic string operations
- Blocks
- Iterators
- Arrays
- Hashes
- Threads
- Basic IO

# What is NOT supported (yet)
- Conditional statements
- Class/method definition
- Native extension interface
- Rubygems

# Related Paper
> [Software Transactional Memory in a Dynamic Programming Language at Virtual Machine Level](http://handle.ncl.edu.tw/11296/ndltd/49813811049358903093)
