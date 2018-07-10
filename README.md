I found when learning to use the CVODE libraries, that there were few simple examples to start off with for learning from scratch how to use the libraries. So here is a simple example using the CVODE library to solve a simple 2d ODE, treating it as a stiff system. 

## What is CVODE?

CVODE is a solver for stiff and nonstiff ordinary differential equation (ODE) systems (initial value problem) given in explicit form y’ = f(t,y).

 - https://computation.llnl.gov/projects/sundials/cvode 

## Where do I get the CVODE solver?

To download the libraries go to their software download page:

 - https://computation.llnl.gov/projects/sundials/sundials-software

Appendix A of the CVODE guide gives a pretty good tutorial of how to download, install, and configure the libraries for use depending on the OS you're currently using. 

 - https://computation.llnl.gov/sites/default/files/public/cv_guide.pdf

## Makefile

For those who are Makefile beginners, a simple solution is to use the cpp generic Makefile from:

 - https://github.com/mbcrawfo/GenericMakefile
 
Then add:

```
-lsundials_cvode -lsundials_nvecserial
```

onto the line:

```
LINK_FLAGS = 
```