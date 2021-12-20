#// myworld1
For fun &amp; learning only
#include<iostream>
using namespace std;
class Area{
public:
void setLength(int l){
length=l;}
void setBreadth(int b){breadth=b;}
protected:
int length,breadth;};
class PerSQcost{
public:
int getCost(int area){return area*1500;}};
class Room:public Area,
public PerSQcost{
public:int getArea(){return(length*breadth);}};
void main(){
Room R;
int area;
R.setLength(5);
R.setBreadth(7);
area=R.getArea();
cout<<"Area of Room"<<R.getArea()<<endl;
cout<<"Cost of Room($):"<<R.getCost(area)<<endl;}
