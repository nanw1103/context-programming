# Context Programming

## Background
A _functional program_ is a program that consists of multiple functional steps, with certain execution orders, to complete a task. To be distinguished from daemon-like programs. A run-and-exit script or a workflow are typical examples of a functional program.

## What is Context Programming
Like a typical computer that consists of _input, output, control unit, compute unit, and memory_, a _functional program_ could be structured as _profile_, _context_, _steps_, and _orchestrator_. As _Context Programming_ pattern.

## Concepts Explained
- **Profile**: The input of the entire module. The one-piece concept of _profile_ simplifies the interface and helps integration. Profile is ideally read-only.
- **Context**: Runtime generated states, shared between _Steps_, normally persisted. The _context_ depicts a unified path for data interchange between steps and supports individual step execution.
- **Steps**: fine-grained operations that read from the _profile_ and read from/write to the _context_. Ideally, each _step_ is executable individually.
- **Orchestrator**: streamline the execution of multiple _steps_ according to workflow or condition, generally as the unified entry for the entire module.


![The Context Programming Pattern](images/context-programming.png?raw=true)

## The Core of Context Programming

_Context Programming helps to achieve a shallow learning curve and low maintenance cost via unit operability._

- **Unit-operability**: Every unit (step) is executable because all required inputs are from profile and context, which is available anytime if persisted. The unit-operability enables single-unit execution, so minimize the testing and debugging effort, by shifting bug discovery from integration verification to unit verification. The more complex the integration is, the more value this point holds. Identifying an issue during integration is more costly than identifying it earlier in the unit verification phase.
 
- **Shallow learning curve**: By separating the whole task into isolated steps, each part will be more straightforward to understand, change, and add. Steps are normally organized intuitively.
 
- **Low maintenance cost**: In many cases, development and maintenance are vital parts of the program lifecycle. An easy-to-understand program is likely easy to maintain. The pattern by its nature leads people away from overwhelming abstraction or wrapping.

- **Integration matters**: As a functional unit in the manner of a black box, it's easy to be integrated with other systems.


## Example
*WIP*
