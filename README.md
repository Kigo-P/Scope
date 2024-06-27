### What is scope in JavaScript, and why is it important?
 - The scope in Javascript is where the values and expressions can be accessed and can be referenced.
 - It helps in the visibility of the values and expressions so if a variable is not in the scope then it cannot be accessed or referenced.

 ### Can you explain the difference between global scope and local scope?
 - The global scope is the outtermost scope which is accessible to every inner or local scope .The local scope variables however ,cannot be accessed by anything in the outter scope.


 ### How does JavaScript handle scope in functions compared to block-level scope?
 -For the functions scope, it encompasses the whole function and does not have access to the block level scope.The block level scope is created by statements like the if, else and for statements. It has access to the functions scope.

 ## How does var, const and let differ in terms of scope
    -global/outer scope are variables are available from all other scopes within your code whether its inside functions, conditional statements,loops or other blocks. the variables are declared using 'var'
    -variables created with the keywords are usually globally available regardless of where they are declared.
    -variables declared inside a function scope can be referenced to inside that function.
    if a variable is not declared inside of a function or a block it is considered to be in the global scope.
    -in the block scope variables declared with "var" are not block scoped. as long as variables are declared with const and let in the block scope, whatever happens in the block stays in the block as in they cannot be referenced outside the block.
    -variables declared with var has only global and function scope.
    -block scope is technically a block of code
    const and let are used in the function and block scope. once you use var it becomes a globalscope
    - in the function scope and block scope, if you invoke it outside the curly braces it gives you an error on th console because the variables declared to the function can only be accessed in its local scope
 
 ### What are the implications of declaring a variable without any keyword (i.e., no var, let, or const)?
   variables declared without key words in a scope are automatically created in a global scope which will later affect your code when running a function.

### What is the scope chain, and how does JavaScript use it to resolve variable access?
    -a scope chain means that a variable can be accessed by other scopes. As in the variable in a function can be referenced in a block scope and other scopes.
    -the most important thing in the scope chain is where the function is declared, not where it is invoked.
    -all variables and functions declared in the outer scope are available in inner scopes via the scope chain.
    As in even for functions nested inside functions can access the variable in the outer/global scope.
    -in a nested scope, the inner function can access the variable in an outer function (to infinity).

### What are some differences between lexical scope and dynamic scope? Which one does JavaScript use?
    lexical scope, is the ability of an inner function to access variables and functions defined in the outer or parent function but not the other way round. Lexical scope is also referred to as static scope and is determined by the code at the time it was written. The lexical scope of a variable is fixed by  its location in the source code and remains unchanged during runtime, it is also about where a variable is declared in the code.

    Dynamic scope looks at how a code is executed and not how it is written. It is more flexible in nature and variables can be acessed from anywhere. Java script uses Lexical scope.

### What is a closure, and how does it relate to scope in JavaScript?
    A closure is a feature in JavaScript where an inner function has access to the outer (enclosing) function's variables—even after the outer function has finished executing. This concept is closely related to lexical scope, as closures "close over" the variables from their lexical environment.
    Closures are fundamentally about scope. They capture the lexical scope, meaning the function remembers the environment in which it was created. This allows the inner function to access variables from its containing (outer) function, adhering to the rules of lexical scoping.