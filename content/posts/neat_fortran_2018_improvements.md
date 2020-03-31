---
layout: post
title: Neat new features of Fortran 2018
tags: fortran
---


## Assumed Rank Arrays
```fortran
real(real64) function f(x)
  real(real64), intent(in) :: x(..)
  
  select rank (x)
  rank (*)
    error stop "Function not defined on assumed-size arrays"
  rank (0)
    f = abs(x)
  rank (1)
    f = sum(abs(x))
  rank (2)
    f = sqrt(sum(x**2))
  rank (3)
    f = sum(abs(x)**3)**(1/3.0d0)
  rank (4)
    f = sum(x**4)**(0.25d0)
  rank default
    error stop "Function not supported for rank>4 (unstable)"
end function
```