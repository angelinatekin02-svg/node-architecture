# Node.js Architecture Overview

```mermaid
graph TD
    A["👤 User Code"] --> B["Node.js APIs"]
    B --> C["JavaScript Layer<br/>62.3%"]
    
    C --> D["V8 Engine"]
    C --> E["Native Modules"]
    
    D --> F["C++ Layer<br/>23.4%"]
    E --> F
    
    F --> G["libuv<br/>Async I/O"]
    F --> H["OpenSSL<br/>Crypto"]
    F --> I["HTTP Parser"]
    
    G --> J["System Calls"]
    H --> J
    I --> J
    
    J --> K["Operating System"]
    
    style C fill:#f9d71c
    style F fill:#68a063
    style K fill:#e0e0e0
```

## Components

- **JavaScript Layer** (62.3%) - User-facing APIs and Node.js core modules
- **V8 Engine** - Google's JavaScript execution engine
- **C++ Layer** (23.4%) - Core implementation and native bindings
- **libuv** - Cross-platform asynchronous I/O library
- **System Integration** - Direct OS access for networking, file I/O, and timers

## Language Composition

- JavaScript: 62.3%
- C++: 23.4%
- Python: 10.1%
- C: 2.6%
- Other: 1.0%