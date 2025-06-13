# MeTTa-WAM Architecture Documentation

## Overview

The MeTTa-WAM (Meta-learning Warren Abstract Machine) represents a revolutionary cognitive architecture that transmutes functional programming into relational programming, enabling neural-symbolic integration through hypergraph-centric computation. This system facilitates distributed cognition by transforming implicit architectural patterns into explicit, actionable knowledge.

## High-Level System Architecture

```mermaid
graph TD
    subgraph "Cognitive Layer"
        A[MeTTa Language Core] --> B[Functional→Relational Transformer]
        B --> C[Hypergraph Knowledge Space]
        C --> D[Neural-Symbolic Integration]
    end
    
    subgraph "Execution Layer"
        E[WAM Engine] --> F[Logic Programming Runtime]
        F --> G[Constraint Logic Programming]
        G --> H[Probabilistic Inference]
    end
    
    subgraph "Integration Layer"
        I[Python Interface] --> J[Jupyter Kernel]
        I --> K[PyTorch Neural Networks]
        I --> L[Hyperon Reference]
        M[C# Debugger Core] --> N[Mono.Cecil Reflection]
        M --> O[JDWP Protocol]
    end
    
    subgraph "Persistence Layer"
        P[AtomSpace] --> Q[Knowledge Base]
        P --> R[Type System]
        P --> S[Ontological Relations]
    end
    
    A --> E
    D --> I
    D --> M
    E --> P
    I --> P
    M --> P
    
    style A fill:#e1f5fe
    style E fill:#f3e5f5
    style I fill:#e8f5e8
    style P fill:#fff3e0
```

## Core Module Interaction Patterns

```mermaid
graph LR
    subgraph "Parser Subsystem"
        P1[metta_parser.pl] --> P2[AST Generator]
        P2 --> P3[Syntax Validator]
    end
    
    subgraph "Compiler Subsystem"
        C1[metta_compiler.pl] --> C2[Functional Transform]
        C2 --> C3[Relational Generator]
        C3 --> C4[WAM Code Generator]
        C5[metta_compiler_douglas.pl] --> C2
        C6[metta_compiler_roy.pl] --> C2
    end
    
    subgraph "Runtime Subsystem"
        R1[metta_runtime.pl] --> R2[Eval Engine]
        R2 --> R3[Space Manager]
        R3 --> R4[Type Checker]
        R5[metta_interp.pl] --> R2
    end
    
    subgraph "Integration Subsystem"
        I1[metta_python.pl] --> I2[Janus Bridge]
        I2 --> I3[Python Executor]
        I4[Jupyter Kernel] --> I2
        I5[PyTorch Interface] --> I2
    end
    
    P3 --> C1
    C4 --> R1
    R4 --> I1
    
    style P1 fill:#bbdefb
    style C1 fill:#c8e6c9
    style R1 fill:#ffcdd2
    style I1 fill:#f8bbd9
```

## Neural-Symbolic Integration Architecture

```mermaid
sequenceDiagram
    participant MeTTa as MeTTa Language
    participant Transformer as Functional→Relational
    participant WAM as WAM Engine
    participant Neural as Neural Networks
    participant Space as AtomSpace
    participant Inference as Probabilistic Inference
    
    MeTTa->>Transformer: Function Definition
    Note right of Transformer: (= (fib $n) ...) → relational form
    Transformer->>WAM: Relational Clauses
    WAM->>Space: Assert Relations
    
    Neural->>Space: Neural Predictions
    Space->>Inference: Combined Knowledge
    Inference->>WAM: Query Constraints
    WAM->>Space: Unified Results
    
    Space->>MeTTa: Answer Bindings
    MeTTa->>Neural: Feedback Signal
    
    Note over MeTTa,Neural: Adaptive Attention Allocation
    Note over Space,Inference: Hypergraph Pattern Matching
```

## Data Flow and Signal Propagation

```mermaid
stateDiagram-v2
    [*] --> Parsing
    Parsing --> FunctionalForm: MeTTa Code
    FunctionalForm --> RelationalTransform: Add Return Args
    RelationalTransform --> WAMCompilation: Generate Clauses
    WAMCompilation --> RuntimeExecution: Execute Logic
    
    state RuntimeExecution {
        [*] --> Unification
        Unification --> ConstraintSolving
        ConstraintSolving --> ProbabilisticReasoning
        ProbabilisticReasoning --> NeuralIntegration
        NeuralIntegration --> ResultBinding
        ResultBinding --> [*]
    }
    
    RuntimeExecution --> KnowledgeSpace: Store/Retrieve
    KnowledgeSpace --> HypergraphMatching: Pattern Recognition
    HypergraphMatching --> AdaptiveAttention: Optimize Allocation
    AdaptiveAttention --> RuntimeExecution: Update Strategy
    
    RuntimeExecution --> [*]: Complete
    
    note right of RelationalTransform
        Transform: (= (f $x) (+ $x 1))
        Into: (==> (plus $x 1 $ret) (f $x $ret))
    end note
    
    note right of HypergraphMatching
        Enables query optimization methods
        from knowledge-base domain in
        program execution context
    end note
```

## Component Relationship and Dependencies

```mermaid
graph TB
    subgraph "Language Core"
        LC1[metta_eval.pl]
        LC2[metta_types.pl]
        LC3[metta_space.pl]
        LC4[metta_utils.pl]
    end
    
    subgraph "Compiler Stack"
        CS1[metta_compiler.pl]
        CS2[metta_compiler_lib.pl]
        CS3[metta_transpiled_header.pl]
        CS4[metta_mizer.pl]
    end
    
    subgraph "Runtime Environment"
        RE1[metta_runtime.pl]
        RE2[metta_threads.pl]
        RE3[metta_persists.pl]
        RE4[metta_repl.pl]
    end
    
    subgraph "Testing Framework"
        TF1[metta_testing.pl]
        TF2[metta_debug.pl]
        TF3[Unit Test Examples]
    end
    
    subgraph "Python Integration"
        PI1[metta_python.pl]
        PI2[metta_jupyter_kernel.py]
        PI3[hyperon_ref/]
        PI4[PyTorch Integration]
    end
    
    subgraph "C# Debugging Infrastructure"
        CD1[Debugger.Core]
        CD2[Mono.Cecil.*]
        CD3[JDWP Protocol]
        CD4[Reflection Visitors]
    end
    
    LC1 --> CS1
    LC2 --> CS1
    LC3 --> CS1
    LC4 --> CS1
    
    CS1 --> RE1
    CS2 --> RE1
    CS3 --> RE1
    
    RE1 --> TF1
    RE2 --> TF1
    
    LC1 --> PI1
    RE1 --> PI1
    PI1 --> PI2
    PI1 --> PI3
    
    TF1 --> CD1
    RE1 --> CD1
    CD1 --> CD2
    CD1 --> CD3
    
    style LC1 fill:#e3f2fd
    style CS1 fill:#f1f8e9
    style RE1 fill:#fce4ec
    style TF1 fill:#fff8e1
    style PI1 fill:#e8f5e8
    style CD1 fill:#f3e5f5
```

## Emergent Cognitive Patterns

### Recursive Implementation Pathways

The system exhibits recursive cognitive patterns through multiple architectural layers:

1. **Functional Recursion → Relational Recursion**: Functions like `(fib $n)` become self-referential relations with constraint propagation
2. **Meta-Circular Evaluation**: The MeTTa interpreter can reason about its own evaluation processes
3. **Hypergraph Recursion**: Knowledge patterns recursively reference and expand through the atomspace

### Adaptive Attention Allocation Mechanisms

```mermaid
flowchart TD
    A[Query Input] --> B{Attention Classifier}
    B -->|High Priority| C[Direct WAM Execution]
    B -->|Medium Priority| D[Constraint Optimization]
    B -->|Low Priority| E[Probabilistic Sampling]
    B -->|Unknown Pattern| F[Neural Network Inference]
    
    C --> G[Result Cache]
    D --> G
    E --> G
    F --> H[Pattern Learning]
    H --> I[Attention Model Update]
    I --> B
    
    G --> J[Hypergraph Integration]
    J --> K[Knowledge Base Update]
    K --> L[Global Pattern Recognition]
    L --> B
    
    style B fill:#ffeb3b
    style F fill:#4caf50
    style H fill:#ff9800
    style L fill:#9c27b0
```

### Cognitive Synergy Optimizations

The architecture achieves cognitive synergy through:

- **Cross-Modal Learning**: Neural predictions inform symbolic reasoning and vice versa
- **Temporal Coherence**: State maintenance across recursive evaluation cycles
- **Emergent Abstraction**: Higher-order patterns emerge from low-level symbolic manipulation
- **Distributed Inference**: Computation distributes across multiple reasoning modalities

## Integration Points and Bridges

### Python-Prolog Bridge (Janus)

```mermaid
sequenceDiagram
    participant Python as Python Module
    participant Janus as Janus Bridge
    participant Prolog as SWI-Prolog
    participant MeTTa as MeTTa Runtime
    
    Python->>Janus: py_call/N
    Janus->>Prolog: Goal Execution
    Prolog->>MeTTa: Eval Request
    MeTTa->>Prolog: Result Binding
    Prolog->>Janus: Success/Failure
    Janus->>Python: Return Value
    
    Note over Python,MeTTa: Bidirectional communication enables<br/>neural-symbolic fusion
```

### C# Debugging Integration

The C# debugging infrastructure provides deep introspection capabilities:

- **Mono.Cecil**: Assembly analysis and code reflection
- **JDWP Protocol**: Remote debugging and process control
- **Visitor Patterns**: Systematic traversal of code structures
- **Metadata Extraction**: Type information and dependency analysis

## Future Architectural Evolution

The system's hypergraph-centric design enables continuous architectural evolution through:

1. **Pattern Emergence**: New computational patterns emerge from symbolic-neural interaction
2. **Self-Modification**: The system can reason about and modify its own architecture
3. **Distributed Cognition**: Multiple reasoning agents can collaborate within the same atomspace
4. **Quantum-Ready**: The relational foundation supports future quantum computing integration

## Technical Implementation Notes

### Warren Abstract Machine Optimization

The WAM engine provides efficient execution through:
- First-argument indexing for predicate dispatch
- Structure sharing for term representation
- Tail-call optimization for recursive functions
- Cut elimination for deterministic execution paths

### Type System Integration

The ontological type system bridges:
- Regular types (functional programming)
- Dependent types (theorem proving)
- Ontological types (knowledge representation)
- Neural types (continuous embeddings)

This comprehensive architecture documentation captures the emergent, recursive, and adaptive nature of the MeTTa-WAM system, facilitating distributed cognition for all contributors through precise technical exposition and visual architectural mapping.