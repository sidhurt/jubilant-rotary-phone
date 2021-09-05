# jubilant-rotary-phone
Write a class “Employee” to read and print information of an employee with following details:  Data members: Name of the employee, Id of the employee, Department of the employee, basic salary
#include <iostream>
#include <string.h>
using namespace std;

class employee
{
    private:
    char emp_name [50];
    int emp_id;
    char dept [20];
    float basic;
    float DA;
    float HRA;
    float TA;
    int gross;
    
    public:
    void input_details();
    float gross_salary();
    void display_details();
};

void employee :: input_details()
{
    cout<<"Enter employee name: ";
    cin>>emp_name;
    cout<<"Enter employee id: ";
    cin>>emp_id;
    cout<<"Enter employee department: ";
    cin>>dept;
    cout<<"Enter basic salary: ";
    cin>>basic;
}

float employee :: gross_salary()
{
    DA = basic * 0.50;
    HRA = basic * 0.30;
    TA = basic * 0.10;
    gross = basic + DA + HRA + TA;
}

void employee :: display_details()
{
    cout<<"Employee name: "<<emp_name<<endl;
    cout<<"Employee ID: "<<emp_id<<endl;
    cout<<"Employee department: "<<dept<<endl;
    cout<<"Basic salary: "<<basic<<endl;
    cout<<"Gross salary: "<<gross_salary();
}

int main()
{
    employee emp;
    emp.input_details();
    emp.gross_salary();
    emp.display_details();
    
    return 0;
    
}
