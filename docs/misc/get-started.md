# Getting started with the Rocker platform

Developing a single-page application (SPA) based on Rocker consists of two different kinds of applications - _Main_ and
_Module_; and the _context._

## Context

The context provides a list of modules that are available to the Rocker-based application - to all modules which are
loaded by the Rocker platform. The context is represented in JSON format. It contains a mapping from the module name to
the URL of the module asset and a bunch of additional metadata.

## Module

An isolated piece of functionality. The module may use, and be used by, other modules via `<Module>` React element
provided by the Rocker platform. If a module is used (by another module), the platform lazily loads the module (in a
safe way) from the URL given in the context.

## The _Main_ and SPA

Typically there is one SPA application that is responsible for:

1. providing the top-level HTML page
2. obtaining the Rocker _context_
3. passing the context to the Rocker platform via the `Main` React element

During the initial render of the `Main` Rocker element, Rocker looks into the given _context_ and dynamically loads the
_entry point_ module specified there. The module triggers dynamic loading of other modules which are transitively used
by this entry module.

# Example

`<WIP>`
