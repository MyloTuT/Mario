Mario
=====

Mario is a simple program that recreates the half-pyramid using hashes (#) for blocks.

#include <cs50.h>
#include <stdio.h>

int main(void)

{
  		//Prompt user for integer
            printf("Pick a number between 1 and 23:");
    		int height = GetInt();
    
    		//Loop that determines if int is correct 
       		while ( (height < 0) || (height > 23) )
            {
                printf("Retry:");
                scanf ("%d", &height);
            }

    
    		// Loop that prints rows, spaces, hashes and newline
    		int i, spaces, hashes;
			for ( i = 1; i <= height; i++ )
    		{ 
                    for ( spaces = 0; spaces <= height - i - 1; spaces++ )  //Loop to print spaces
					{
						printf(" ");
					}
                    
                    for ( hashes = 0; hashes <= height - spaces; hashes++ )  //Loop to print hashes
                    {
                        printf("#");
                    }
                   
                    printf("\n");
            }
            return 0;
}
