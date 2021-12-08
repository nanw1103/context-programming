
# Context Programming

## Concept
A _functional program_ is a program that consists of multiple functional steps, with certain execution order, to complete a task. To be distinguished from daemon-like programs. A run-and-exit script or a workflow are typical examples of functional program.

## Definition of Context Programming
Like a typical computer that consists of _input, output, control unit, compute unit, and memory_, a _functional program_ could be structured as _profile, context, steps, and orchestrator_. As _Context Programming_ pattern.

## Traits Of A Functional Program
- Consists of multiple operations
- Development and maintenance are vital parts of the program lifecycle. So the followings are essential factors:
  - Straightforward: simple to understand, change, and add. Avoid overwhelming abstraction or wrapping.
  - Ideally executable per operation, so it's development-friendly, redo an operation anytime, or resume the workflow at any point.
- As a functional unit in the manner of a black box, it can be integrated with other systems.

## Concepts Explained
- **Profile**: A dynamic input of the entire module. The one-piece concept of _profile_ simplifies the interface and helps integration.
- **Context**: Shared states, generated and used by _Steps_, normally persisted. The _context_ depicts a unified path for data interchange between steps and supports individual step execution.
- **Steps**: fine-grained operations that read from the _profile_ and read from/write to the _context_. Ideally, each _step_ is executable individually.
- **Orchestrator**: streamline the execution of multiple _steps_ according to workflow or condition, generally as the unified entry for the entire module.
