# puzzle-games 
#In python
import math
number_of_bananas=int(input('Enter number of bananas: '))
distance_of_camel=int(input('Enter distance the camel can travel at once: '))
camel_eats=int(input('Enter the number of bananas the camel eats at every km: '))
carry=int(input('Enter number of bananas it can carry: '))
#for first drop- (drop at every 1k) Lets say x distance
#3000-5x=2000
#3000-2000=5x
#x=(3000-2000)/5
x=(number_of_bananas-(number_of_bananas-1000))/(((number_of_bananas*2)/carry)-1)
x=math.ceil(x)
number_of_bananas=number_of_bananas-1000
#for second drop- (drop at every 1k) Lets say y distance
#2000-3y=1000
#2000-1000=3y
#y=(2000-1000)/3
y=(number_of_bananas-(number_of_bananas-1000))/(((number_of_bananas*2)/carry)-1)
y=math.ceil(y)
number_of_bananas=number_of_bananas-1000;
z=distance_of_camel-(x+y); #1000-(200+334)=466
print('Maximum Bananas to reach market:')   
print(number_of_bananas-z) #1000-466=534

#In c++
#include <iostream>
#include <cmath>
using namespace std;

int main()
{
    double number_of_bananas, distance_of_camel, camel_eats, carry, x=0.0,y=0.0,z=0.0;
    cout<<"Enter number of bananas: ";
    cin>>number_of_bananas;
    cout<<"Enter distance the camel can travel at once: ";
    cin>>distance_of_camel;
    cout<<"Enter the number of bananas the camel eats at every km: ";
    cin>>camel_eats;
    cout<<"Enter number of bananas it can carry: ";
    cin>>carry;
    /*for first drop- (drop at every 1k) Lets say x distance
    
    3000-5x=2000
    3000-2000=5x
    x=(3000-2000)/5
    */
    x=(number_of_bananas-(number_of_bananas-1000))/(((number_of_bananas*2)/carry)-1);
    
    number_of_bananas=number_of_bananas-1000;
    /*for second drop- (drop at every 1k) Lets say y distance
    
        2000-3y=1000
        2000-1000=3y
        y=(2000-1000)/3
        */
        
y=(number_of_bananas-(number_of_bananas-1000))/(((number_of_bananas*2)/carry)-1);
cout<<y<<endl;
y=ceil(y);
cout<<y<<endl;
   
    
number_of_bananas=number_of_bananas-1000;
z=distance_of_camel-(x+y);
   cout<<number_of_bananas-z;
    return 0;
}

