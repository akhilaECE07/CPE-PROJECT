#include<stdio.h>

int main()
{
    int i,num,a[9],p,q,r;
    printf("\n-------------------LET'S PLAY SUDOKU-------------------\nHey Player...looks like you have a great mind!\nLet's test it.\nSolve this Sudoku...");
    printf("\nPick a number from 1, 2, 3: ");
    scanf("%d",&num);
    //-----------------FIRST SUDOKU-------------------
    if(num==1)
    {
        int b[]={1,2,3,3,1,2,2,3,1};
        printf(" 1  _  3 \n_  _  2 \n_  3  _ ");
        printf("\nComplete the grid and enter them\n");
        for(i=0;i<9;i++)
            scanf("%d",&a[i]);
        for(i=0;i<9;i++)
        {
            if(a[i]!=b[i])
            {
                p=1;
                break;
            }
        }
        if(p==1)
            printf("\nOoops...Better luck next time..");
        else
            printf("\nWHOOO..THAT'S GREAT!!!You got it right...");
    }
    //-----------------SECOND SUDOKU------------------
    else
    {
        int c[]={2,3,1,1,2,3,3,1,2};
        if(num==2)
        {
            printf(" 2  3  _ \n_  _  3 \n_  1  _ ");
            printf("\nComplete the grid and enter them\n");
            for(i=0;i<9;i++)
                scanf("%d",&a[i]);
            for(i=0;i<9;i++)
            {
                if(a[i]!=c[i])
                {
                    q=1;
                    break;
                }
            }
            if(q==1)
                printf("\nOoops...Better luck next time..");
            else
                printf("\nWHOOO..THAT'S GREAT!!!You got it right...");
        }
    //----------------THIRD SUDOKU--------------------    
        else
        {
            int d[]={3,1,2,2,3,1,1,2,3};
            printf(" _  1  _ \n2  _  _ \n_  _  3 ");
            printf("\nComplete the grid and enter them\n");
            for(i=0;i<9;i++)
                scanf("%d",&a[i]);
            for(i=0;i<9;i++)
            {
                if(a[i]!=c[i])
                {
                    r=1;
                    break;
                }
            }
            if(r==1)
                printf("\nOoops...Better luck next time..");
            else
                printf("\nWHOOO..THAT'S GREAT!!!You got it right...");
        }
    }
}
