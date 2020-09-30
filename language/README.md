# A Linguagem Cminus (ou C-)

The C- language specification is excerpted  and adapted from the book Compiler Construction Principles And Practice by Kenneth Louden. The language includes integer variables, functions, and arrays. It has local and global declarations and supports conditions (if-statement) and repetitions (while-statement), as well as supports recursive function calls. It is essentially a subset of C, but is missing some more advanced features, hence its name.

Below you can find the lexical conventions, syntax and semantics description of the language.

## Lexical Conventions

## Syntax

## Semantics

## Sample Programs

### Sample Program 1
The following is a program that inputs two integers, computes their greatest common divisor, and prints it:

```
/* A program to perform Euclid's

   Algorithm to compute gcd. */



int gcd (int u, int v)

{

    if (v == 0) return u ;

    else return gcd(v,u-u/v*v);

    /* u-u/v*v == u mod v */

}



void main(void) 

{ 

   int x; int y;

   x = input(); 

   y = input();

   output(gcd(x, y)) ;

}
```

### Sample Program 2
The following is a program that inputs a list of 10 integers, sorts them by selection sort, and outputs them again:

```
/* A program to perform selection sort on a 10 element array */



int x[10];



int minloc(int a[], int low, int high) {

    int i; int x; int k;

    k = low;

    x = a[low];

    i = low + 1;

    while (i < high) {

        if (a[i] < x) {

            x = a[i];

            k = i;

        }

        i = i + 1;

    }

    return k;

}

void sort(int a[], int low, int high) {

    int i;

    int k;

    i = low;

    while (i < high - 1) {

        int t;

        k = minloc(a, i, high);

        t = a[k];

        a[k] = a[i];

        a[i] = t;

        i = i + 1;

    }

}

void main(void) {

    int i;

    i = 0;

    while (i < 10) {

        x[i] = input();

        i = i + 1;

    }

    sort(x, 0, 10);

    i = 0;

    while (i < 10) {

        output(x[i]);

        i = i + 1;

    }

```
}
