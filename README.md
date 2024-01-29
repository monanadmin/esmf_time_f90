# ESMF_TIME - F90 Version 

Tony Craig, Feb, 2012

This is a partial substitute for the ESMF Time Manager.  As of Feb, 2012,
what exists is consist (in interfaces and datatypes) with ESMF 5.2.0rp1.
The datatypes in this version are not interchangable with ESMF nor will the
answers be exactly identical.

This version supports the NOLEAP and GREGORIAN calendar.  It also supports
use of the D and Dl interfaces in ESMF_TimeSet and ESMF_TimeGet.  The julian
day reference is that day 1 is year 0, month 1, day 1 (0000-01-01 or Jan 1, 0000).
It also supports positive or negative years.

Several aspects of the ESMF interfaces are not supported.

There is a unit tester that tests ESMF_Time and ESMF_TimeInterval actions
for both gregorian and noleap calendar.

The code was adapted by Rodrigues, L.F. from INPE. The ESMF Time Manager is used by MONAN's model

## How to get the code

To build the library You will need the FPM, Fortran Package Manager.
You can obtain FPM in https://fpm.fortran-lang.org/ or by github in https://github.com/fortran-lang/fpm

## How to compile

To compile go to main dir (ESMF_TIME_F90) and type the command in a terminal:

```bash
fpm build --compiler 'mpif90'
```
The library will be present in build directory.