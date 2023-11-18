
# Modular Architecture for Pixflow Application

A modular architecture refers to organizing your codebase into modular, reusable components. This approach helps in maintaining a clear and scalable code structure. Each component should ideally represent a self-contained and reusable piece of the user interface.

The modular architecture diagram illustrates a straightforward, scalable design that aligns with our core principles.


insert a image


### Note: Each arrowhead in the above diagram symbolizes an import statement.

## Core Principles

#### Modules Isolation:
Each module should be encapsulated with its own set of dependencies, and it  must be cognizant of all the dependencies it relies on, providing a designated entry point for all its APIs.

#### No-circular Dependency
Modules should refrain from importing one another to adhere to the Acyclic 	Dependencies Principle, preventing circular dependencies within the system.

#### Dependent Modules
Independent modules exhibit loose coupling with other modules, except for shared modules within the application. This flexibility allows us to outsource them to an external library.

### Dependent Modules

#### Application

The application/root module essentially serves as the aggregation or composition of containers. Its role includes initializing the application with react-suspense, error boundaries, and any top-level providers.

#### Containers

The containers module is a collection of smart components that are connected to the state via the hooks. As you can see that the containers modules only import common, components and hooks modules and it doesn’t concern the state module at all. This helps us to scale the hooks module without affecting the states.

#### Hooks

The hooks module supplies data to the containers through the state and also updates the state based on the user interaction with the container components.

#### State

The state module takes on the responsibility of populating the client-side state utilizing the service and common modules. This approach helps us prevent the containers and hooks from being cluttered with service APIs.


### Independent Modules

#### Components

The components module is simply a compilation of purely functional components that remain indifferent to the application state. While it could be entirely independent, resembling an external library, there's a possibility of creating application-specific components that closely mirror the data types from the common module. Therefore, it proves beneficial to distinguish between generic and specific components. Generic components refrain from utilizing any types from the common modules, facilitating their potential relocation to an external component library.

#### Services

The services module constitutes a collection of APIs that interact with the backend, ensuring that the resulting response aligns with the core data types present in our common modules.


## React-Redux Architecture Overview

image 2

## The Front End Diagram