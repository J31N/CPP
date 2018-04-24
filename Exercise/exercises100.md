###### exercise1:陣列存取與基本運算

```
#include <iostream>
using namespace std;

int main()
{
  const int NUMBER_OF_ELEMENTS = 2;
  double numbers[NUMBER_OF_ELEMENTS];
  double numbers_squared[NUMBER_OF_ELEMENTS];
  double sum = 0;

  for (int i = 0; i < NUMBER_OF_ELEMENTS; i++)
  {
    cout << "Enter a new number: ";
    cin >> numbers[i];
    sum += numbers[i];
    numbers_squared[i]=numbers[i]*numbers[i];
  }
  cout << "numbers[1] is " << numbers[1] << endl;
  cout << "numbers_squared[1] is " << numbers_squared[1] << endl;
  
  double average = sum / NUMBER_OF_ELEMENTS;

  int count = 0; // The number of elements above average
  for (int i = 0; i < NUMBER_OF_ELEMENTS; i++)
    if (numbers[i] > average)
      count++;

  cout << "Average is " << average << endl;
  cout << "Number of elements above the average " << count << endl;
  system("pause"); 
  return 0;
}


```
```
說明:
numbers_squared[i]=numbers[i]*numbers[i];


```

![result](PIC/EX1.png)

###### exercise2:程式閱讀題

```
#include <iostream>
using namespace std;
int S(int,int);
int main(void)
{
    int i,f[5],x,ans=0;
    for(i=0;i<5;i++) {
      cout<<"請輸入方程式中"<< i <<" 次項的係數";
      cin>>f[i];
    }
    cout<<"請輸入欲計算的變數值";
    cin>>x;
    for(i=0;i<5;i++) {
      ans = ans + S(x,i) * f[i];
    }
    cout<<"f("<<x<<") = "<<ans<<endl;
    return 0; 
}
int S(int x,int n)
{
    int i,tmp=x;
    if(n==0) return 1;
    for(i=1;i<n;i++)
      x = x*tmp;
    return x;  
}

```
###### exercise3:矩陣相乘

```
#include<iostream.h>
#include<math.h>
int a[2][2],b[2][2],c[2][2];
 
void input()
{
for (int i=0;i<=1;i++){
for (int j=0;j<=1;j++)
{
cout<<"請輸入a["<<i+1<<"]["<<j+1<<"]=";
cin>>a[i][j];
cout<<endl
<<"請輸入b["<<i+1<<"]["<<j+1<<"]=";
cin>>b[i][j];
cout<<endl;	
}
}
}
void input2()
{
input();	
for (int i=0;i<=1;i++){
for (int j=0;j<=1;j++){
for (int k=0;k<=1;i++){
c[i][j]=c[i][j]+a[k][j]*b[i][k];
}
}
}
void main()
{
char x='y';
while (x=='y'||x=='Y')
{
input2();
for (int i=0;i<=1;i++){
for (int j=0;j<=1;j++){
cout<<"c["<<i+1<<"]["<<j+1<<"]="<<c[i][j]<<"\t";
}
cout<<endl;
}
cout<<"Do you want to try again?(y/n)";
cin>>x;
cout<<endl;
}
}

```
###### exercise3:矩陣相乘

```
#include <iostream>
using namespace std;

class Circle
{
public:
  // The radius of this circle
  double radius;

  // Construct a default circle object
  Circle()
  {
    radius = 1;
  }

  // Construct a circle object
  Circle(double newRadius)
  {
    radius = newRadius;
  }

  // Return the area of this circle
  double getArea()
  {
    return radius * radius * 3.14159;
  }
};  // Must place a semicolon here

int main()
{
  Circle circle1(1.0);
  Circle circle2(25);
  Circle circle3(125);

  cout << "The area of the circle of radius "
    << circle1.radius << " is " << circle1.getArea() << endl;
  cout << "The area of the circle of radius "
    << circle2.radius << " is " << circle2.getArea() << endl;
  cout << "The area of the circle of radius "
    << circle3.radius << " is " << circle3.getArea() << endl;

  // Modify circle radius
  circle2.radius = 100;
  cout << "The area of the circle of radius "
    << circle2.radius << " is " << circle2.getArea() << endl;

  return 0;
}
'''
