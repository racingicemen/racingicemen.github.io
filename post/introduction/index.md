# Introduction

This blog mainly serves as an annotation for my software side projects. A lot of these projects are samples
from various books and articles. Some will be full applications. All projects will have complete code, 
including instructions on installing and running the code. Of course, the source code will be provided on 
[GitHub](https://github.com/racingicemen).

# Testing the Even theme
In the remainder of this post, I will include some rather meaningless snippets to see how the Hugo theme
[Even](https://github.com/olOwOlo/hugo-theme-even) lays out various elements.

## Code samples

### Python
```python
def hello(name):
    print(f'hello {name}')

if __name__ == '__main__':
    hello('racingicemen')
```

### C++
```cpp
#include <iostream>
#include <string>
using namespace std;

void hello(const string& name)
{
    cout << name << endl;
}

int main()
{
    hello("racingicemen");
}
```

## Plant UML diagrams
[PlantUML](http://plantuml.com) is an excellent tool for drawing UML diagrams. Install the PlantUML plugin 
in any of JetBrains' products, and you have a state of the art UML editor. The best thing is there is no 
messing around with the mouse etc. Just write your textual description of the diagram in an extremely 
intuitive DSL, and PlantUML does the rest. For example, the following text

```
@startuml

title a sample PlantUML sequence diagram

skinparam handwritten true
skinparam sequenceArrowThickness 2

actor Alice as A
actor Bob as B
database DB as D

A -> B: Authentication Request
B -> D: Check authentication
D --> B: Success
A <-- B: Authentication Response

@enduml
```

is rendered as

![image](/static/test.png)