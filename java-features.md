## This page is used to get knowledge on new java features. 

---
Language: Java
Version: 9
---

**1. Factory methods in collections**

* Many a times, you want to create a collection (e.g., a List or Set) in your Java program and fill it with some elements.    

```
List immutableList = List.of(); - EmptyList
List immutableList = List.of("one", "two", "three");
```
**2.JShell: the interactive Java REP**

    Oracle Corp. has introduced a new tool called “jshell”. It stands for Java Shell and also known as REPL (Read Evaluate Print Loop). 
		Many languages already feature an interactive Read-Eval-Print-Loop, and Java now joins this club. 
		It is used to execute and test any Java Constructs like class, interface, enum, object, statements etc. very easily. 
		You can launch jshell from the console and directly start typing and executing Java code. 
		The immediate feedback of jshell makes it a great tool to explore APIs and try out language features.

**Commands:**
* EDIT : Edits the class in JShell edit pad
```
Syntax : edit <class>
```
* list -all : List all the source codes.
```
		Syntax : /l <ClassName>
			* View the class file.
```
Exit: Exit from jShell.
```
Syntax : /exit
```

**3. Stream API Improvements.**
		 Four new methods added to the Stream interface: dropWhile, takeWhile, ofNullable.

**4. Private methods and private-static methods in interface**
* Since java 8, default method was introduced. 
* When default method grows, it won't be readable and we can't add a private method to breakdown.

```
public interface Card{
			private Long createCardID(){
				// Method implementation goes here.
			}
			private static void displayCardDetails(){
				// Method implementation goes here.
			}
			}
```
**5.Convenient way to read the file and print**
```new FileInputStream("C:\\Users\\vijaykumar.s\Documents\\Personal\\TechnicalLinks.txt").transferTo(System.out);
```
---
Language: Java
Version: 12
---
**1. Switch expression**
* Simple, clear and flexible.
```
String s = "v";
switch(s) {
case "v" -> System.out.println("Vijaykumar");
default -> System.out.println("Default");
}
```
* with multiple cases:
```
switch(s) {
case "v,vi" -> System.out.println("Vijaykumar");
default -> System.out.println("Default");
}
```
