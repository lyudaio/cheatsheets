# Perl Cheatsheet

## Basic Syntax

Perl is a high-level programming language, with a syntax that is highly readable and often reminiscent of shell scripts or sed and awk programs. Here are some basic syntax rules to follow:

```perl
# This is a comment
print "Hello, World!\n"; # This is a print statement

$num = 42; # This is a variable assignment

# Perl uses the $ symbol to indicate scalar variables

@array = (1, 2, 3); # This is an array assignment

# Perl uses the @ symbol to indicate arrays

%hash = (one => 1, two => 2, three => 3); # This is a hash assignment

# Perl uses the % symbol to indicate hashes

# Perl uses => to separate keys from values in hashes
```

## Variables

Perl variables can hold scalar, array, and hash values. Scalar variables are denoted by the $ symbol, array variables are denoted by the @ symbol, and hash variables are denoted by the % symbol.

```perl
# Scalar variable
$num = 42;

# Array variable
@array = (1, 2, 3);

# Hash variable
%hash = (one => 1, two => 2, three => 3);
```

## Operators

Perl supports a variety of operators, including arithmetic, comparison, and logical operators.

```perl
# Arithmetic operators
$sum = 5 + 10; # Addition
$difference = 20 - 5; # Subtraction
$product = 5 * 10; # Multiplication
$quotient = 20 / 5; # Division

# Comparison operators
if (5 == 10) { # Equal to
  print "5 is equal to 10\n";
}
if (5 != 10) { # Not equal to
  print "5 is not equal to 10\n";
}
if (5 < 10) { # Less than
  print "5 is less than 10\n";
}
if (5 > 10) { # Greater than
  print "5 is greater than 10\n";
}
if (5 <= 10) { # Less than or equal to
  print "5 is less than or equal to 10\n";
}
if (5 >= 10) { # Greater than or equal to
  print "5 is greater than or equal to 10\n";
}

# Logical operators
if ((5 == 5) && (10 == 10)) { # And
  print "Both conditions are true\n";
}
if ((5 == 5) || (10 == 11)) { # Or
  print "At least one condition is true\n";
}
if (! (5 == 5)) { # Not
  print "The condition is not true\n";
}
```

## Loops

Perl supports a variety of looping constructs, including for loops, foreach loops, and while loops.

```perl
# For loop
for ($i = 0; $i < 10; $i++) {
  print "$i\n";
}

# Foreach loop
@array = (1, 2, 3);
foreach $num (@array) {
  print "$num\n";
}

# While loop
$counter = 0;
while ($counter < 10) {
  print "$counter\n";
  $counter++;
}
```

## Hashes

Hashes are similar to arrays, but instead of accessing elements with an index, you access them with a key.

```perl
%hash = ('key1', 'value1', 'key2', 'value2');
print "$hash{'key1'}\n";
```

## Regular Expressions

Perl's regular expressions are very powerful. The following is an example of how to match a pattern in a string.

```perl
if ($string =~ /pattern/) {
  print "Match found!\n";
}
```

## Subroutines

Subroutines are blocks of code that can be called multiple times with different arguments.

```perl
sub say_hello {
  my $name = shift;
  print "Hello, $name!\n";
}

say_hello("John");
```

## Packages

Packages are used to organize your code into namespaces and to allow you to reuse code from other packages.

```perl
package MyPackage;

sub say_hello {
  print "Hello from MyPackage\n";
}

1;

# Use the code from MyPackage
use MyPackage;

MyPackage::say_hello();
```
