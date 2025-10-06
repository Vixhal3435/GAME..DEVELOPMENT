# EX 7 : THREE DIMENSIONAL TRANSFORMATIONS

## AIM :
 
 To implement the various transformations on three dimensional odjects using a c coding.

## EQUIPMENT REQUIRED:

●	Hardware: Personal Computer (PC)

●	Software: C Compiler

## ALGORITHM :


   Step 1 : Start.

   Step 2 : Draw an image with default parameters.

   Step 3 : Get the choice from user.

   Step 4 : Get the parameters for transformation.

   Step 5 : Perform the transformation.

   Step 6 : Display the output.

   Step 7 : Stop.

## Program :
```
#include<stdio.h> 
#include<conio.h> 
#include<graphics.h> 
#include<math.h> 
int maxx,maxy,midx,midy; 
void axis() 
{ 
getch(); 
cleardevice(); 
line(midx,0,midx,maxy); 
line(0,midy,maxx,midy); 
} 
void main() 
{ 
int gd,gm,x,y,z,o,x1,x2,y1,y2; 
detectgraph(&gd,&gm); 
initgraph(&gd,&gm,"C://TURBOC3//BGI"); 
setfillstyle(0,getmaxcolor()); 
maxx=getmaxx(); 
maxy=getmaxy(); 
midx=maxx/2; 
midy=maxy/2; 
axis(); 
bar3d(midx+50,midy-100,midx+60,midy-90,5,1); 
printf("Enter Translation Factor"); 
scanf("%d%d%d",&x,&y,&z); 
axis(); 
printf("after translation"); 
bar3d(midx+(x+50),midy-(y+100),midx+x+60,midy-(y+90),5,1); 
axis(); 
bar3d(midx+50,midy+100,midx+60,midy-90,5,1); 
printf("Enter Scaling Factor"); 
scanf("%d%d%d",&x,&y,&z); 
axis(); 
printf("After Scaling"); 
bar3d(midx+(x*50),midy-(y*100),midx+(x*60),midy-(y*90),5*z,1); 
axis(); 
bar3d(midx+50,midy-100,midx+60,midy-90,5,1); 
printf("Enter Rotating Angle"); 
scanf("%d",&o); 
x1=50*cos(o*3.14/180)-100*sin(o*3.14/180); 
y1=50*cos(o*3.14/180)+100*sin(o*3.14/180); 
x2=60*sin(o*3.14/180)-90*cos(o*3.14/180); 
y2=60*sin(o*3.14/180)+90*cos(o*3.14/180); 
axis(); 
printf("After Rotation about Z Axis"); 
bar3d(midx+x1,midy-y1,midx+x2,midy-y2,5,1); 
axis(); 
printf("After Rotation about X Axis"); 
bar3d(midx+50,midy-x1,midx+60,midy-x2,5,1); 
axis(); 
printf("After Rotation about Y Axis"); 
bar3d(midx+x1,midy-100,midx+x2,midy-90,5,1); 
getch(); 
closegraph(); 
}

```
## Output :

<img width="637" height="508" alt="Screenshot 2025-10-06 114425" src="https://github.com/user-attachments/assets/bdda86f4-be1d-4911-a832-dbc8a9284c79" />

<img width="641" height="503" alt="Screenshot 2025-10-06 114441" src="https://github.com/user-attachments/assets/bca062dc-488e-46e6-853f-759dc135b222" />

<img width="638" height="508" alt="Screenshot 2025-10-06 114506" src="https://github.com/user-attachments/assets/4e7da4df-1327-447a-ac46-9a0ab3dc6aad" />

<img width="636" height="508" alt="Screenshot 2025-10-06 114521" src="https://github.com/user-attachments/assets/8e4614df-514f-49a5-b7c6-68e180558df6" />

<img width="640" height="508" alt="Screenshot 2025-10-06 114545" src="https://github.com/user-attachments/assets/d19d4131-04bc-4629-82c7-80515df61e44" />

<img width="634" height="507" alt="Screenshot 2025-10-06 114556" src="https://github.com/user-attachments/assets/0aef1ad8-9ab3-451a-9c23-e6b008723cd6" />

<img width="637" height="510" alt="Screenshot 2025-10-06 114605" src="https://github.com/user-attachments/assets/77313dfc-6d5d-41f9-97f5-1a1f9065d219" />

<img width="635" height="509" alt="Screenshot 2025-10-06 114617" src="https://github.com/user-attachments/assets/cfb73bc1-39c6-47d8-afdb-21227d90e29a" />

## Result :

Thus, the C program for performing three-dimensional transformations — including translation, scaling, and rotation about the X, Y, and Z axes — was successfully implemented and the output was verified through graphical representation.
