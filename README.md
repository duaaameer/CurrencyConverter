#include <iostream>
#include <iomanip>
using namespace std;

enum countries{
  BDT = 'a',
  AFN = 'b',
  PKR = 'c',
  INR = 'd', 
  NPR = 'e',
  LKR = 'f',
};

class CurrencyConverter {
protected:
float amount;

public:
CurrencyConverter(float amo) : amount(amo) {}
virtual ~CurrencyConverter() {}
virtual void show() = 0;
};

class SouthAsianConverter : public CurrencyConverter {

public:
SouthAsianConverter(float amo) : CurrencyConverter(amo) {}

void show() override {
char option, posession, choice;
do {
    cout<<"LIST:"<<endl;
    cout<<"a. BDT"<<endl;
    cout<<"b. AFN"<<endl;
    cout<<"c. PKR"<<endl;
    cout<<"d. INR"<<endl;
    cout<<"e. NPR"<<endl;
    cout<<"f. LKR"<<endl;

    cout<<"Your Currency?: ";
    cin>>posession;

    cout<<"Enter Currency for conversion: ";
    cin>>option;

    cout<<"Enter the Amount: ";
    cin>>amount;

if (posession == BDT) {
switch (option) {

        case AFN:
        {cout<<"BDT to AFN = "<<amount*0.66<<" AFN"<<endl;
         break;}
                    
        case PKR:
        {cout<<"BDT to PKR = "<<amount*2.54<<" PKR"<<endl;
        break;}
                    
        case INR:
        {cout<<"BDT to INR = "<<amount*0.76<<" INR"<<endl;
        break;}
                    
        case NPR:
        {cout<<"BDT to NPR = "<<amount*1.22<<" NPR"<<endl;
        break;}
                    
        case LKR:
        {cout<<"BDT to LKR = "<<amount*2.7<<" LKR"<<endl;
        break;}
                    
        default:
        {cout<<"INVALID"<<endl;}}} 
        
else if (posession == AFN) {
    
        switch (option) {

        case BDT:
        {cout<<"AFN to BDT = "<<amount/0.66<<" BDT"<<endl;
        break;}
                    
        case PKR:
        {cout<<"AFN to PKR = "<<amount*3.86<<" PKR"<<endl;
        break;}
                    
        case INR:
        {cout<<"AFN to INR = "<<amount*1.15<<" INR"<<endl;
        break;}
                    
        case NPR:
        {cout<<"AFN to NPR = "<<amount*1.85<<" NPR"<<endl;
        break;}
                    
        case LKR:
        {cout<<"AFN to LKR = "<<amount*4.1<<" LKR"<<endl;
        break;}

        default:
        {cout<<"INVALID"<<endl;}}} 
        
else if (posession == PKR) {
            switch (option) {
            case BDT:
            {cout<<"PKR to BDT = "<<amount*0.39<<" BDT"<<endl;
            break;}
                    
            case AFN:
            {cout<<"PKR to AFN = "<<amount*0.25<<" AFN"<<endl;
            break;}
                    
            case INR:
            {cout<<"PKR to INR = "<<amount*0.299<<" INR"<<endl;
            break;}
                    
            case NPR:
            {cout<<"PKR to NPR = "<<amount*0.482<<" NPR"<<endl;
            break;}
                    
            case LKR:
            {cout<<"PKR to LKR = "<<amount*1.064<<" LKR"<<endl;
            break;}
                    
            default:
            {cout<<"INVALID"<<endl;}}}
            
else if (posession == INR) {
            switch (option) {

            case BDT:
            {cout<<"INR to BDT = "<<amount*1.31<<" BDT"<<endl;
            break;}
                    
            case AFN:
            {cout<<"INR to AFN = "<<amount*0.86<<" INR"<<endl;
            break;}
                    
            case PKR:
            {cout<<"INR to PKR = "<<amount*3.33<<" PKR"<<endl;
            break;}
                    
            case NPR:
            {cout<<"INR to NPR = "<<amount*1.60<<" NPR"<<endl;
            break;}
                    
            case LKR:
            {cout<<"INR to LKR = "<<amount*3.57<<" LKR"<<endl;
            break;}
                    
            default:
            {cout<<"INVALID"<<endl;}}}
else if (posession == NPR) {
        switch (option) {

            case BDT:
            {cout<<"NPR to BDT = "<<amount*0.82<<" BDT"<<endl;
            break;}

            case AFN:
            {cout<<"NPR to AFN = "<<amount*0.52<<" AFN"<<endl;
            break;}
                    
            case PKR:
            {cout<<"NPR to PKR = "<<amount*2.09<<" PKR"<<endl;
            break;}
                    
            case INR:
            {cout<<"NPR to INR = "<<amount*0.62<<" INR"<<endl;
            break;}
                    
            case LKR:
            {cout<<"NPR to LKR = "<<amount*2.23<<" LKR"<<endl;
            break;}
                    
            default:
            {cout<<"INVALID"<<endl;}}}
            
else if (posession == LKR) {
        switch (option) {
                    
            case BDT:
            {cout<<"LKR to BDT = "<<amount*0.37<<" BDT"<<endl;
            break;}
                    
            case AFN:
            {cout<<"LKR to AFN = "<<amount*0.24<<" AFN"<<endl;
            break;}
                    
            case PKR:
            {cout<<"LKR to PKR = "<<amount*0.94<<" PKR"<<endl;
            break;}
                    
            case INR:
            {cout<<"LKR to INR = "<<amount*0.28<<" INR"<<endl;
            break;}
                    
            case NPR:
            {cout<<"LKR to NPR = "<<amount*0.45<<" NPR"<<endl;
            break;}
                    
            default:
            {cout<<"INVALID"<<endl;}}}

else {cout<<"INVALID"<<endl;}

cout << "Do you want to continue? (y/n): ";
cin >> choice;
} while (choice == 'y' || choice == 'Y');
}
};

int main() {
    string name;
    string password;

    cout<<setw(15)<<"=================================================================="<<endl;
    cout<<setw(15)<<"===                                                            ==="<<endl;
    cout<<setw(15)<<"===                     CURRENCY CONVERTER                     ==="<<endl;
    cout<<setw(15)<<"===                                                            ==="<<endl;
    cout<<setw(15)<<"===         That Converts all South Asian Currencies           ==="<<endl;
    cout<<setw(15)<<"===                                                            ==="<<endl;
    cout<<setw(15)<<"=================================================================="<<endl;

    cout<<"Login First!"<<endl;
    cout<<"Enter your Name: ";
    cin>>name;

    do {
        cout<<"Enter your Password : ";
        cin>>password;

        try {
            if(password.length() != 7 || password.substr(0, 4) != "2023") {
            throw ("Incorrect Password");}

            else 
            {cout << "Login Access Granted!" << endl;
            SouthAsianConverter obj(89.95);
            obj.show();}

        } catch (const char* e) {
            cout << "Error: " << e << endl;
        }
    } while (password.length() != 7 || password.substr(0, 4) != "2023");

    return 0;
}

