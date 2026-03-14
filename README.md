
College website Simulator:This code simulates a college website by taking names and rolls and checking them then calculating marks of those subjects and other actions as well.The three names and rolls used in the website are Awais(721),Saif(726),Haris(709)

      //This code simulates the structure of a college website,ofcourse it needs many things but this basic code helped me understand a lot about C language.
      #include <stdio.h>
      #include <conio.h>
      #include <string.h>
      #include <unistd.h>
      #include<stdlib.h>
    //The code may not work in some softwares

      int bb()
    {
	printf("\tError...Restrart");
	clrscr();
	return 0;
    }
     int nn()
         {
	int q,j;
	clrscr();
	printf("\t1.Check Attandence\n\t2.College Notices\n\t3.Announcements\n\t4.Exit\n");
	
	
	printf("\tEnter:");
	scanf("%d",&q);
	if(q==1)
	{
		clrscr();
		printf("\tEnter roll number:");
		scanf("%d",&j);
		    if(j==721)
		    {
		    	printf("\tPresent days:49\n");
		    	printf("\tAbsent days:51");
		    }
		    else if(j==709)
		    {
		    	printf("\tPresent days:39\n");
		    	printf("\tAbsent days:61");
		    }
		
		    else if(j==726)
		    {
		    	printf("\tPresent days:1\n");
		    	printf("\tAbsent days:99");
		    }
		    else
		    printf("\tWrong roll number");
		   
		

	}
	else if(q==2)
     {
	printf("\n\t--- College Notices ---\n");
    printf("\t1. College will be closed on Friday due to public holiday.\n");
      printf("\t2. Annual Sports Day will be held on 25th March.\n");
        printf("\t3. Library timings have been changed to 8:00 AM - 5:00 PM.\n");
         printf("\t4. Semester exams will start from 10th April.\n");
          printf("\t5. Students must submit their lab assignments by 15th March.\n");
           printf("\t6. Scholarship applications are open until 20th March.\n");
            printf("\t7. College has organized a guest lecture on Cybersecurity on 18th March.\n");
             printf("\t8. Notice: Strict attendance policy will be enforced this semester.\n");
              printf("\t9. College ID cards must be carried at all times.\n");
               printf("\t10. Maintenance work in the computer lab from 12 PM to 3 PM on 16th March.\n");
	}
	else if (q==3)
	{
		printf("\n\t--- College Announcements ---\n");
    printf("\t1. New semester registration starts from 1st March.\n");
    printf("\t2. Guest lecture on Artificial Intelligence on 22nd March in Auditorium.\n");
    printf("\t3. Inter-college debate competition on 28th March.\n");
    printf("\t4. Blood donation camp on 30th March in the main hall.\n");
    printf("\t5. College annual cultural festival on 5th April.\n");
    printf("\t6. Workshop on Ethical Hacking scheduled for 15th April.\n");
    printf("\t7. Parent-teacher meeting on 12th April from 10 AM.\n");
    printf("\t8. Notice: Wearing college uniform is mandatory from 1st April.\n");
    printf("\t9. Online course registrations are open for Python and Cybersecurity.\n");
    printf("\t10. Library will remain closed on public holidays.\n");

	}
	else 
	exit(0);
	
	
	
	
	
	
	
	return 0;
    }
    int gg(int x,char k[])
     {
     if(x == 721) {
        if(strcmp(k, "Awais") == 0 || strcmp(k, "awais") == 0) {
            printf("\tAccess granted for Awais\n");
        } else {
            printf("\tInvalid roll number\n");
            exit(0);
        }
    } 
    else if(x == 709) {
        if(strcmp(k, "Haris") == 0 || strcmp(k, "haris") == 0) {
            printf("\tAccess granted for Haris\n");
        } else {
            printf("\tInvalid roll number\n");
            exit(0);
        }
    } 
    else if(x == 726) {
        if(strcmp(k, "Saif") == 0 || strcmp(k, "saif") == 0) {
            printf("\tAccess granted for Saif\n");
        } else {
            printf("\tInvalid roll number\n");
            exit(0);
        }
    } 
    else {
        printf("\tInvalid roll number\n");
        exit(0);
      }



	return 0;
      }


     int main()
     {
	char y[20];
	int o, a, b, c, d, f, g, v;
	float n, m;

	puts("\t\tWelcome to our College Website");
	printf("\tEnter your name:");
	scanf("%s", &y);
	if (strcmp(y, "Awais") == 0 || strcmp(y,"awais") == 0 || strcmp(y,"Saif")==0 || strcmp(y,"Haris")==0 ||strcmp(y,"haris")==0)
	{
		puts("\t Name matched");

		printf("\t Enter Roll number:");
		scanf("%d", &c);
		if (c == 721||c==709||c==726)
		{
			gg(c,y);
			puts("\t Roll number matched");
			printf("\tLoading");
			sleep(2);
			clrscr();
			printf("\tEnter your marks of:\n\tEnglish:");
			scanf("%d", &b);

			if (b > 100)
			{
				puts("\tWrong marks");
				bb();
			}

			printf("\tMaths:");
			scanf("%d", &a);

			if (a > 100)
			{
				puts("\tWrong marks");
				bb();
			}
					printf("\tPhysics:");
					scanf("%d", &o);

					if (o > 85)
					{
						puts("\tWrong marks");
						bb();
					}

					printf("\tUrdu:");
					scanf("%d", &d);

					if (d > 100)
					{
							puts("\tWrong marks");
							bb();
					}

					printf("\tComputer:");
					scanf("%d", &f);

					if (f > 75)
					{
						puts("\tWrong marks");
						bb();
					}

					printf("\tPakistan Studies:");
					scanf("%d", &g);

					if (g > 50)
					{
						puts("\tWrong marks");
						bb();
					}

					printf("\tTarjumatal Quran:");
					scanf("%d", &v);

					if (v > 50)
					{
						puts("\tWrong marks");
						bb();
					}

					printf("\tTotal marks:%d|560", a + b + o + d + f + g + v);
					m = a + b + o + d + f + g + v;
					printf("\tPercentage:%.2f|100", m / 560 * 100);
					printf("\n     Your grade is:");
					n = m / 560 * 100;
					if (n <= 32)
						puts("\tF");
					else if (n >= 33 && n <= 40)
						puts("\tD");
					else if (n >= 41 && n <= 63)
						puts("\tC");
					else if (n >= 64 && n <= 79)
						puts("\tB");
					else if (n >= 80 && n <= 100)
						puts("\tA");
					else
						puts("\tError \n\t Try again");
				}
				else printf("\t Wrong roll number");
			}

			else
				puts("\t wrong name");
			
					int gha;
				printf("\n\tEnter 1 for servies\n\tEnter 2 to leave");
				scanf("%d",&gha);
				if(gha==1)
				{
				nn();
				}
				else
				{
    puts("\tLoading...");
    sleep(1);
				}

			getche();
			return 0;
		}
    
