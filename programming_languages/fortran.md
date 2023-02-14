# Fortran Programming Language

Fortran is a high-level programming language used primarily in scientific and engineering applications. It was first developed in the 1950s and has since evolved through various versions. The current version is Fortran 2018, released in November 2018.

## Hello, World

```fortran
program hello
    print *, "Hello, World!"
end program hello
```

## Variables

```fortran
! Declare a variable
integer :: x
real :: y
character(len=10) :: name

! Assign a value to a variable
x = 10
y = 3.14159
name = "Fortran"
```

## Data Types

```fortran
! Numbers
integer :: i
real :: x
complex :: z

! Characters
character(len=10) :: name

! Arrays
integer, dimension(3) :: a
real, dimension(3,3) :: b
```

## Control Structures

```fortran
! Conditionals
if (x == 0) then
    print *, "x is zero"
elseif (x < 0) then
    print *, "x is negative"
else
    print *, "x is positive"
end if

! Loops
do i = 1, 10
    print *, i
end do

do i = 1, 10, 2
    print *, i
end do

do while (x < 10)
    print *, x
    x = x + 1
end do
```

## Functions

```fortran
function factorial(n)
    integer :: n, factorial
    if (n == 0) then
        factorial = 1
    else
        factorial = n * factorial(n - 1)
    end if
end function factorial

result = factorial(5)
```

## Subroutines

```fortran
subroutine swap(a, b)
    integer :: a, b, temp
    temp = a
    a = b
    b = temp
end subroutine swap

call swap(x, y)
```

## File I/O

```fortran
! Read from a file
open(unit=1, file="input.txt")
read(1, *) x, y
close(1)

! Write to a file
open(unit=2, file="output.txt")
write(2, *) "The result is ", x + y
close(2)
```

## Modules

```fortran
module my_module
    integer :: x
contains
    subroutine my_subroutine(y)
        integer :: y
        x = y + 1
    end subroutine my_subroutine
end module my_module

use my_module
call my_subroutine(10)
print *, x
```

For more information on Fortran programming, please refer to the [Fortran WikiBook](https://en.wikibooks.org/wiki/Fortran).
