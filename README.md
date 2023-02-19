# The Ecosystem
The ecosystem should include a basis of at least the following:
* [Package Manager](Package%20Manager.md)

# Programming Language Wishlist

A series of 5 programming languages based on complexity-layers:
1. A Multimodal Intermediary Language (IL) based on a multimodal type theory (MMTT) that
  * can be reduced and compiled, or interpreted, into any of
    * WASM
    * Machine Code
  * can be validated against specific requirements to be used as standards for targets like
    * database queries (for relational databases, graph databases, etc.)
    * quantum computers
    * GPGPUs
    * a language describing valid communication sessions between client-and-server
  * can be further validated against environmental settings to generate state-languages
    * for Infrastructure-as-Code (IaC)
    * for Programmable configuration settings
    * for FPGA, ASIC, PLC, and other PLD settings
    
2. A Multimodal language with access to the modalities to create primitives
  * Primitives, such as freshness, glue, weld, extent, gel, mill, etc.    
  * A clock-type for guarded recursion
  * Various linearity axioms
    * Relevant
    * Affine
    * Uniqueness  
  * Directed Types
    * Dependent categories (and categories-with-families)
    * A proof of directed univalence
  * Undirected Types
    * A proof of undirected univalence
    * An Identity Type
    * A proof of function extensionality
  * Representations of the following, with some isomorphisms
    * Unbounded Unsigned Integers with Binary Representations and the Trivial Natural Numbers (Infinite Cyclic Group)
    * Bounded Unsigned Integers with (2^n) Binary Representations and Circular Group Rings
      * A Multiply-Accumulate
    * Unbounded Signed Integers with Binary Representations
    * Bounded Signed Integers with Binary Representations
    * Interrupts as tagged
    
    
3. A lazy-pure-functional language with strictness markers
  * That can compile
    * Directly into the IL
    * Into the Multimodal language, in order to bring additions if necessary
  * That evaluates much like Idris or other Haskell variants
  * Can create production code
  * Can use as a proof assistant
  * Comes with literate options
  * Has a Prelude library with the following
  * Has an operator-import, such that any program can select an operator-style
    * Operators on Semigroupoid
      * (>>) compose to the right
      * (<<) compose to the left
    * Operators on Applicative
      * (<|) apply to the left
      * (|>) apply to the right
      * (<||) uncurry to the left
      * (||>) uncurry to the right
    ... (unfinished)
    * Operators on comonads
    
4. An eager Ada-style language, similar to C#
  * For any defined type, in order to give it similarity to OOP, `this` is implicitly passed as the **last** parameter, instead of the first parameter
    * (.) is defined as left apply and auto-curry, such that the following would be interpreted by #3 as:
      * `person.name` would have been `name person`
      * `manager.addEmployee(person, "developer")` would have been `addEmployee person "developer" manager` or `manager |> addEmployee person "developer"`
  *  `this` has the property that it comes at the **end** of the function, instead of the beginning
  * Operator-style has the following:
    * Treating `Opt<T>` as a monad:
      * (?.) means 
    * Since pointers are bimonads:
      * (&) 



Person.Name

Name : Person -> string

Opt<Person> -> string

person?.Name

person >>= Name?????

