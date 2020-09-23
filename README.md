<div align="center">

## Bubble Sort


</div>

### Description

The purpose of this code is to show novice programmers the simple and classic sorting method of Bubble Sort. The code is in C/C++ and should be compilied in DJGPP. The code includes the Bubble Sort Algorithm in action.
 
### More Info
 
No Inputs

The code is complete. The Bubble Sort Algorithm is modulizied inside its own function. It is called from main, the current implementation sorts an array of ints, but can be modified to sort varying data types.

No Returns

No Side Effects


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Joshua Thompson](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/joshua-thompson.md)
**Level**          |Beginner
**User Rating**    |4.2 (21 globes from 5 users)
**Compatibility**  |C, C\+\+ \(general\)
**Category**       |[Algorithms](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/algorithms__3-29.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/joshua-thompson-bubble-sort__3-550/archive/master.zip)

### API Declarations

```
#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
```


### Source Code

```

/* Function Prototypes */
void BubbleSort( int Array[], const int Size );
void PrintArray( int Array[], const int Size );
int main( void )
{
 int i;
 const int Size = 20;
 int Array[ Size ];
 /* Fill the Array with random values
   between 0 and 99 */
 for( i = 0; i < Size; i++ )
  Array[i] = random() % 100;
 /* Print the Random Array to Screen */
 clrscr();
 printf( "The Array with random order:\n\n");
 PrintArray( Array, Size );
 /* Wait for key Press... */
 printf( "\nPress any key..." );
 getch();
 /* Sort the Array using Bubble Sort */
 BubbleSort( Array, Size );
 /* Print the Smallest-to-Largest
   Order Array */
 clrscr();
 printf( "The Array after Bubble Sort:\n\n");
 PrintArray( Array, Size );
 /* End the Program */
 printf( "\nPress any key to quit..." );
 getch();
 return 0;
}
/* Uses the classic bubble sort algorithm */
void BubbleSort( int Array[], const int Size )
{
 int i, j, temp;
 for( i = 0; i < Size - 1; i++ )
  for( j = 0; j < Size - i + 1; j++ )
   if( Array[j] > Array[j + 1] )
   {
    temp = Array[j];
	Array[j] = Array[j + 1];
	Array[j + 1] = temp;
   }
}
/* Prints an integer Array line by line */
void PrintArray( int Array[], const int Size )
{
 int i;
 for( i = 0; i < Size; i++ )
  printf("Array[%i] = %i\n", i, Array[i] );
}
```

