#include<iostream.h>
#include <conio.h>

class Shape
{
protected:
int dim1,dim2;
public:
Shape(){
dim1=dim2=0;
}
Shape(int m){
dim1=dim2=m;
}
Shape(int m,int n){
dim1=m;
dim2=n;
}
void set_dim1(int m){
dim1=m;
}
void set_dim2(int m){
dim2=m;
}
int get_dim1(){
return dim1;
}
int get_dim2(){
return dim2;
}
virtual float area()=0;
};
class Circle: public Shape
{
public:
Circle(int r):Shape(r){}
float area(){
return(3.14*dim1*dim2);
}
};

class Triangle: public Shape
{
public:
Triangle (int dim1,int dim2):Shape(dim1,dim2){}
float area(){
return(0.5*dim1*dim2);
}
};

class Rectangle:public Shape
{
public:
Rectangle (int dim1,int dim2):Shape(dim1,dim2){}
float area(){
return(1.0*dim1*dim2);
}
};

class Square:public Rectangle
{
public:
Square(int dim1):Rectangle (dim1,dim1)
{}
};
class GeoShape
{
Shape * pt[4];
public:
GeoShape(Shape * p1,Shape * p2,Shape * p3,Shape * p4)
{

pt[0]=p1;
pt[1]=p2;
pt[2]=p3;
pt[3]=p4;

}
float get_total_area(){
float sum=0.0;
for(int i=0;i<4;i++){
sum+=pt[i]->area();
}
return sum;
}
};
int main(){
clrscr();
Circle c(5);
Triangle t(3,4);
Square s(2);
Rectangle r(2,4);
Shape * pt[4];
pt[0]=&c;
pt[1]=&t;
pt[2]=&s;
pt[3]=&r;

for(int i=0;i<4;i++){
cout << pt[i]->area()<<endl;
}
GeoShape g(&r,&t,&c,&s);
cout<<g.get_total_area() << endl;
return 0;
}
