
# Resumable Script Pattern

Like a typical computer that consists of input, output, control unit, compute unit, and memory, a complex resumable script module, should generally be structured as profile, context, step scripts, and orchestrator. As _Resumable Script Pattern_.

## Traits Of A Complex Script Model
- Consists of multiple operations
- Development and maintenance are vital parts of the script lifecycle. So the followings are essential factors:
  - Straightforward: simple to understand, change, and add. Avoid overwhelming abstraction or wrapping.
  - Ideally executable per operation, so it's development-friendly, redo an operation anytime, or resume the workflow at any point.
- As a functional unit in the manner of a black box, it can be integrated with other systems.

## Concepts Explained
- *Profile*: dynamic input to the entire script module. The one-piece concept of _profile_ simplifies the interface and helps integration.
- *Context*: shared states, generated and used by _Step Scripts_, normally persisted. The _context_ depicts a unified path for data interchange between steps and supports individual step execution.
- *Step Scripts*: fine-grained scripts that read from the _profile_ and read from/write to the _context_. Ideally, each _step script_ is executable individually.
- *Orchestrator*: streamline the execution of multiple _step scripts_ according to workflow or condition, generally as the unified entry for the script module.
