# cxx_metro
Clang tool reporting C++ metrics

The idea of thi clang tool is to compile together metrics related to the different C++ entities, as e.g. other non-public tools do.
While we have some clang-tidy checkers that report an isse as soon as a specific threshold is reached, we don't have an idea of the specific KPI all around the project and how this KPI can evolve.

An idea is to extract from readability-function-size clang-tidy-checker the following KPIs

Some ideas of the metrics are:

* Function 
  * MacCabe complexity
  *  Number of Lines
  *  Number of Statements
    This may differ significantly from the number of lines for macro-heavy code
  *  Number of Branches
  *  Number of Parameters
  *  Number of whitespace characters used for indentation
  *  Maximum Nesting Level
    Count compound statements which create next nesting level. This may differ significantly from the expected value for macro-heavy code. 
  * Number of Local variables
    Please note that function parameters and variables declared in lambdas, GNU Statement Expressions, and nested class inline functions are not counted.

* Classes
  * Number of base classes
  * Number of nested types (public/protected/private)
  * Number of functions members (static or not public/protected/private)
  * Number of data members (static or not public/protected/private)
  
* Files
  * Number of included files
  
* Namespaces
  * Level
  

