### tuto_yacc

testing lex and yacc with a small interpreter



* -> accepts assignation to variable: a=5   (52 variables, from a to z and A to Z)
* -> can add and rest in expression, with variables or values
* -> print command to show the results of an expression or a variable
* -> exit to exit the interpreter
* -> lines end with ";"

examples:
```
└─$ ./calc
a=14;
b=45;
c=a+b;
print c;
Printing 59
exit;
```

```
└─$ ./calc
print 5+6 ;
Printing 11
exit;
```

```
└─$ ./calc
a=5;
print a+33;
Printing 38
exit;
```

--------------------
to generate the calculator:
```
yyacc -d calc.y
lex calc.l
gcc -g lex.yy.c y.tab.c -o calc


  
