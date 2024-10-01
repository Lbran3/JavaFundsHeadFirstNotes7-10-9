# JavaFundsHeadFirstNotes7-10-9
   /*
    Mod 7
    String Class
    stores sequence of Unicode characters
    enclosed in double quotes
    can be concatenated using + or +=
    hold a reference to the instance of string
    parallel arrays = elements from one array correspondent with same elements in the other array
    Strings are immutable = changes in the value create a new string instance

    String variable
    don't directly store a string instance
    hold a reference to string instance

    String Equality
    compare strings w/the equality operator (==)
    character by character comparison (equals method; .equals)
    prefers the equals method

    String Class Methods
    OPERATIONS:length = METHOD:length
    create new strings from existing = concat, replace, to LowerCase, toUppercase, trim , split
    extract substring = charArt, substring
    test substring = contains, endsWith, startsWith, indexOf, lastIndexOf
    comparison = equals, equalsIgnoreCase, isEmpty, compareTo, compareToIgnoreCase
    formatting = format
    String for non-string = valueOf

    StringBuilder class
    provides mutable string buffer; any modifications made to the string doesn't actually change string and creates a new string
    efficiently constructs string values
    add content within with insert
    extract content to a string using (toString method)

    Ex:
    String location = "Florida";
    int flightNumber = 175;
    StringBuilder sb = new StringBuilder(40);
    sb.append("I flew to ");
    sb.append(location);
    sb.append(" on Flight #");
    sb.append(flightNumber);
    String message = sb.toString(); // "I flew to Florida on Flight #175"

    String time = "9:00";
    int pos = sb.indexOf(" on");
    sb.insert(pos, " at ");
    sb.insert(pos + 4, time);
    message = sb.toString(); // "I flew to Florida at 9:00 on Flight #175"
    -------------------------------------------------------------------------------
    Mod 8
    Java is an object-oriented language
    objects encapsulate data, ops, and usage
    allow storage and manipulation details to be hidden
    separated what is to be done and how it is done
    before having an object you have to declare/create a class first
    body of class is contained within brackets {}
    classes are made up of both state and executable code
    classes variables hold a reference
    instances created with new keyword;
    multiple variables can reference the same instance
    classes = template for creating objects
    object = instance of a class
    fields = store object state
    methods = executable code that manipulates state of the object and performs operations related to the class
    constructors = executable code used during object creation to set objects initial state

    Encapsulation and Access Identifiers
    implementation details of a class are generally hidden is known as ENCAPSULATION
    Access modifiers = used to achieve encapsulation; allows to control visibility of classes and their memmbers

    BASIC ACCESS MODIFIERS
    Access modifiers:
    control class visibility
    control member visibility
    enable encapsulation
    no access modifiers = visibility: only within its own package
    public = visibility: everywhere
    private = visibility: only within declaring class

    Special References Java Provides
    this = reference to current object; allows object to pass itself as a parameter
    null = represents an uncreated object; can be assigned to any reference variable

    Field Encapsulation
    specific fields a class uses  to manage data values; generally considered to be an implementation detail
    use methods to control field access

    Accessors and Mutators
    Accessors = retrieves value if the field; commonly known as a "getter method"; ex: getFieldName
    Mutator = modifies field value; known as a "setter"; ex: setFieldName
    -------------------------------------------------------------------------------------------------------------------
    Mod 9
    3 ways to establish initial state
    field initializers = specify fields initial value as part of the fields declaration(can include: an equation, other
    fields, method calls)
    constructors = code that runs during object session; no return type

     # of constructors
     must have at least one
     can have multiple each with a unique parameter list,
     constructors need to differ in number of parameters and different parameter type
     once you provide one constructor, you have to provide all constructors
     default constructor = a constructor that doesn't accept any arguments

     Chaining constructor = one constructor can call another constructor
     -must be first line of constructor
     -use (this.) keyword followed by the parameter list

     initialization blocks = automatically runs whenever a class instance is created; allow us to have code that get
     shared across all constructors; cannot receive parameters

      initialization and Construction Order
      field initializer ---> initialization ---> constructors
      -----------------------------------------------------------------------------------------------------------------
     Mod 10
     Static Members
     static field = a value not associated w/ a specific instance; all instances access the same value
     static method =perform action not tied to an instance
     can only access static members
     Static import = allows static methods to used w/o being class qualified
     Static initialization blocks = performs one time type initialization
     */
//--------------------------------------------------------------------------------------------------------------------// -
     /*HeadFirstJava
     Stack and Heap
     2 areas of memory
     Heap = where the objects live known as "the garbage collection heap"
     Stack = where the method invocations and local variables live
     JVM = Java Virtual Machine
     2 variables - instance and local variables
     instance variables = declared inside a class but not inside a method; live w/in the obj they belong to, on the Heap
     local variables = declared inside a method, including method parameters; live only w/in the method that declared the variable
     stack frame = holds the state of the method including which line of code is executing, and values of all local
     variables
     call stack =  when you call a method, the method lands on top; the top stack is always the current executing method
     all local variables live on the stack, in the frame corresponding to the method where variable is declared
     all objects live in the heap, regardless of whether the reference is a local or instance variable
     3 steps of object creation = declare a reference variable, create an object, assign the object to the reference
     the only way to invoke a constructor is  with the keyword ;new; followed by the class name
     a constructor must have the same name as the class, and not have a return type
     if you don't put a constructor in your class, the compiler will input a default constructor for you
     if you build the constructor yourself, the compiler will not build a default constructor; it will leave it all to you
     overloaded constructors mean you have more than one in your class
     instance variables are assigned default values, even if you don't assign one;
     default values = 0/0.0/false for primitives and null for references
     the only to call a super constructor is bu calling super()
     calling super() in your constructor puts the superclass constructor on the top of the Stack
     the call super() must be the first statement of each constructor
     every constructor can have a call to super() OR this(), never both
     life = local variable is alive as long as its Stack frame is on the Stack (until the method completes)
     scope = visibility and lifetime of variables, methods and classes with the program
     an object become eligible for garbage collection when its last live reference disappears
     null = "deprogramming the remote control"
     */
