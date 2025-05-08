# What are some differences between interfaces and types in TypeScript?

**Introduction:** In typescript, both type and `interface` are used for defining structure like objects. Both have different purposes but work the same meanwhile `interface` uses for `object` structure most useful feature of it is extendable. But type is more versatile, it uses for unions intersection and more complex definitions.

**Declaration:** Interfere supports multiple `interfaces` with the same name that is known as declaration merging. While `type` does not support this feature. 

**Flexibility:** Type has multiple uses such as defining union, intersection and `tuples`, Where interfaces are primarily designed for using in `objects`.

**Performance:** In Typescript, there are slight differences in performance between type and interface. `Interfaces` can provide slightly less performance than type during type checking, because they create a single flat object type that detects property conflicts efficiently, Types especially when using Unions and intersections. Differences are very minimal and these are not noticeable in most projects. 

**Use cases:** 
	**When to use `type`:**
Use `type` when defining an alias for primitive types (string, boolean, number, bigint, symbol, etc)
Use `type` when defining tuple types
Use `type` when defining function types
Use `type` when defining a union
Use `type` when trying to overload functions in object types via composition
Use `type` when needing to take advantage of mapped types
When to use interface:
Use `interface` for all object types where using type is not required (see above)
Use `interface` when you want to take advantage of declaration merging.

Feature difference between `type` and `interfere`: In the context of TypeScript, the core difference between type and interface lies in their flexibility and how they handle type aliases.


### Feature Comparison Between Type and Interface in TypeScript

| **Feature**                         | **Type**                                                    | **Interface**                                                |
|-------------------------------------|-------------------------------------------------------------|-------------------------------------------------------------|
| **Flexibility**                     | More flexible than interface.                               | Less flexible compared to type.                             |
| **Merged Declarations**             | Does not support multiple merged declarations.              | Supports multiple merged declarations.                      |
| **Name Conflicts**                  | Two types with the same name raise an exception.            | Two interfaces with the same name get merged.                |
| **Implementation**                  | Does not have implementation purposes.                      | Used for implementation and extending in classes.           |
| **Union Types**                     | Does not support implementing or extending union types.     | Supports implementing and extending union types.            |
| **Intersection Types**              | Can create intersection types by combining multiple types.  | Cannot create intersection interfaces.                       |
| **Usage with Primitives, Unions, and Tuples** | Can be used for types like primitives, unions, and tuples. | Cannot be used with other types of declaration.              |



<br><br><br><br>






# What is the use of enums in TypeScript? Provide an example of a numeric and string enum.

**Introduction:** Enums, short for enumerations, provide a way to define a set of named constants in TypeScript. Developers can define a set of named constants. Using enums can make it easier to read code, creating a set of distinct cases. TypeScript provides both numeric and string-based enums. It provides well organized code and manages related values, making code more readable and maintainable.

**Numeric enums**: A numeric enum is a type that creates a set of named constants.
Key characteristics of numeric enums are named constants, numeric values, Default initialization, Explicit, initialization..

**String enums:** A set of named constants, where each constant is associated with a string value. Key characteristics of string enums: String Values, meaningful Values, serialization.

**Why Use Enums?** 
- Enums can be used as types for variables, function parameters, and return types, ensuring type safety and improving code clarity.
- Readability: Makes code easier to understand (Status.Active is more meaningful than 1).
- Safety: Helps prevent invalid values.
- Maintainability: Centralizes value definitions in one place.


**Purpose of Enums:** 
  1. Enums allows the creation of a group of constant data under a single name.
  2. It enhances the code readability and provides type safety with effective maintenance.
  3. It can handle different states of an application
  4. Helps to avoid using raw data like strings or numbers and ensure consistency.


**Limitations:**
- Runtime Code: Enums generate JavaScript code, increasing bundle size.
- No Tree Shaking: They cannot be removed during optimization if unused.
- Poor Interop: Not easily shared with plain JavaScript.
- Limited Flexibility: Can't be extended or composed.
- Confusing Behavior: Numeric enums support reverse mapping, which can cause bugs.
- Better Alternatives: const objects with union types are more flexible and safer.

 **Advantages of Enums**
- Improves code readability and maintainability
- Enables type checking at compile time, reducing runtime errors
- Enhances developer experience with auto-completion and IntelliSense
- Prevents hardcoding by centralizing constant values

**Conclusion:** Enums in TypeScript are a way to define a set of named constants, improving code readability and maintainability. They can be numeric or string-based and are useful for representing fixed sets of values. Enums enable compile-time type checking, reducing runtime errors and enhancing the developer experience with features like IntelliSense and auto-completion. They also help prevent hardcoding by centralizing constant values in one place. However, they introduce runtime code and may not be easily tree-shaken, making alternatives like const objects or union types sometimes preferable.