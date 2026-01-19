---
title: "JavaScript: Fetch API Example"
language: "javascript"
tags: ["javascript", "api", "async"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "js-example-1"
description: "Simple async function to fetch JSON data from an API"
---

Simple async function to fetch JSON data from an API

```javascript
async function fetchJson(url) {
  const res = await fetch(url);
  if (!res.ok) throw new Error('Request failed');
  return res.json();
}

// Usage
const data = await fetchJson('https://api.example.com/data');
console.log(data);
```

---
title: "JavaScript: Array Methods"
language: "javascript"
tags: ["javascript", "arrays", "functional"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "js-example-2"
description: "Common array manipulation methods"
---

Common array manipulation methods

```javascript
const numbers = [1, 2, 3, 4, 5];

// Map: transform each element
const doubled = numbers.map(n => n * 2);

// Filter: keep only matching elements
const evens = numbers.filter(n => n % 2 === 0);

// Reduce: accumulate values
const sum = numbers.reduce((acc, n) => acc + n, 0);
```

---
title: "JavaScript: Promise Chain"
language: "javascript"
tags: ["javascript", "promises", "async"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "js-example-3"
description: "Promise chaining with error handling"
---

Promise chaining with error handling

```javascript
fetch('/api/data')
  .then(response => response.json())
  .then(data => {
    console.log('Success:', data);
    return processData(data);
  })
  .catch(error => {
    console.error('Error:', error);
  });
```

---
title: "TypeScript: Interface Definition"
language: "typescript"
tags: ["typescript", "types", "interface"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "ts-example-1"
description: "TypeScript interface with optional properties"
---

TypeScript interface with optional properties

```typescript
interface User {
  id: number;
  name: string;
  email: string;
  age?: number;
  isActive: boolean;
}

function createUser(user: User): User {
  return {
    ...user,
    isActive: user.isActive ?? true
  };
}
```

---
title: "TypeScript: Generic Function"
language: "typescript"
tags: ["typescript", "generics", "functions"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "ts-example-2"
description: "Generic function with type constraints"
---

Generic function with type constraints

```typescript
function getProperty<T, K extends keyof T>(obj: T, key: K): T[K] {
  return obj[key];
}

const user = { name: 'John', age: 30 };
const name = getProperty(user, 'name'); // Type: string
```

---
title: "TypeScript: Class with Generics"
language: "typescript"
tags: ["typescript", "class", "generics"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "ts-example-3"
description: "Generic class implementation"
---

Generic class implementation

```typescript
class Repository<T> {
  private items: T[] = [];

  add(item: T): void {
    this.items.push(item);
  }

  findById(id: number): T | undefined {
    return this.items.find((item: any) => item.id === id);
  }
}
```

---
title: "Python: List Comprehension"
language: "python"
tags: ["python", "lists", "comprehension"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "py-example-1"
description: "Python list comprehension examples"
---

Python list comprehension examples

```python
# Square numbers
squares = [x**2 for x in range(10)]

# Filter even numbers
evens = [x for x in range(20) if x % 2 == 0]

# Nested comprehension
matrix = [[i*j for j in range(3)] for i in range(3)]
```

---
title: "Python: Dictionary Operations"
language: "python"
tags: ["python", "dictionaries", "data-structures"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "py-example-2"
description: "Common dictionary operations in Python"
---

Common dictionary operations in Python

```python
# Create dictionary
user = {'name': 'Alice', 'age': 30, 'city': 'NYC'}

# Access with default
age = user.get('age', 0)

# Dictionary comprehension
squared = {k: v**2 for k, v in user.items() if isinstance(v, int)}
```

---
title: "Python: Decorator Pattern"
language: "python"
tags: ["python", "decorators", "functions"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "py-example-3"
description: "Function decorator example"
---

Function decorator example

```python
def timing_decorator(func):
    def wrapper(*args, **kwargs):
        import time
        start = time.time()
        result = func(*args, **kwargs)
        print(f"{func.__name__} took {time.time() - start:.2f}s")
        return result
    return wrapper

@timing_decorator
def slow_function():
    time.sleep(1)
```

---
title: "Java: Class Definition"
language: "java"
tags: ["java", "class", "oop"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "java-example-1"
description: "Basic Java class with constructor and methods"
---

Basic Java class with constructor and methods

```java
public class User {
    private String name;
    private int age;

    public User(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }
}
```

---
title: "Java: Stream API"
language: "java"
tags: ["java", "streams", "functional"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "java-example-2"
description: "Java Stream API operations"
---

Java Stream API operations

```java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);

// Filter and map
List<Integer> doubled = numbers.stream()
    .filter(n -> n % 2 == 0)
    .map(n -> n * 2)
    .collect(Collectors.toList());

// Sum
int sum = numbers.stream()
    .reduce(0, Integer::sum);
```

---
title: "Java: Exception Handling"
language: "java"
tags: ["java", "exceptions", "error-handling"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "java-example-3"
description: "Try-catch-finally block example"
---

Try-catch-finally block example

```java
try {
    FileReader file = new FileReader("data.txt");
    BufferedReader reader = new BufferedReader(file);
    String line = reader.readLine();
} catch (FileNotFoundException e) {
    System.err.println("File not found: " + e.getMessage());
} catch (IOException e) {
    System.err.println("IO error: " + e.getMessage());
} finally {
    if (reader != null) {
        reader.close();
    }
}
```

---
title: "Go: Function Definition"
language: "go"
tags: ["go", "functions", "golang"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "go-example-1"
description: "Go function with multiple return values"
---

Go function with multiple return values

```go
package main

import "fmt"

func divide(a, b float64) (float64, error) {
    if b == 0 {
        return 0, fmt.Errorf("division by zero")
    }
    return a / b, nil
}

func main() {
    result, err := divide(10, 2)
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Println("Result:", result)
    }
}
```

---
title: "Go: Goroutines"
language: "go"
tags: ["go", "goroutines", "concurrency"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "go-example-2"
description: "Concurrent execution with goroutines"
---

Concurrent execution with goroutines

```go
package main

import (
    "fmt"
    "time"
)

func printNumbers() {
    for i := 1; i <= 5; i++ {
        fmt.Println(i)
        time.Sleep(100 * time.Millisecond)
    }
}

func main() {
    go printNumbers()
    go printNumbers()
    time.Sleep(1 * time.Second)
}
```

---
title: "Go: Struct and Methods"
language: "go"
tags: ["go", "structs", "methods"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "go-example-3"
description: "Go struct with receiver methods"
---

Go struct with receiver methods

```go
type Rectangle struct {
    Width  float64
    Height float64
}

func (r Rectangle) Area() float64 {
    return r.Width * r.Height
}

func (r *Rectangle) Scale(factor float64) {
    r.Width *= factor
    r.Height *= factor
}
```

---
title: "Rust: Ownership Example"
language: "rust"
tags: ["rust", "ownership", "memory"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "rust-example-1"
description: "Rust ownership and borrowing"
---

Rust ownership and borrowing

```rust
fn main() {
    let s1 = String::from("hello");
    let s2 = s1; // s1 is moved to s2
    
    // println!("{}", s1); // Error: s1 no longer valid
    
    let s3 = s2.clone(); // Clone the data
    println!("{}", s3);
    
    let len = calculate_length(&s3); // Borrow reference
    println!("Length: {}", len);
}

fn calculate_length(s: &String) -> usize {
    s.len()
}
```

---
title: "Rust: Error Handling"
language: "rust"
tags: ["rust", "errors", "result"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "rust-example-2"
description: "Result type for error handling"
---

Result type for error handling

```rust
use std::fs::File;
use std::io::Error;

fn read_file(filename: &str) -> Result<String, Error> {
    match std::fs::read_to_string(filename) {
        Ok(content) => Ok(content),
        Err(e) => Err(e),
    }
}

fn main() {
    match read_file("data.txt") {
        Ok(content) => println!("File content: {}", content),
        Err(e) => println!("Error: {}", e),
    }
}
```

---
title: "Rust: Pattern Matching"
language: "rust"
tags: ["rust", "match", "pattern-matching"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "rust-example-3"
description: "Match expression with Option type"
---

Match expression with Option type

```rust
fn find_user(id: u32) -> Option<String> {
    if id == 1 {
        Some("Alice".to_string())
    } else {
        None
    }
}

fn main() {
    match find_user(1) {
        Some(name) => println!("Found user: {}", name),
        None => println!("User not found"),
    }
}
```

---
title: "C++: Class Template"
language: "cpp"
tags: ["cpp", "templates", "class"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "cpp-example-1"
description: "C++ template class example"
---

C++ template class example

```cpp
#include <iostream>
#include <vector>

template<typename T>
class Stack {
private:
    std::vector<T> elements;

public:
    void push(T const& elem) {
        elements.push_back(elem);
    }
    
    T pop() {
        T elem = elements.back();
        elements.pop_back();
        return elem;
    }
    
    bool empty() const {
        return elements.empty();
    }
};
```

---
title: "C++: Smart Pointers"
language: "cpp"
tags: ["cpp", "pointers", "memory"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "cpp-example-2"
description: "Using unique_ptr for memory management"
---

Using unique_ptr for memory management

```cpp
#include <memory>
#include <iostream>

class MyClass {
public:
    MyClass() { std::cout << "Constructor\n"; }
    ~MyClass() { std::cout << "Destructor\n"; }
    void doSomething() { std::cout << "Doing something\n"; }
};

int main() {
    std::unique_ptr<MyClass> ptr = std::make_unique<MyClass>();
    ptr->doSomething();
    // Automatically deleted when ptr goes out of scope
    return 0;
}
```

---
title: "C++: STL Algorithms"
language: "cpp"
tags: ["cpp", "stl", "algorithms"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "cpp-example-3"
description: "STL algorithm examples"
---

STL algorithm examples

```cpp
#include <algorithm>
#include <vector>
#include <iostream>

int main() {
    std::vector<int> vec = {3, 1, 4, 1, 5, 9, 2, 6};
    
    // Sort
    std::sort(vec.begin(), vec.end());
    
    // Find
    auto it = std::find(vec.begin(), vec.end(), 5);
    
    // Count
    int count = std::count(vec.begin(), vec.end(), 1);
    
    return 0;
}
```

---
title: "C: Pointer Operations"
language: "c"
tags: ["c", "pointers", "memory"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "c-example-1"
description: "C pointer arithmetic and dereferencing"
---

C pointer arithmetic and dereferencing

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int arr[] = {10, 20, 30, 40, 50};
    int *ptr = arr;
    
    printf("First element: %d\n", *ptr);
    printf("Second element: %d\n", *(ptr + 1));
    
    // Iterate through array
    for (int i = 0; i < 5; i++) {
        printf("arr[%d] = %d\n", i, *(ptr + i));
    }
    
    return 0;
}
```

---
title: "C: Dynamic Memory"
language: "c"
tags: ["c", "malloc", "memory"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "c-example-2"
description: "Dynamic memory allocation with malloc"
---

Dynamic memory allocation with malloc

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n = 5;
    int *arr = (int*)malloc(n * sizeof(int));
    
    if (arr == NULL) {
        printf("Memory allocation failed\n");
        return 1;
    }
    
    for (int i = 0; i < n; i++) {
        arr[i] = i * 10;
    }
    
    free(arr); // Always free allocated memory
    return 0;
}
```

---
title: "C: Struct Usage"
language: "c"
tags: ["c", "structs", "data-structures"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "c-example-3"
description: "C struct definition and usage"
---

C struct definition and usage

```c
#include <stdio.h>
#include <string.h>

struct Person {
    char name[50];
    int age;
    float height;
};

int main() {
    struct Person p1;
    strcpy(p1.name, "John");
    p1.age = 30;
    p1.height = 5.9;
    
    printf("Name: %s, Age: %d, Height: %.1f\n", 
           p1.name, p1.age, p1.height);
    
    return 0;
}
```

---
title: "C#: LINQ Query"
language: "csharp"
tags: ["csharp", "linq", "queries"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "csharp-example-1"
description: "LINQ query expressions in C#"
---

LINQ query expressions in C#

```csharp
using System;
using System.Linq;

class Program {
    static void Main() {
        int[] numbers = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
        
        var evens = from n in numbers
                   where n % 2 == 0
                   select n;
        
        foreach (var num in evens) {
            Console.WriteLine(num);
        }
    }
}
```

---
title: "C#: Async/Await"
language: "csharp"
tags: ["csharp", "async", "await"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "csharp-example-2"
description: "Asynchronous programming with async/await"
---

Asynchronous programming with async/await

```csharp
using System;
using System.Net.Http;
using System.Threading.Tasks;

class Program {
    static async Task Main() {
        using (var client = new HttpClient()) {
            string result = await client.GetStringAsync("https://api.example.com/data");
            Console.WriteLine(result);
        }
    }
    
    static async Task<string> FetchDataAsync() {
        await Task.Delay(1000);
        return "Data fetched";
    }
}
```

---
title: "C#: Properties and Auto-Properties"
language: "csharp"
tags: ["csharp", "properties", "classes"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "csharp-example-3"
description: "C# property syntax examples"
---

C# property syntax examples

```csharp
public class User {
    // Auto-property
    public string Name { get; set; }
    
    // Property with backing field
    private int _age;
    public int Age {
        get { return _age; }
        set { _age = value > 0 ? value : 0; }
    }
    
    // Read-only property
    public string FullName => $"{FirstName} {LastName}";
}
```

---
title: "PHP: Array Functions"
language: "php"
tags: ["php", "arrays", "functions"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "php-example-1"
description: "PHP array manipulation functions"
---

PHP array manipulation functions

```php
<?php
$numbers = [1, 2, 3, 4, 5];

// Map
$doubled = array_map(function($n) {
    return $n * 2;
}, $numbers);

// Filter
$evens = array_filter($numbers, function($n) {
    return $n % 2 == 0;
});

// Reduce
$sum = array_reduce($numbers, function($carry, $n) {
    return $carry + $n;
}, 0);
?>
```

---
title: "PHP: Class and Object"
language: "php"
tags: ["php", "class", "oop"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "php-example-2"
description: "PHP class definition with constructor"
---

PHP class definition with constructor

```php
<?php
class User {
    private $name;
    private $email;
    
    public function __construct($name, $email) {
        $this->name = $name;
        $this->email = $email;
    }
    
    public function getName() {
        return $this->name;
    }
    
    public function getEmail() {
        return $this->email;
    }
}

$user = new User("John", "john@example.com");
echo $user->getName();
?>
```

---
title: "PHP: PDO Database"
language: "php"
tags: ["php", "pdo", "database"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "php-example-3"
description: "PDO database connection and query"
---

PDO database connection and query

```php
<?php
try {
    $pdo = new PDO("mysql:host=localhost;dbname=mydb", $user, $pass);
    $pdo->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    
    $stmt = $pdo->prepare("SELECT * FROM users WHERE id = :id");
    $stmt->execute(['id' => 1]);
    $user = $stmt->fetch(PDO::FETCH_ASSOC);
    
} catch(PDOException $e) {
    echo "Error: " . $e->getMessage();
}
?>
```

---
title: "Ruby: Block Syntax"
language: "ruby"
tags: ["ruby", "blocks", "iterators"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "ruby-example-1"
description: "Ruby blocks and iterators"
---

Ruby blocks and iterators

```ruby
# Each iterator
[1, 2, 3, 4, 5].each do |n|
  puts n * 2
end

# Map
doubled = [1, 2, 3].map { |n| n * 2 }

# Select
evens = [1, 2, 3, 4, 5].select { |n| n.even? }

# Reduce
sum = [1, 2, 3, 4, 5].reduce(0) { |acc, n| acc + n }
```

---
title: "Ruby: Class Definition"
language: "ruby"
tags: ["ruby", "class", "ruby"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "ruby-example-2"
description: "Ruby class with attr_accessor"
---

Ruby class with attr_accessor

```ruby
class User
  attr_accessor :name, :email
  
  def initialize(name, email)
    @name = name
    @email = email
  end
  
  def to_s
    "#{@name} <#{@email}>"
  end
end

user = User.new("Alice", "alice@example.com")
puts user
```

---
title: "Ruby: Hash Operations"
language: "ruby"
tags: ["ruby", "hash", "data-structures"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "ruby-example-3"
description: "Ruby hash manipulation"
---

Ruby hash manipulation

```ruby
# Create hash
user = { name: "John", age: 30, city: "NYC" }

# Access
name = user[:name]

# Add key
user[:email] = "john@example.com"

# Iterate
user.each do |key, value|
  puts "#{key}: #{value}"
end

# Symbol keys
config = { host: "localhost", port: 3000 }
```

---
title: "Swift: Optionals"
language: "swift"
tags: ["swift", "optionals", "ios"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "swift-example-1"
description: "Swift optional unwrapping"
---

Swift optional unwrapping

```swift
var name: String? = "John"

// Optional binding
if let unwrappedName = name {
    print("Name is \(unwrappedName)")
}

// Guard statement
func greet(name: String?) {
    guard let name = name else {
        print("No name provided")
        return
    }
    print("Hello, \(name)")
}

// Nil coalescing
let displayName = name ?? "Anonymous"
```

---
title: "Swift: Struct and Protocol"
language: "swift"
tags: ["swift", "struct", "protocol"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "swift-example-2"
description: "Swift struct conforming to protocol"
---

Swift struct conforming to protocol

```swift
protocol Drawable {
    func draw()
}

struct Circle: Drawable {
    var radius: Double
    
    func draw() {
        print("Drawing circle with radius \(radius)")
    }
}

let circle = Circle(radius: 5.0)
circle.draw()
```

---
title: "Swift: Closures"
language: "swift"
tags: ["swift", "closures", "functional"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "swift-example-3"
description: "Swift closure syntax"
---

Swift closure syntax

```swift
let numbers = [1, 2, 3, 4, 5]

// Map with closure
let doubled = numbers.map { $0 * 2 }

// Filter
let evens = numbers.filter { $0 % 2 == 0 }

// Sort
let sorted = numbers.sorted { $0 > $1 }

// Trailing closure
numbers.forEach { print($0) }
```

---
title: "Kotlin: Data Class"
language: "kotlin"
tags: ["kotlin", "data-class", "android"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "kotlin-example-1"
description: "Kotlin data class with properties"
---

Kotlin data class with properties

```kotlin
data class User(
    val id: Int,
    val name: String,
    val email: String
)

fun main() {
    val user = User(1, "Alice", "alice@example.com")
    println(user) // Automatically generated toString()
    
    val (id, name, email) = user // Destructuring
}
```

---
title: "Kotlin: Extension Functions"
language: "kotlin"
tags: ["kotlin", "extensions", "functions"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "kotlin-example-2"
description: "Kotlin extension function example"
---

Kotlin extension function example

```kotlin
// Extension function
fun String.removeSpaces(): String {
    return this.replace(" ", "")
}

fun main() {
    val text = "Hello World"
    println(text.removeSpaces()) // "HelloWorld"
}

// Extension property
val String.firstChar: Char
    get() = this[0]
```

---
title: "Kotlin: When Expression"
language: "kotlin"
tags: ["kotlin", "when", "control-flow"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "kotlin-example-3"
description: "Kotlin when expression (switch replacement)"
---

Kotlin when expression (switch replacement)

```kotlin
fun describe(obj: Any): String = when (obj) {
    1 -> "One"
    "Hello" -> "Greeting"
    is Long -> "Long type"
    !is String -> "Not a string"
    else -> "Unknown"
}

fun main() {
    println(describe(1))
    println(describe("Hello"))
    println(describe(100L))
}
```

---
title: "HTML: Basic Structure"
language: "html"
tags: ["html", "structure", "web"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "html-example-1"
description: "Basic HTML5 document structure"
---

Basic HTML5 document structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Page</title>
</head>
<body>
    <header>
        <h1>Welcome</h1>
    </header>
    <main>
        <p>This is the main content.</p>
    </main>
    <footer>
        <p>&copy; 2025</p>
    </footer>
</body>
</html>
```

---
title: "HTML: Form Elements"
language: "html"
tags: ["html", "forms", "input"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "html-example-2"
description: "HTML form with various input types"
---

HTML form with various input types

```html
<form action="/submit" method="POST">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    
    <label for="age">Age:</label>
    <input type="number" id="age" name="age" min="18" max="100">
    
    <label for="country">Country:</label>
    <select id="country" name="country">
        <option value="us">United States</option>
        <option value="uk">United Kingdom</option>
    </select>
    
    <button type="submit">Submit</button>
</form>
```

---
title: "HTML: Semantic Elements"
language: "html"
tags: ["html", "semantic", "html5"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "html-example-3"
description: "HTML5 semantic elements"
---

HTML5 semantic elements

```html
<article>
    <header>
        <h2>Article Title</h2>
        <time datetime="2025-01-15">January 15, 2025</time>
    </header>
    <section>
        <p>Article content goes here.</p>
    </section>
    <aside>
        <p>Related information</p>
    </aside>
    <footer>
        <p>Author: John Doe</p>
    </footer>
</article>
```

---
title: "CSS: Flexbox Layout"
language: "css"
tags: ["css", "flexbox", "layout"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "css-example-1"
description: "CSS Flexbox for responsive layout"
---

CSS Flexbox for responsive layout

```css
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
}

.item {
    flex: 1;
    padding: 20px;
    background-color: #f0f0f0;
}

.item:first-child {
    flex: 2; /* Takes twice the space */
}
```

---
title: "CSS: Grid Layout"
language: "css"
tags: ["css", "grid", "layout"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "css-example-2"
description: "CSS Grid layout example"
---

CSS Grid layout example

```css
.grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: auto;
    gap: 20px;
}

.grid-item {
    background-color: #e0e0e0;
    padding: 20px;
}

.grid-item:nth-child(1) {
    grid-column: span 2;
}
```

---
title: "CSS: Animations"
language: "css"
tags: ["css", "animations", "keyframes"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "css-example-3"
description: "CSS keyframe animations"
---

CSS keyframe animations

```css
@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.element {
    animation: fadeIn 0.5s ease-in-out;
}

.element:hover {
    animation: fadeIn 0.3s ease-in-out;
}
```

---
title: "SQL: SELECT Queries"
language: "sql"
tags: ["sql", "select", "queries"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "sql-example-1"
description: "Basic SQL SELECT with WHERE and JOIN"
---

Basic SQL SELECT with WHERE and JOIN

```sql
SELECT u.id, u.name, u.email, p.title
FROM users u
INNER JOIN posts p ON u.id = p.user_id
WHERE u.active = 1
ORDER BY u.name ASC
LIMIT 10;
```

---
title: "SQL: INSERT and UPDATE"
language: "sql"
tags: ["sql", "insert", "update"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "sql-example-2"
description: "SQL INSERT and UPDATE statements"
---

SQL INSERT and UPDATE statements

```sql
-- Insert single row
INSERT INTO users (name, email, created_at)
VALUES ('John Doe', 'john@example.com', NOW());

-- Insert multiple rows
INSERT INTO users (name, email) VALUES
    ('Alice', 'alice@example.com'),
    ('Bob', 'bob@example.com');

-- Update
UPDATE users
SET email = 'newemail@example.com', updated_at = NOW()
WHERE id = 1;
```

---
title: "SQL: Aggregate Functions"
language: "sql"
tags: ["sql", "aggregate", "group-by"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "sql-example-3"
description: "SQL aggregate functions with GROUP BY"
---

SQL aggregate functions with GROUP BY

```sql
SELECT 
    category,
    COUNT(*) as total,
    AVG(price) as avg_price,
    MAX(price) as max_price,
    MIN(price) as min_price
FROM products
WHERE active = 1
GROUP BY category
HAVING COUNT(*) > 5
ORDER BY total DESC;
```

---
title: "JSON: Object Structure"
language: "json"
tags: ["json", "object", "data"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "json-example-1"
description: "JSON object with nested structures"
---

JSON object with nested structures

```json
{
  "user": {
    "id": 1,
    "name": "John Doe",
    "email": "john@example.com",
    "address": {
      "street": "123 Main St",
      "city": "New York",
      "zip": "10001"
    },
    "tags": ["developer", "admin"]
  }
}
```

---
title: "JSON: Array of Objects"
language: "json"
tags: ["json", "array", "objects"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "json-example-2"
description: "JSON array containing multiple objects"
---

JSON array containing multiple objects

```json
[
  {
    "id": 1,
    "name": "Product A",
    "price": 29.99,
    "inStock": true
  },
  {
    "id": 2,
    "name": "Product B",
    "price": 39.99,
    "inStock": false
  },
  {
    "id": 3,
    "name": "Product C",
    "price": 19.99,
    "inStock": true
  }
]
```

---
title: "JSON: Configuration"
language: "json"
tags: ["json", "config", "settings"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "json-example-3"
description: "JSON configuration file example"
---

JSON configuration file example

```json
{
  "app": {
    "name": "MyApp",
    "version": "1.0.0",
    "debug": false
  },
  "database": {
    "host": "localhost",
    "port": 5432,
    "name": "mydb"
  },
  "features": {
    "enableCache": true,
    "maxConnections": 10
  }
}
```

---
title: "YAML: Basic Structure"
language: "yaml"
tags: ["yaml", "config", "data"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "yaml-example-1"
description: "YAML configuration structure"
---

YAML configuration structure

```yaml
---
app:
  name: MyApp
  version: 1.0.0
  debug: false

database:
  host: localhost
  port: 5432
  name: mydb

features:
  enableCache: true
  maxConnections: 10
```

---
title: "YAML: Lists and Nested"
language: "yaml"
tags: ["yaml", "lists", "nested"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "yaml-example-2"
description: "YAML with lists and nested structures"
---

YAML with lists and nested structures

```yaml
users:
  - name: Alice
    email: alice@example.com
    roles:
      - admin
      - user
  - name: Bob
    email: bob@example.com
    roles:
      - user

settings:
  theme: dark
  languages:
    - en
    - es
    - fr
```

---
title: "YAML: Multi-line Strings"
language: "yaml"
tags: ["yaml", "strings", "multiline"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "yaml-example-3"
description: "YAML multi-line string examples"
---

YAML multi-line string examples

```yaml
description: |
  This is a multi-line string
  that preserves line breaks
  and can span multiple lines.

summary: >
  This is a folded string
  that converts line breaks
  to spaces.

code: |
  function hello() {
    console.log("Hello");
  }
```

---
title: "Markdown: Headers and Lists"
language: "markdown"
tags: ["markdown", "formatting", "text"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "md-example-1"
description: "Markdown headers and list syntax"
---

Markdown headers and list syntax

```markdown
# Heading 1
## Heading 2
### Heading 3

- Unordered list item 1
- Unordered list item 2
  - Nested item

1. Ordered list item 1
2. Ordered list item 2
3. Ordered list item 3
```

---
title: "Markdown: Links and Images"
language: "markdown"
tags: ["markdown", "links", "images"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "md-example-2"
description: "Markdown link and image syntax"
---

Markdown link and image syntax

```markdown
[Link text](https://example.com)

[Link with title](https://example.com "Title")

![Alt text](image.jpg)

![Alt text](image.jpg "Image title")

[Reference link][ref]

[ref]: https://example.com
```

---
title: "Markdown: Code Blocks"
language: "markdown"
tags: ["markdown", "code", "blocks"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "md-example-3"
description: "Markdown code blocks and inline code"
---

Markdown code blocks and inline code

```markdown
Inline code: `const x = 10;`

Code block:
```javascript
function hello() {
  console.log("Hello");
}
```

Fenced code block with language:
```python
def greet(name):
    print(f"Hello, {name}")
```
```

---
title: "Bash: File Operations"
language: "bash"
tags: ["bash", "files", "shell"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "bash-example-1"
description: "Bash file manipulation commands"
---

Bash file manipulation commands

```bash
#!/bin/bash

# Read file line by line
while IFS= read -r line; do
    echo "$line"
done < file.txt

# Find and process files
find . -name "*.txt" -type f -exec grep -l "pattern" {} \;

# Copy with backup
cp file.txt file.txt.bak
```

---
title: "Bash: Conditional Logic"
language: "bash"
tags: ["bash", "conditionals", "logic"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "bash-example-2"
description: "Bash if-else and case statements"
---

Bash if-else and case statements

```bash
#!/bin/bash

if [ -f "$1" ]; then
    echo "File exists"
elif [ -d "$1" ]; then
    echo "Directory exists"
else
    echo "Not found"
fi

case "$1" in
    start)
        echo "Starting..."
        ;;
    stop)
        echo "Stopping..."
        ;;
    *)
        echo "Unknown command"
        ;;
esac
```

---
title: "Bash: Functions and Loops"
language: "bash"
tags: ["bash", "functions", "loops"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "bash-example-3"
description: "Bash function definition and loop examples"
---

Bash function definition and loop examples

```bash
#!/bin/bash

# Function definition
greet() {
    local name=$1
    echo "Hello, $name"
}

# For loop
for i in {1..5}; do
    echo "Iteration $i"
done

# While loop
count=0
while [ $count -lt 5 ]; do
    echo "Count: $count"
    ((count++))
done
```

---
title: "PowerShell: Cmdlets"
language: "powershell"
tags: ["powershell", "cmdlets", "windows"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "ps-example-1"
description: "PowerShell cmdlet examples"
---

PowerShell cmdlet examples

```powershell
# Get processes
Get-Process | Where-Object {$_.CPU -gt 100}

# Read file content
$content = Get-Content "file.txt"

# Write to file
"Hello, World" | Set-Content "output.txt"

# Filter and select
Get-Service | Where-Object {$_.Status -eq "Running"} | Select-Object Name, Status
```

---
title: "PowerShell: Functions"
language: "powershell"
tags: ["powershell", "functions", "scripts"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "ps-example-2"
description: "PowerShell function with parameters"
---

PowerShell function with parameters

```powershell
function Get-UserInfo {
    param(
        [string]$UserName,
        [int]$Age
    )
    
    Write-Host "User: $UserName"
    Write-Host "Age: $Age"
}

Get-UserInfo -UserName "John" -Age 30

# Function with pipeline
function Process-Items {
    process {
        Write-Host "Processing: $_"
    }
}

1..5 | Process-Items
```

---
title: "PowerShell: Arrays and Hashtables"
language: "powershell"
tags: ["powershell", "arrays", "hashtables"]
folder: null
source: null
createdAt: 1704067200000
updatedAt: 1704067200000
id: "ps-example-3"
description: "PowerShell array and hashtable operations"
---

PowerShell array and hashtable operations

```powershell
# Array
$numbers = @(1, 2, 3, 4, 5)
$numbers | ForEach-Object { $_ * 2 }

# Hashtable
$user = @{
    Name = "John"
    Age = 30
    City = "NYC"
}

$user.Name
$user["Age"]

# Iterate hashtable
$user.GetEnumerator() | ForEach-Object {
    Write-Host "$($_.Key): $($_.Value)"
}
```

