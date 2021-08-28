//MINI PROJECT USING C--ELECTION SYSTEM
#include<stdio.h>
#include<string.h>
struct candidateinfo
{
  char name[50];
  int age;
  int yearsinpower;
} e[3], *eptr;
int vcA = 0, vcB = 0, vcC = 0, vS = 0,i;
void
castvote (struct candidateinfo *eptr)
{
  int yoursvote;
  printf
    ("\nWhom do you wanna look upto for the next 5 years ?\n Please , Enter your choice of candidate (1-4) :\n");
  scanf ("%d", &yoursvote);
  switch (yoursvote)
    {
    case 1:
      vcA++;
      break;
    case 2:
      vcB++;
      break;
    case 3:
      vcC++;
      break;
    case 4:
      vS++;
      break;
    default:
      printf ("\n Oopss ! INVALID\n TRY AGAIN PLEASE!!!:(");
    }
  system ("cls");
}

 

void
votes (struct candidateinfo *eptr)
{
  printf ("\n ALISHA_BUDHA=%d",vcA);
  printf ("\n MOKSHADA_DAHAL=%d",vcB);
  printf ("\n LAYAS_THAPALIYA=%d",vcC);
  printf ("\n %s=%d\n", "Spoiled Votes", vS);
}

 

void
winner ()
{
  printf ("\n----|-------|--------|------\n\a");
  if (vS > vcA && vS > vcB && vS > vcC) {
    printf("NONE IS LEADING FOR NOW :(");
  } else if (vcA == vcB && vcB == vcC && vcA == vcC) {
    printf("\n\t##IT'S ALL TIE FOR NOW!!");
  } else if (vcA == vcB ? (vcA >
      vcC ? printf("ALISHA BUDHA and MOKSHADA DAHAL are in same line!!") :
      printf("\n\t##LAYAS THAPALIYA is leading\n")) :
    (vcA == vcC ? (vcA >
        vcB ? printf("ALISHA BUDHA and LAYAS THAPALIYA are in same line!!") :
        printf("\n\t##MOKSHADA DAHAL is leading\n")) :
      (vcC == vcB ? (vcC >
          vcA ?
          printf("MOKSHADA DAHAL and LAYAS THAPALIYA are in same line!!") :
          printf("\n\t##ALISHA BUDHA is leading\n")) :
        (vcA >
          vcB ? (vcA >
            vcC ? printf("\n\t##ALISHA BUDHA is leading\n") :
            printf("\n\n##LAYAS THAPALIYA is leading\n")) : (vcB >
            vcC ?
            printf("\n\t##MOKSHADA DAHAL is leading\n") :
            printf("\n\t##LAYAS THAPALIYA is leading\n"))))));
  printf
    ("\nTHANKS FOR VOTING!! \n Looking forward to calling them leader LOL");
  printf ("\n----|-------|--------|------\n\a");
}

 

int
main ()
{
  struct candidateinfo e[3] = {
    [0].name = "ALISHA_BUDHA",
    [1].name = "MOKSHADA_DAHAL",
    [2].name = "LAYAS_THAPALIYA",
    [0].age = 55,
    [1].age = 45,
    [2].age = 50,
    [0].yearsinpower = 3,
    [1].yearsinpower = 4,
    [2].yearsinpower = 5,
  };
  int choice;
  //Use of pointer to structure
  eptr = &e[0];
  FILE *fptr;
  fptr = fopen ("D:\\Electioninfo.txt", "w+b");
  int i;
  //Election2024 info being written to file for permanent security OKIEE !!
  //Use of Repetitive Structure(looping)
  for (i = 0; i < 3; i++)
    {
      fflush (stdin);
      fprintf (fptr, "\nName=%s \t\t Age=%d\t\t Yearsinpower=%d\t\t\n ",
           e[i].name, e[i].age, e[i].yearsinpower);
    }
  //Reading info from the file
  fseek (fptr, 0, SEEK_SET);
  fflush (stdin);
  for (i = 0; i < 3; i++)
    {
      fscanf (fptr, "\nName=%s\t\t Age=%d\t\t Yearsinpower=%d\t\t\n ",
          e[i].name, &e[i].age, &e[i].yearsinpower);
    }
    printf("                                                  ================================================================");
  printf
    ("\n                                                         WELCOME TO 2024 PRESIDENTIAL ELECTION VOTING PLATFORM  \n");
     printf("                                                 ===============================================================\n\n\n\n");
  do
    {
    	system("color 0C");
    //Use of escape sequences
     printf(" \t\t\t\t  =================   FOLLOW THIS  ===================");
      printf("\n                                 ||                                                  ||");
      printf ("\n                                 || [1]  Cast vote to the most elligible candidate ! ||");
      printf("\n                                 ||                                                  ||");
      printf ("\n                                 || [2]  Find the numbers of votes each won !        ||");
      printf("\n                                 ||                                                  ||");
      printf ("\n                                 || [3]  Check who's on board a winning cruise !     ||");
      printf("\n                                 ||                                                  ||");
      printf ("\n                                 || [0]  EXIT !                                      ||");
      printf("\n                                 ||                                                  ||\n");
    printf(" \t\t\t\t  ====================================================");
          printf ("\nEnter your choice:\n");
      scanf ("%d", &choice);
      system ("cls");
      if (choice == 1)
    {
    	printf ("                                     The info of the candidates at your disposal !!\n\n\n");
      for (i = 0; i < 3; i++)
        {
          printf (" %d))", i + 1);
          printf ("\n Name=%s\t\t Age=%d\t\t Yearsinpower=%d\t\t\n ",
              (eptr + i)->name, (eptr + i)->age,
              (eptr + i)->yearsinpower);
        }
      printf ("\n\t4 for none of those candidates:/\n");
      castvote (&e[3]);
    }
      if (choice == 2)
    {
      votes (&e[3]);
    }
      if (choice == 3)
    {
      winner ();
    }
    }
  while (choice != 0);
  fclose (fptr);
  printf ("\n\n\t## THANKS FOR VOTING !!!!! HAVE A GREAT DAY :) ##\n\n");
  return 0;
}
 
