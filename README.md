# Hostel-Management
#include<iostream>
#include<fstream>
#include<string>
#include<conio.h>
#include<windows.h>

using namespace std;

class workers
{
	private:
	 	string w_name;
	 	string w_Phone_No;
	 	string w_Address;
	 	string w_job;
	public:
		workers()
		{
			w_name = "";
			w_Phone_No = "";
			w_Address = "";
			w_job = "";
		}
		workers(string n, string p, string a   , string j)
		{
			w_name = n;
			w_Phone_No = p;
			w_Address = a;
			w_job = j;
		}
		string getName()
        {
            return w_name;
        }
        string getAddress()
        {
            return w_Address;
        }
        string getPhone_no()
        {
            return w_Phone_No;
        }
        string getjob()
        {
            return w_job;
        }
	 	void display()
	 	{
	 		cout<<"\t\t> Name : "<<w_name<<endl;
	 		cout<<"\t\t> Address : "<<w_Address<<endl;
			cout<<"\t\t> Phone_No : "<<w_Phone_No<<endl; 	
			cout<<"\t\t> Job : "<<w_job<<endl<<endl;
		}
};

class Student
{
    protected:
        string std_name;
        string std_Address;
        string std_Phone_No;
        int Room_No;
    public:
        Student()
        {
        	 std_name = "";
        	 std_Address = "";
        	 std_Phone_No = "";
        	 Room_No = 0;
        }
        string getName()
        {
            return std_name;
        }
        string getaddress()
        {
            return std_Address;
        }
        string getphone_no()
        {
            return std_Phone_No;
        }
        int getroom_no()
        {
            return Room_No;
        }
};

class HostelManagementSystem :public Student
{
    private:
        double Total_income;
        double bulding_rent;
        double water_bill;
        double electercity_bill;
        double Gas_bill;
        double Total_salary_of_workers;
        double Mess_payments;
         

    public:
    	HostelManagementSystem()
    	{
    		Total_income = 0;
    		bulding_rent = 0;
    		water_bill = 0;
    		electercity_bill = 0;
    		Gas_bill = 0;
    		Total_salary_of_workers = 0;
    		Mess_payments = 0;
		}
		
        void menu();
		void facilites();
        void write_student();
		void calculation();
		void search();
		void show_student();
};

void HostelManagementSystem::calculation()
{
			cout<<endl;
			cout<<"\t\t> Enter the total income : ";
			cin>>Total_income;
			while(Total_income < 0)
        	{
        		cout<<"\t\tYou Enter an Invalid Total_income."<<endl;
        		cout<<"\t\t> Again Enter the Total_income :  ";
        		cin>>Total_income;
			}
			cout<<"\t\t> Enter the bulding rent : ";
			cin>>bulding_rent;
			while(bulding_rent < 0)
        	{
        		cout<<"\t\tYou Enter an Invalid bulding_rent."<<endl;
        		cout<<"\t\t> Again Enter the bulding_rent :  ";
        		cin>>bulding_rent;
			}
			cout<<"\t\t> Enter the water_bill : ";
			cin>>water_bill;
			while(water_bill < 0)
        	{
        		cout<<"\t\tYou Enter an Invalid water_bill."<<endl;
        		cout<<"\t\t> Again Enter the water_bill :  ";
        		cin>>water_bill;
			}
			cout<<"\t\t> Enter the electercity_bill : ";
			cin>>electercity_bill;
			while(electercity_bill < 0)
        	{
        		cout<<"\t\tYou Enter an Invalid electercity_bill."<<endl;
        		cout<<"\t\t> Again Enter the electercity_bill :  ";
        		cin>>electercity_bill;
			}
			cout<<"\t\t> Enter the Gas_bill : ";
			cin>>Gas_bill;
			while(Gas_bill < 0)
        	{
        		cout<<"\t\tYou Enter an Invalid Gas_bill."<<endl;
        		cout<<"\t\t> Again Enter the Gas_bill :  ";
        		cin>>Gas_bill;
			}
			cout<<"\t\t> Enter the Mess_payments : ";
			cin>>Mess_payments;
			while(Mess_payments < 0)
        	{
        		cout<<"\t\tYou Enter an Invalid Mess_payments."<<endl;
        		cout<<"\t\t> Again Enter the Mess_payments :  ";
        		cin>>Mess_payments;
			}
			cout<<"\t\t> Enter the salary of workers : ";
			cin>>Total_salary_of_workers;
			while(Total_salary_of_workers < 0)
        	{
        		cout<<"\t\tYou Enter an Invalid Total_salary_of_workers."<<endl;
        		cout<<"\t\t> Again Enter the Total_salary_of_workers :  ";
        		cin>>Total_salary_of_workers;
			}
			
			Total_income = Total_income - (bulding_rent + water_bill + electercity_bill + Gas_bill + Mess_payments + Total_salary_of_workers );
			cout<<endl<<endl<<"\t\t> The total income of this month : "<<Total_income<<endl;
			cout<<endl<<endl;
			cout<<"\t\tPRESS ANY KEY TO GO BACK TO HOMEPAGE."<<endl;
        	_getch();
}

void HostelManagementSystem::facilites()
{
	system("cls");
			cout<<endl<<endl<<endl;
			cout<<"\t\t *************************AL-NEEL BOYS HOSTEL****************************"<<endl;
			cout<<endl;
			cout<<"\t\t ***************************OTHER SERVICES*******************************"<<endl;
			cout<<"\t\t ------------------------------------------------------------------------"<<endl;
			cout<<endl;
			cout<<"\t\t > FACILITES..."<<endl<<endl;
			cout<<"\t\t  * Quality Food & Times"<<endl;
			cout<<"\t\t  * Bedding & Sofa Cam Bed System"<<endl;
			cout<<"\t\t  * 24/7 Backup Generator Facilites"<<endl;
			cout<<"\t\t  * Secures High Speed Internet"<<endl;
			cout<<"\t\t  * Gas, Heater in Winter Season"<<endl;
			cout<<"\t\t  * Hot & Cool Water"<<endl;
			cout<<"\t\t  * First Aid Kit Available in office"<<endl;
			cout<<endl;
			cout<<"\t\t > SPECIAL SERVICES..."<<endl<<endl;
			cout<<"\t\t  * Guest are free for Quarter of every month."<<endl;
			cout<<"\t\t  * Use of Kitchen and Order of desire meal."<<endl;
			cout<<"\t\t  * AC Room on Demand."<<endl;
			cout<<"\t\t  * Servant for Room Services and House Job."<<endl;
			cout<<"\t\t  * Room Cleaning Services in Daily Basis."<<endl;
			cout<<"\t\t  * High Security System With CCTV Camera and Biometric System on main Gate."<<endl<<endl;
			cout<<"\t\t  ****************************CONTACT NUMBERS****************************"<<endl<<endl;
			cout<<"\t\t                 |   Afaq Nasir   | Muhammad Ashir | "<<endl;
			cout<<"\t\t                 |  0300-1756987  |  0317-5678543  | "<<endl<<endl<<endl;
			cout<<"\t\t ----------------------------------------------------------------------------"<<endl;
			
			
			ofstream file("Service.txt",ios::app);
			if(!file.is_open())
			{
				cout<<"File is not open..."<<endl;
			}
			
			else
			{
				cout<<endl<<endl<<endl;
			file<<"\t\t *************************AL-NEEL BOYS HOSTEL****************************"<<endl;
			file<<endl;
			file<<"\t\t ***************************OTHER SERVICES*******************************"<<endl;
			file<<"\t\t ------------------------------------------------------------------------"<<endl;
			file<<endl;
			file<<"\t\t > FACILITES..."<<endl<<endl;
			file<<"\t\t  * Quality Food & Times"<<endl;
			file<<"\t\t  * Bedding & Sofa Cam Bed System"<<endl;
			file<<"\t\t  * 24/7 Backup Generator Facilites"<<endl;
			file<<"\t\t  * Secures High Speed Internet"<<endl;
			file<<"\t\t  * Gas, Heater in Winter Season"<<endl;
			file<<"\t\t  * Hot & Cool Water"<<endl;
			file<<"\t\t  * First Aid Kit Available in office"<<endl;
			file<<endl;
			file<<"\t\t > SPECIAL SERVICES..."<<endl<<endl;
			file<<"\t\t  * Guest are free for Quarter of every month."<<endl;
			file<<"\t\t  * Use of Kitchen and Order of desire meal."<<endl;
			file<<"\t\t  * AC Room on Demand."<<endl;
			file<<"\t\t  * Servant for Room Services and House Job."<<endl;
			file<<"\t\t  * Room Cleaning Services in Daily Basis."<<endl;
			file<<"\t\t  * High Security System With CCTV Camera and Biometric System on main Gate."<<endl<<endl;
			file<<"\t\t  ****************************CONTACT NUMBERS****************************"<<endl<<endl;
			file<<"\t\t                 |   Afaq Nasir   | Muhammad Ashir | "<<endl;
			file<<"\t\t                 |  0300-1756987  |  0317-5678543  | "<<endl<<endl<<endl;
			file<<"\t\t ----------------------------------------------------------------------------"<<endl;
			
			file.close();
			
			}
			cout<<"\t\tPress Enter key to go back to menu"<<endl;
			_getch();
			system("cls");
			
}

void HostelManagementSystem::menu()
{
	system("cls");
			cout<<"\t\t   *************************AL-NEEL BOYS HOSTEL***************************"<<endl;
			cout<<endl;
			cout<<"\t\t   *******************************MESS MENU*******************************"<<endl;
			cout<<endl<<endl;
			cout<<"\t\t    --------------------------------------------------------------------"<<endl;
			cout<<"\t\t    | DAYS |   BREAKFAST   |        LUNCH         |       DINNER       |"<<endl;
			cout<<"\t\t    --------------------------------------------------------------------"<<endl;
			cout<<"\t\t    | MON  | Paratha + tea | Chappati + Vegetable | Chicken + Chappati |"<<endl;
			cout<<"\t\t    --------------------------------------------------------------------"<<endl;
			cout<<"\t\t    | TUE  | Paratha + tea |   Chappati + Daal    |       Biryani      |"<<endl;
			cout<<"\t\t    --------------------------------------------------------------------"<<endl;
			cout<<"\t\t    | WED  | Paratha + tea |   Chappati + Lobia   |    Chinese Rice    |"<<endl;
			cout<<"\t\t    --------------------------------------------------------------------"<<endl;
			cout<<"\t\t    | TRU  | Paratha + tea | Chappati + Vegetable | Chicken + Chappati |"<<endl;
			cout<<"\t\t    --------------------------------------------------------------------"<<endl;
			cout<<"\t\t    | FRI  | Paratha + tea |   Chappati + Daal    |  Haleem + Chappati |"<<endl;
			cout<<"\t\t    --------------------------------------------------------------------"<<endl;
			cout<<"\t\t    | SAT  | Paratha + tea |      Tea party       |  Qeema + Chappati  |"<<endl;
			cout<<"\t\t    --------------------------------------------------------------------"<<endl;
			cout<<"\t\t    | SUN  |     Al-Neel special breakfast        |       Biryani      |"<<endl;
			cout<<"\t\t    --------------------------------------------------------------------"<<endl;
			
			cout<<endl<<endl;
			cout<<"\t\t NOTE : INCASE OF ANY KIND OF COMPLAINT PLEASE CONTACT HOSTEL ADMINISTRATION"<<endl<<endl;
			cout<<"\t\t  ****************************CONTACT NUMBERS****************************"<<endl<<endl;
			cout<<"\t\t                 |   Afaq Nasir   | Muhammad Ashir | "<<endl;
			cout<<"\t\t                 |  0300-1756987  |  0317-5678543  | "<<endl<<endl<<endl;
			cout<<"\t\t ----------------------------------------------------------------------------"<<endl;
			
			
			
			ofstream outfile("menu.txt",ios::app);
			if(!outfile.is_open())
			{
				cout<<"File is not open..."<<endl;
			}
			
			else
			{
				outfile<<"\t\t   *************************AL-NEEL BOYS HOSTEL***************************"<<endl;
				outfile<<endl;
				outfile<<"\t\t   *******************************MESS MENU*******************************"<<endl;
				outfile<<endl<<endl;
				outfile<<"\t\t    --------------------------------------------------------------------"<<endl;
				outfile<<"\t\t    | DAYS |   BREAKFAST   |        LUNCH         |       DINNER       |"<<endl;
				outfile<<"\t\t    --------------------------------------------------------------------"<<endl;
				outfile<<"\t\t    | MON  | Paratha + tea | Chappati + Vegetable | Chicken + Chappati |"<<endl;
				outfile<<"\t\t    --------------------------------------------------------------------"<<endl;
				outfile<<"\t\t    | TUE  | Paratha + tea |   Chappati + Daal    |       Biryani      |"<<endl;
				outfile<<"\t\t    --------------------------------------------------------------------"<<endl;
				outfile<<"\t\t    | WED  | Paratha + tea |   Chappati + Lobia   |    Chinese Rice    |"<<endl;
				outfile<<"\t\t    --------------------------------------------------------------------"<<endl;
				outfile<<"\t\t    | TRU  | Paratha + tea | Chappati + Vegetable | Chicken + Chappati |"<<endl;
				outfile<<"\t\t    --------------------------------------------------------------------"<<endl;
				outfile<<"\t\t    | FRI  | Paratha + tea |   Chappati + Daal    |  Haleem + Chappati |"<<endl;
				outfile<<"\t\t    --------------------------------------------------------------------"<<endl;
				outfile<<"\t\t    | SAT  | Paratha + tea |      Tea party       |  Qeema + Chappati  |"<<endl;
				outfile<<"\t\t    --------------------------------------------------------------------"<<endl;
				outfile<<"\t\t    | SUN  |     Al-Neel special breakfast        |       Biryani      |"<<endl;
				outfile<<"\t\t    --------------------------------------------------------------------"<<endl;
				outfile<<endl<<endl;
				outfile<<"\t\t NOTE : INCASE OF ANY KIND OF COMPLAINT PLEASE CONTACT HOSTEL ADMINISTRATION"<<endl<<endl;
				outfile<<"\t\t  ****************************CONTACT NUMBERS****************************"<<endl<<endl;
				outfile<<"\t\t                 |   Afaq Nasir   | Muhammad Ashir | "<<endl;
				outfile<<"\t\t                 |  0300-1756987  |  0317-5678543  | "<<endl<<endl<<endl;
				outfile<<"\t\t ----------------------------------------------------------------------------"<<endl;
				outfile.close();
			}
			cout<<"\t\tPress Enter key to go back to menu..."<<endl;
			_getch();
			system("cls");
			return;
				
}

void HostelManagementSystem::search()
{
	string NAME;
			cout<<"\t\t> Enter the student name:";
			cin>>NAME;
			ifstream fi("student.txt");
			if(! fi.is_open())
			{
				cout<<"file is not open";
			}
			else
			{
				string line;
				bool found = false;
			while (getline(fi, line, '\n'))
			{
				if (line.find(NAME) != -1)
				{
					cout<<"\t\t"<<line <<endl;
					found = true;
					break;
				}
			}
		if (found == false)
			cout << NAME << " is not found!"<<endl;
			fi.close();
			}
			cout<<endl<<endl;
			cout<<"\t\tPRESS ANY KEY TO GO BACK TO HOMEPAGE."<<endl;
        	_getch();
}

void HostelManagementSystem::show_student()
{
	ifstream fi("student.txt");
			if(!fi.is_open())
			{
				cout<<"File is not open"<<endl;
			}
			else
			{
				string line;
				while (getline(fi, line, '\n'))
				{
					cout << line << endl;
				}
				fi.close();
			}
			cout<<endl<<endl;
			cout<<"\t\t PRESS ANY KEY TO GO BACK TO HOMEPAGE."<<endl;
        	_getch();
}

void HostelManagementSystem::write_student()
{
	cin.get();
        	cout<<"\t\t> Enter the student name :  ";
        	getline(cin,std_name);
        	
        	cout<<"\t\t> Enter the student address :  ";
        	getline(cin,std_Address);
        	
        	cout<<"\t\t> Enter the student phone no :  ";
        	getline(cin,std_Phone_No);
        	
        	cout<<"\t\t> Enter the student room no :  ";
        	cin>>Room_No;
        	
			while(Room_No < 0)
        	{
        		cout<<"\t\tYou Enter an Invalid Room no."<<endl;
        		cout<<"\t\t> Again Enter the student room no :  ";
        		cin>>Room_No;
			}
        	cout<<endl;
        	cout<<"\t\t> NOW YOU HAVE BEEN REGISTERED SUCCESSFULLY CHECK YOUR MESS MENU OR EXTRA FACILITIES. THANK YOU"<<endl;
        	
        	ofstream Outfile("Student.txt",ios::app);
			if(!Outfile.is_open())
			{
				cout<<"\t\t File is not open..."<<endl;
			}
			else
			{
				Outfile << "|     Name    |       Address     |     phone no      | Room no |"<<endl;
				Outfile << "|"<<std_name<<"      |"<<std_Address<<"       |"<<std_Phone_No<<"     |"<<Room_No<<" |"<<endl;
        	}
        	cout<<endl;
        	cout<<"\t\t PRESS ANY KEY TO GO BACK TO HOMEPAGE."<<endl;
        	_getch();
}


int main()
{
	system("color 2"); 
	workers w1("Keewan Haider" , "03334567876" , "Kashmir ,PAKISTAN"  , "Cook" );
	workers w2("Ubaid Rizwan" , "03335678876" , "Punjab ,PAKISTAN"  , "Sweeper");
	
	HostelManagementSystem hms;
	bool flag=true;
	while(flag)
	{
		system("cls");
		cout<<endl<<endl;
		cout<<"\t\t***************AL-NEEL BOYS HOSTEL*******************"<<endl;
	    cout<<"\t\t    NEAR CUST UNIVERSITY SIHALA, ISLAMABAD"<<endl;
	    cout<<"\t\t       Contact no. :  03345678987     "<<endl;
	    cout<<"\t\t*****************************************************"<<endl;
		cout << "\t\t1. Add a new student" << endl;
		cout << "\t\t2. Show student information" << endl;
		cout << "\t\t3. Search student" << endl;
		cout << "\t\t4. Show Mess menu" << endl;
		cout << "\t\t5. Show Extra services" << endl;
		cout << "\t\t6. Show Worker details" << endl;
		cout << "\t\t7. Hostel Management system calculation"<<endl;
		cout << "\t\t8. Exit" << endl<< endl;
			
				int choice;
				// user input
				cout << "\t\tEnter your choice: ";
				cin >> choice;
				// switch statement to select an option
				switch (choice)
				{
				case 1:
					hms.write_student();
					break;
				case 2:
					hms.show_student();
					break;
				case 3:
					hms.search();
					break;
				case 4:
					hms.menu();
					break;
				case 5:
					hms.facilites();
					break;
				case 6:
					system("cls");
					cout<<"\t\tDetails of first worker.."<<endl<<endl;
					w1.display();
					cout<<"\t\tDetails of second worker.."<<endl<<endl;
					w2.display();
					cout<<endl<<endl;
					cout<<"\t\tPRESS ANY KEY TO GO BACK TO HOMEPAGE."<<endl;
        			_getch();
					break;
				case 7:
					hms.calculation();
					break;
				case 8:
					cout << "\t\tYou choose to exit." << endl;
					flag=false;
					break;
				default:
					//Invalid choice
					cout << "\t\tInvalid choice. Please try again." ;
					Sleep(2000);
					break;
	    }
	}
return 0;
}
