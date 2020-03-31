---
layout: post
title: Fortran Unit Testing with PFUnit
tags: fortran testing tdd
category: Testing
---

Under `tests/unit_tests/` the conents of the `CMakeLists.txt` file:


```cmake
add_pfunit_ctest(test_geo_functions
                 TEST_SOURCES
                 test_geo_functions.pf
                 LINK_LIBRARIES
                 iris
                 )
```


Testing Fortran Software with pFUnit (2019-04-10) [[Slides]](https://ideas-productivity.org/wordpress/wp-content/uploads/2019/04/webinar028-pfunit.pdf)

[https://ideas-productivity.org/events/hpc-best-practices-webinars/](https://ideas-productivity.org/events/hpc-best-practices-webinars/)

