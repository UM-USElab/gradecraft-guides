Ruby Style Guide
================

A style guide for writing Ruby for [GradeCraft](http://gradecraft.com).

## Table of Contents

1. [Whitespace](#whitespace)
   1. [Indentation](#indentation)
   1. [Inline](#inline)
1. [Commenting](#commenting)
   1. [Class-level comments](#class-level-comments)
   1. [Method comments](#method-comments)
   1. [Inline comments](#inline-comments)
1. [Naming](#naming)
1. [File structure](#file-structure)
   1. Line length
1. [Conditional expressions](#conditional-expressions)
1. [Loops](#loops)
1. [Methods](#methods)
1. [Classes](#classes)
1. [Collections](#collections)
1. [Exceptions](#exceptions)
1. [Strings](#string)
1. [Symbols](#symbols)
1. [Regular Expressions](#regular-expressions)

## Whitespace

### Indentation

* **Use soft-tabs with a two space-indent** Hard tabs require you to know the tab size in advance and different text editors in different operating systems treat tabs differently. This can result in the code alignment being different for different people on the team, thus reducing code readability.

* **Indent `when` as deep as `case`**

```
case
when grade.passing?
  puts "You rock!"
when grade.failing?
  puts "Try harder!"
else
  puts "You don't yet have a grade"
end
```

* **Align method parameters on same line or one per line**

```
# good
def a_lot_of_parameters(parameter_1,
                        parameter_2,
                        parameter_3,
                        parameter_4,
                        last_parameter)
end

# good
def some_parameters(parameter_1, parameter_2, last_parameter)
end

# bad
def several_parameters(parameter_1, parameter_2, parameter_3, parameter_4,
                       parameter_5, last_parameter)
end
```

* **Indent succeeding boolean expressions on multiple lines**

```
# good
def eligible?
  is_cool? && something_has_happened? &&
    this == that
end

# bad
def eligible?
  is_cool? && something_has_happened? &&
  this == that
end
```

### Inline

* **Never leave a trailing whitespace** Trailing whitespace can affect development in a few ways. For one, when you want to go to an end of a line in a text editor, you expect it be on the last character, not a space. For two, extra space at the end of the line cause havoc when concatinating spans multiple lines.

* **Use space around operators**

```
1 + 2
a = b
c == d
exp =~ /^*/
```

* **Use space around colons and after semicolons**

```
first_grade > second_grade ? puts "You did worse" : puts "You did better!"
def initialize; end
```

* **Use spaces around `{` and `}`**

```
students.map { |student| student.passing? }
```

* **No spaces after `(` or `[` nor before `)` nor `]`**

```
courses(student).length
[charlie, rose].length
```

## Commenting

The best code is self-documenting. This can be achieved through sensible [naming](#naming). However, code comments can be helpful when describing the reason behind a decision. Comments that describe what the code is doing is a red flag that should lead to refactoring the code to make it self-documenting.

* **Avoid organizational comments** These tend to get out of whack and it's more important to put methods in alphabetical order for finding the code easier.

```
# bad
class Course
  # Validations

  # Query
end
```

### Class-level comments

Every class definition should have an accompanying comment that describes what it is for and how it should be used. This helps create [readme-driven development](http://tom.preston-werner.com/2010/08/23/readme-driven-development.html) and create focused, single-responsibility classes.

```
# Identifies a series of assignments and grades for a specific subject for a collection of students.
class Course
  # ...
end
```

### Method comments

Every function declaration should have comments immediately preceding it that describe what the function does and how to use it. The comment describes the function, it does not tell the function what to do. In general, these comments do not describe how the function performs its task.

```
# Returns a boolean to indicate if the student is passing the course based on the current criteria.
def passing?
  # ...
end
```

### Inline comments

Inline comments should be used sparingly. It should not describe what the code does. If you feel this is neeed, refactor the code so that it is self-documenting. It can describe the reason behind what the code does. If you feel you will need to explain why in a code review, that would make a good inline comment.

```
def copy(options={})
  # save the copy so that the associations can be automatically inserted
  copy.save if self.persisted?
end
```

## Naming

## File structure

## Conditional expressions

## Loops

## Methods

## Classes

## Collections

## Exceptions

## Strings

## Symbols

## Regular expressions
