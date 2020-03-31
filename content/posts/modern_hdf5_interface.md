---
layout: post
title: Modern Fortran HDF5 Interface
tags: fortran io
category: Development
---


```fortran
use hdf5_interface, only: hdf5_file

implicit none

type(hdf5_file) :: h5f

call h5f%initialize('new_file.h5', status='new', &
                     action='w', comp_lvl=6)
call h5f%add('/title', 'Title of my new file')
call h5f%add('/density', rho)
call h5f%writeattr('/density', 'description', 'Fluid Mass Density')
call h5f%writeattr('/density', 'units', '[g/cc]')

call h5f%finalize()
```