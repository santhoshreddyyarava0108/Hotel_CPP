# Hotel_CPP
#include<iostream>
#include<iomanip>
#include<cstring>
using namespace std; 

class Management_of_Rooms
{
    public:
        int quant;
        int rcost;
        int rt;
        int aprooms;
        int sprooms;
        int audrooms;
        int sudrooms;
        int adrooms;
        int sdrooms;
        int qp,qu,qd;
        Management_of_Rooms()
        {
            aprooms=20;
            sprooms=0;
            audrooms=20;
            sudrooms=0;
            adrooms=20;
            sdrooms=0;
			rcost=0;
        }
        void display()
        {
        	switch(rt)
        	{
        		case 1: 
        		cout<<"The available Premium Rooms are: "<<aprooms-sprooms<<endl;
        		 if(aprooms-sprooms>=quant)
            	{
                  sprooms=sprooms+quant;
                  rcost=rcost+quant*1800;
                  cout<<"\t\t"<<quant<<" Premium Room/Rooms have been alloted to you for next 24 hours."<<endl;
            	}
            	else
            	{
            	    cout<<"\t\tOnly "<<aprooms-sprooms<<" Premium Rooms are remaining in the Hotel."<<endl;
            	}
            	break;
            	case 2:
            		cout<<"The available Ultra Deluxe Rooms are: "<<audrooms-sudrooms<<endl;
            		 if(audrooms-sudrooms>=quant)
            		{
                  	  	sudrooms=sudrooms+quant;
                  		rcost=rcost+quant*1500;
                  		cout<<"\t\t"<<quant<<" Ultra Deluxe Room/Rooms have been alloted to you for next 24 hours."<<endl;
            		}
            		else
            		{
                		cout<<"\t\tOnly "<<audrooms-sudrooms<<" Ultra Deluxe Rooms are remaining in the Hotel."<<endl;
            		}
            		break;
            	case 3:
            	    cout<<"The available Deluxe Rooms are: "<<adrooms-sdrooms<<endl;
            		if(adrooms-sdrooms>=quant)
            		{
                  		sdrooms=sdrooms+quant;
                  		rcost=rcost+quant*1200;
                  		cout<<"\t\t"<<quant<<" Deluxe Room/Rooms have been alloted to you for next 24 hours."<<endl;
            		}
            		else
            		{
            		    cout<<"\t\tOnly "<<adrooms-sdrooms<<" Deluxe Rooms are remaining in the Hotel."<<endl;
            		}
            		break;
            	default: 
            	cout<<"Please enter valid choice"<<endl;
            	break;
			}
            
        }
        void display2(int p,int ud,int d)
        {
        	 if(aprooms-sprooms>=p)
            	{
                  sprooms=sprooms+p;
                  rcost=rcost+p*1800;
                  cout<<"\t\t"<<p<<" Premium Room/Rooms have been alloted to you for next 24 hours."<<endl;
            	}
            	else
            	{
            	    cout<<"\t\tOnly "<<aprooms-sprooms<<" Premium Rooms are remaining in the Hotel."<<endl;
            	}
            if(audrooms-sudrooms>=ud)
           		{
    	       	  	sudrooms=sudrooms+ud;
               		rcost=rcost+ud*1500;
                  	cout<<"\t\t"<<ud<<" Ultra Deluxe Room/Rooms have been alloted to you for next 24 hours."<<endl;
            	}
           	else
       		{
           		cout<<"\t\tOnly "<<audrooms-sudrooms<<" Ultra Deluxe Rooms are remaining in the Hotel."<<endl;
            	}
			if(adrooms-sdrooms>=d)
            		{
                  		sdrooms=sdrooms+d;
                  		rcost=rcost+d*1200;
                  		cout<<"\t\t"<<d<<" Deluxe Room/Rooms have been alloted to you for next 24 hours."<<endl;
            		}
            		else
            		{
            		    cout<<"\t\tOnly "<<adrooms-sdrooms<<" Deluxe Rooms are remaining in the Hotel."<<endl;
            		}		
		}
};
class Menu
{
    public:
           //const string s[6]={"Pasta","Biryani","Soup","Dessert","Shake","Cake"};
           int tpasta_cost,pasta_cost,pasta,spasta,qpasta;
           int tbiryani_cost,biryani_cost,biryani,sbiryani,qbiryani;
           int tsoup_cost,soup_cost,soup,ssoup,qsoup;
           int tdessert_cost,dessert_cost,dessert,sdessert,qdessert;
           int tshake_cost,shake_cost,shake,sshake,qshake;
           int tcake_cost,cake_cost,cake,scake,qcake;
    Menu()
    {
		tpasta_cost=0;
		tbiryani_cost=0;
		tsoup_cost=0;
		tdessert_cost=0;
		tshake_cost=0;
		tcake_cost=0;
		spasta=0;
		sbiryani=0;
		ssoup=0;
		sdessert=0;
		sshake=0;
		scake=0;
        pasta_cost=120;
        biryani_cost=150;
        soup_cost=60;
        dessert_cost=90;
        shake_cost=100;
        cake_cost=400;
        pasta=50;
        biryani=20;
        soup=20;
        dessert=40;
        shake=30;
        cake=10;
    }
        void menudisplay(int sh)
        {
        	switch(sh)
        	{
        		case 1:
        			cout<<"Enter the number of pasta quantities: "<<endl;
        			cin>>qpasta;
        			if(pasta-spasta>=qpasta)
            	{
                  spasta=spasta+qpasta;
                  tpasta_cost=tpasta_cost+qpasta*pasta_cost;
                  cout<<"\t\t"<<qpasta<<" Pastas are ordered and will be served in 30 minutes."<<endl;
            	}
            	else
            	{
            	    cout<<"\t\tOnly "<<pasta-spasta<<" Pastas are remaining in the Hotel."<<endl;
            	}
            	break;
            	case 2:
            		cout<<"Enter the number of biryani quantities: "<<endl;
        			cin>>qbiryani;
        			if(biryani-sbiryani>=qbiryani)
            	{
                  sbiryani=sbiryani+qbiryani;
                  tbiryani_cost=tbiryani_cost+qbiryani*biryani_cost;
                  cout<<"\t\t"<<qbiryani<<" Biryanis are ordered and will be served in 30 minutes."<<endl;
            	}
            	else
            	{
            	    cout<<"\t\tOnly "<<biryani-sbiryani<<" Biryanis are remaining in the Hotel."<<endl;
            	}
            	break;
            	case 3:
            		cout<<"Enter the number of Soup quantities: "<<endl;
        			cin>>qsoup;
        			if(soup-ssoup>=qsoup)
            	{
                  ssoup=ssoup+qsoup;
                  tsoup_cost=tsoup_cost+qsoup*soup_cost;
                  cout<<"\t\t"<<qsoup<<" Soups are ordered and will be served in 30 minutes."<<endl;
            	}
            	else
            	{
            	    cout<<"\t\tOnly "<<soup-ssoup<<" Soups are remaining in the Hotel."<<endl;
            	}
            	break;
            	case 4:
				cout<<"Enter the number of dessert quantities: "<<endl;
        			cin>>qdessert;
        			if(dessert-sdessert>=qdessert)
            	{
                  dessert=sdessert+qdessert;
                  tdessert_cost=tdessert_cost+qdessert*dessert_cost;
                  cout<<"\t\t"<<qdessert<<" Desserts are ordered and will be served in 30 minutes."<<endl;
            	}
            	else
            	{
            	    cout<<"\t\tOnly "<<dessert-sdessert<<" Desserts are remaining in the Hotel."<<endl;
            	}
            	break;	
            	case 5:
            		cout<<"Enter the number of shake quantities: "<<endl;
        			cin>>qshake;
        			if(shake-sshake>=qshake)
            	{
                  sshake=sshake+qshake;
                  tshake_cost=tshake_cost+qshake*shake_cost;
                  cout<<"\t\t"<<qshake<<" Shakes are ordered and will be served in 30 minutes."<<endl;
            	}
            	else
            	{
            	    cout<<"\t\tOnly "<<shake-sshake<<" Shakes are remaining in the Hotel."<<endl;
            	}
            	break;
            	case 6:
            		cout<<"Enter the number of cake quantities: "<<endl;
        			cin>>qcake;
        			if(cake-scake>=qcake)
            	{
                  scake=scake+qcake;
                  tcake_cost=tcake_cost+qcake*cake_cost;
                  cout<<"\t\t"<<qcake<<" Cakes are ordered and will be served in 30 minutes."<<endl;
            	}
            	else
            	{
            	    cout<<"\t\tOnly "<<cake-scake<<" Cakes are remaining in the Hotel."<<endl;
            	}
            	break;
            	default:
            		cout<<"Please enter valid number"<<endl;
            		break;
			}
		}
        
      
    
};
class Payment:public Menu,public Management_of_Rooms
{
    public:
        int total_gain;
        Payment()
        {
            total_gain=0;
        }
        void pay()
        {
             total_gain=rcost+tpasta_cost+tbiryani_cost+tsoup_cost+tdessert_cost+tshake_cost+tcake_cost;
             cout<<"Outstanding amount: "<<total_gain;
        }
};
class Customer
{
    public:
        string name;
        long int phone_no;
};
int main()
{
	cout<<"********************************************************************************************************"<<endl;
	cout<<"\t\t**********************************************************************\t\t\t\t\t\t"<<endl;
	cout<<"\n";
	cout << "HH      HH    UU      UU    GGGGGG           AAAA         HH    HH    OOOOOO    TTTTTTTTT   EEEEEEE     LL         " << endl;
    cout << "HH      HH    UU      UU   GG    GG         AAAAAA        HH    HH   OO    OO      TTT      EE          LL         " << endl;
    cout << "HHHHHHHHHH    UU      UU   GG              AA   AA        HHHHHHHH   OO    OO      TTT      EEEE        LL         " << endl;
    cout << "HH      HH    UU      UU   GG   GGGG      AAAAAAAAA       HH    HH   OO    OO      TTT      EE          LL         " << endl;
    cout << "HH      HH     UUUUUUUU     GGGGGGGG      AA     AA       HH    HH    OOOOOO       TTT      EEEEEEE     LLLLLL     " << endl;
    cout<<"\n";
	cout<<"\t\t**********************************************************************\t\t\t\t\t\t"<<endl;
	cout<<"********************************************************************************************************"<<endl;
    Customer O[100];
    Payment o;
    static int i=0;
    int choice;
    m:
    	cout<<"\n\n\n";
    cout<<"If choice is 1 Entering details of Customer"<<endl;
    cout<<"If choice is 2 To book availabe rooms"<<endl;
    cout<<"If choice is 3 To book multiple types of available rooms"<<endl;
    cout<<"If choice is 4 Menu displayed and ordering"<<endl;
    cout<<"If choice is 5 Bill to pay"<<endl;
    cout<<"If choice is 6 Information regarding sales and collection"<<endl;
    cout<<"If choice is invalid"<<endl;
    cout<<"Please enter the choice:"<<endl;
    cin>>choice;
    switch(choice)
    {
    	case 1:cout<<"Enter the name of the Customer:";
               cin>>O[i].name;
            cout<<"Enter the phone number of the Customer:";
            cin>>O[i].phone_no;
            i++;
            break;
        case 2:cout<<"Enter Number of rooms required:";
        	cin>>o.quant;
       		cout<<"Choose the room type:"<<endl;
        	cout<<"\t\t 1.Premium Rooms(A/C)(4 Beds) - 1800/-"<<endl;
        	cout<<"\t\t 2.Ultra Deluxe Rooms(A/C)(3 Beds) - 1500/-"<<endl;
        	cout<<"\t\t 3.Deluxe Rooms(2 Beds) - 1200/-"<<endl;
        	cin>>o.rt;
               o.display();
               break;
        case 3:
        	cout<<"Enter Number of Premium rooms required: "<<endl;
        	cin>>o.qp;
        	cout<<"Enter Number of Ultra Deluxe rooms required: "<<endl;
        	cin>>o.qu;
        	cout<<"Enter Number of Deluxe rooms required: "<<endl;
        	cin>>o.qd;
        	o.display2(o.qp,o.qu,o.qd);
        	break;
        case 4:int choose;
              cout<<"1.To order Pasta - 120/-"<<endl;
              cout<<"2.To order Biryani - 150/-"<<endl;
              cout<<"3.To order Soup - 60/-"<<endl;
              cout<<"4.To order Dessert - 90/-"<<endl;
              cout<<"5.To order Shake - 100/-"<<endl;
              cout<<"6.To order Cake(1 KG) - 400/-"<<endl;
              cin>>choose;
              o.menudisplay(choose);
               break;
        case 5:o.pay();
              break;
		case 6:
			cout<<"Number of Premium Rooms available: "<<o.aprooms-o.sprooms<<endl;
			cout<<"Number of Ultra Deluxe Rooms available: "<<o.audrooms-o.sudrooms<<endl;
			cout<<"Number of Deluxe Rooms available: "<<o.adrooms-o.sdrooms<<endl;
			cout<<"\n";
			cout<<"Number of Premium Rooms booked: "<<o.sprooms<<endl;
			cout<<"Number of Ultra Deluxe Rooms booked: "<<o.sudrooms<<endl;
			cout<<"Number of Deluxe Rooms booked: "<<o.sdrooms<<endl;
			cout<<"\n";
			cout<<"Revenue generated by room rent: "<<o.rcost<<endl;
			cout<<"\n\n\n";
			cout<<"Remaining Pastas: "<<o.pasta-o.spasta<<endl;
			cout<<"Number of Pastas ordered: "<<o.spasta<<endl;
			cout<<"Revenue generated by solding Pastas: "<<o.tpasta_cost<<endl;
			cout<<"\n\n\n";
			cout<<"Remaining Biryanis: "<<o.biryani-o.sbiryani<<endl;
			cout<<"Number of Biryanis ordered: "<<o.sbiryani<<endl;
			cout<<"Revenue generated by solding Biryanis: "<<o.tbiryani_cost<<endl;
			cout<<"\n\n\n";			
			cout<<"Remaining Soups: "<<o.soup-o.ssoup<<endl;
			cout<<"Number of Soups ordered: "<<o.ssoup<<endl;
			cout<<"Revenue generated by solding Soups: "<<o.tsoup_cost<<endl;
			cout<<"\n\n\n";			
			cout<<"Remaining Desserts: "<<o.dessert-o.sdessert<<endl;
			cout<<"Number of Desserts ordered: "<<o.sdessert<<endl;
			cout<<"Revenue generated by solding Desserts: "<<o.tdessert_cost<<endl;
			cout<<"\n\n\n";
			cout<<"Remaining Shakes: "<<o.shake-o.sshake<<endl;
			cout<<"Number of Shakes ordered: "<<o.sshake<<endl;
			cout<<"Revenue generated by solding Shakes: "<<o.tshake_cost<<endl;
			cout<<"\n\n\n";
			cout<<"Remaining Cakes: "<<o.cake-o.scake<<endl;
			cout<<"Number of Cakes ordered: "<<o.scake<<endl;
			cout<<"Revenue generated by solding Cakes: "<<o.tcake_cost<<endl;
			cout<<"\n\n\n";
			cout<<"Total amount collected: "<<o.total_gain<<endl;									
        case 7:
		exit(0);
		default:
		cout<<"Invalid Choice";     
    }
    goto m;
    return 0;
}
