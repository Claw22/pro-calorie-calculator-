
#include <stdio.h>
#include<string.h>
int main()
{
    int w,h,a,mc;
    int choice;
    char g[50];
    char gender[]="male";
    printf("enter your gender:");
    scanf("%s",g);
    printf("\nenter your weight:");
    scanf(" %d",&w);
    printf("\nenter your height:");
    scanf("%d",&h);
    printf("\nenter your age:");
    scanf("%d",&a);
    //printf("%s\n",gender);
    int res=strcmp(g,gender);
    if(res==0)
    {
        mc=(((10* w) + (6.25* h) - (5* a))*1.2);
        printf("your maintance calories:%d cal/day\n",mc);
        printf("macros:\n");
        printf("protien:%.0f g\n",(w*2.2));
        printf("fat:%.0f g\n",(w*1.025));
        printf("carb:%.0f g\n",(w*2.3));
        printf("1:mild weight loss\n2:weight loss\n3:exterme weight loss\n4:weight gain");
        printf("enter your choice:\n");
        scanf("%d",&choice);
        switch(choice){
            case 1:printf("mild weight loss\n");
            printf("calories for mild weight loss:%d cal/day",((mc*90)/100));
            printf("macros:\n");
            printf("protien:%.0f g\n",(w*2.2));
            printf("fat:%.0f g\n",(w*0.8625));
            printf("carb:%.0f g",(w*1.95));
            break;
            case 2:printf("weight loss\n");
            printf("calories for weight loss:%d cal/day",((mc*80)/100));
            printf("macros:\n");
            printf("protien:%.0f g\n",(w*2.2));
            printf("fat:%.0f g\n",(w*0.7125));
            printf("carb:%.0f g",(w*1.6125));
            break;
            case 3:printf(" exterme weight loss\n");
            printf("calories for exterme weight loss:%d cal/day",((mc*70)/100));
            printf("macros:\n");
            printf("protien:%.0f g\n",(w*2.2));
            printf("fat:%.0f g\n",(w*0.5625));
            printf("carb:%.0f g",(w*1.275));
            break;
            case 4:printf("weight gain\n");
            printf("calories for weight gain:%d cal/day",((mc*120)/100));
            printf("macros:\n");
            printf("protien:%.0f g\n",(w*2.2));
            printf("fat:%.0f g\n",(w*1.3125));
            printf("carb:%.0f g",(w*2.9625));
            break;
            default:
            printf("choose the correct choice");
        }
    }
    else{
        mc=(((10* w) + (6.25* h) - (5* a) - 161)*1.2);
        printf("female your maintance calories:%d cal/day\n",mc);
        printf("1:mild weight loss\n2:weight loss\n3:exterme weight loss\n4:weight gain");
        printf("enter your choice:\n");
        scanf("%d",&choice);
        switch(choice){
            case 1:printf("mild weight loss\n");
            printf("calories for mild weight loss:%d cal/day\n",((mc*90)/100));
            printf("macros:\n");
            printf("protien:%.0f g\n",(w*2.2));
            printf("fat:%.0f g\n",(w*0.95));
            printf("carb:%.0f g",(w*2.133));
            break;
            case 2:printf("weight loss\n");
            printf("calories for weight loss:%d cal/day\n",((mc*80)/100));
            printf("macros:\n");
            printf("protien:%.0f g\n",(w*2.2));
            printf("fat:%.0f g\n",(w*0.6));
            printf("carb:%.0f g",(w*1.783));
            break;
            case 3:printf(" exterme weight loss\n");
            printf("calories for exterme weight loss:%d cal/day\n",((mc*70)/100));
            printf("macros:\n");
            printf("protien:%.0f g\n",(w*2.2));
            printf("fat:%.0f g\n",(w*0.633));
            printf("carb:%.0f g",(w*1.416));
            break;
            case 4:printf("weight gain\n");
            printf("calories for weight gain:%d cal/day\n",((mc*120)/100));
            printf("macros:\n");
            printf("protien:%.0f g\n",(w*2.2));
            printf("fat:%.0f g\n",(w*1.433));
            printf("carb:%.0f g",(w*3.216));
            break;
            default:
            printf("choose the correct choice");
        }
    }
    
} 