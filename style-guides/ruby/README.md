Ruby Style Guide
================

A style guide for writing Ruby for [GradeCraft](http://gradecraft.com).

## Table of Contents

1. [Whitespace](#whitespace)
   1. [Indentation](#indentation)
   1. [Inline](#inline)
1. [Commenting](#commenting)
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
