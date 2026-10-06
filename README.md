#include<bits/stdc++.h>
using namespace std;
class Employee
{
public:
    string name;
    int id;
    double salary;
    Employee()
    {

    }
    void display()
    {
        cout<<"Name: "<<name<<endl<<"ID: "<<id<<endl
        <<"Salary: "<<salary<<endl;
    }
};
int main()
{
    Employee o[5];
    for(int i=0;i<5;i++)
    {
        cin>>o[i].name>>o[i].id>>o[i].salary;
    }
    for(int i=0;i<5;i++)
    {
        o[i].display();
    }
    double highest=o[0].salary;
    int index=0;
    for(int i=1;i<5;i++)
    {
        if(highest<o[i].salary)
        {
            highest=o[i].salary;
            index=i;
        }
    }
    cout<<highest<<endl<<endl;
    o[index].display();
}
