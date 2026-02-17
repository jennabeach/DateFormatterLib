# DateFormatterLib

## About

- **Library Name:** DateFormatterLib  
- **Version:** 1.0.0  
- **Author:** Jenna Beach
- **Published Date:** 17/02/2026
- **Description:** A simple Java library for formatting, converting, and validating date strings.  
- **Java Version:** 8+  

## Overview
DateFormatterLib is a simple Java library that provides reusable methods for formatting, converting, and validating date strings.  
It is designed to make working with different date formats easier and more consistent in Java applications.

---

## Features
- Convert dates from one format to another  
- Display dates in a long, human-readable format  
- Validate date strings against a given pattern  
- Retrieve today's date in a specified format  

---

## Requirements
- Java 8 or higher  
- No external dependencies  

---

## Installation

### Add the JAR to your project
1. Download `DateFormatterLib.jar`.
2. In IntelliJ:
   - Go to **File → Project Structure → Libraries**
   - Click **+ → Java**
   - Select the JAR file
3. Click **OK** to add it to your project.

---

## Using DateFormatterLib in Other IDEs or Command Line

DateFormatterLib is a standard Java JAR, so it can be used in any IDE or with the command line.

### Eclipse / NetBeans
- Add the JAR to your project's libraries.
- Import classes as usual.

### Command Line
- Compile with `javac -cp DateFormatterLib.jar MyApp.java`
- Run with `java -cp .:DateFormatterLib.jar MyApp`
  - On Windows, replace `:` with `;` in the classpath.
 
> Note: The JAR includes an optional TestApp class for demonstration purposes.  
> You can run it directly with `java -jar DateFormatterLib.jar` to see example output

---

## Usage

### Import the library
```java
import com.jennabeach.dateformatter.DateFormatter;
```

---

## Testing

### Convert a date format
```java
String result = DateFormatter.convertFormat("17/02/2026", "dd/MM/yyyy", "yyyy-MM-dd");
System.out.println(result);
```
Output: 2026-02-17

### Convert to long date format
```java
String longDate = DateFormatter.toLongDate("2026-02-17");
System.out.println(longDate);
```
Output: February 17, 2026

### Validate a date
```java
boolean valid = DateFormatter.isValidDate("2026-02-17", "yyyy-MM-dd");
System.out.println(valid);
```
Output: true

### Get today's date
```java
String today = DateFormatter.getToday("dd/MM/yyyy");
System.out.println(today);
```
Expected Output: N/A

---

## API Reference
### convertFormat(String date, String inputFormat, String outputFormat)
Converts a date string from one format to another.

### toLongDate(String date)
Converts a date from yyyy-MM-dd format to a long readable format (for example, "February 17, 2026").

### isValidDate(String date, String format)
Checks whether a date string matches a specified format.

### getToday(String format)
Returns today's date formatted using the given pattern.

---

## Date Format Pattern Examples
- yyyy → Year
- MM → Month number
- dd → Day of month
  
---

## License
This project is provided for educational purposes only for the course 26W-CST8411-Information Systems Development and Deployment at Algonquin College, Ottawa, ON CANADA
