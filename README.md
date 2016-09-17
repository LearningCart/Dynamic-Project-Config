#Dynamic-Project-Config
========================================
This project will allow the large software (C/C++)

configuration through the means of text configuration file.

e.g.,
Project confugration text file:
"Project.conf"

BUILD_CORE_COMP=TRUE

CREATE_DEBUG_BUILD=false

USE_LOCAL_ALLOC=true

ENABLE_VM=false

ENABLE_REMAPPING=True

etc...,
Generated sysconfig.h

\#define BUILD_CORE_COMP    (1)

\#define CREATE_DEBUG_BUILD    (0)

\#define USE_LOCAL_ALLOC    (1)

\#define ENABLE_VM    (0)

\#define ENABLE_REMAPPING    (1)

How to use in the code?
\#define	ENABLED	(1)

C/C++ soruce code:

\#if (BUILD_CORE_COMP == ENABLED)

    printf("BUILD_CORE_COMP is defined we can enable code which does this feature\n");

\#endif




TODO/FIXME/Future Enhancement:
=================================
1)  multiple = sign not supoorted

2) Trimming of macro not supported yet., e.g, if it is defined as "    ENABLE_CORE_COMP" it will remain as it is in sysconf.h file.

3) Converting LHS value(macro name) to upper case is not yet supported.

4) Spaces or tabs between word are not supported yet., this will bhe cool.., instead of ENABLE_CORE_COMP, we will be able to write enable  "enable _core   _comp" and it sould generate same macro

5) Spell correction is not added e.g., "true" is not "ture"..,

6) Comments are not supported yet.

7) One level of indirection can be added., e.g., file can say which config file to be used.., but not sure of use-case.

