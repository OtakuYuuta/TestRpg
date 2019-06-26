 #include <iostream>
#include <stdlib.h>
#include <cctype>
#include <string>
using namespace std;

char name [100];
void startmenu();
void fighter_type();
void fighter_warior();
void fighter_mage();
void round_onemage();
void round_onewarrior();
void enemymage();
void enemywarrior();
struct warrior;
struct mage;

int main(){
	startmenu();
	fighter_type();
	system ("pause>0");
	return 0;
}


	int hp = 100; //stat ng mage
	int atk = 80;


struct warrior{ //stat ng warrior
	int hp = 200;
	int atk = 40;
}swar;

struct enemy_one{ //stat ng enemy one
	int hp = 300;
	int atk = 10;
}eone;


void enemywarrior(){
	system("cls");
	int action_choice;
	cout << "   ==============================   ============================== " << endl;
	cout << "   ==============================   ============================== " << endl;
	cout << "   =====       * * *        =====   =====       * * *        =====" << endl;
	cout << "   =====     * __   __*     =====   =====     * __   __*     =====" << endl;
	cout << "   =====   *   O     O  *   =====   =====   *   O     O  *   =====" << endl;
	cout << "   =====   *            *   =====   =====   *            *   =====" << endl;
	cout << "   =====   *     ___    *   =====   =====   *     ___    *   =====" << endl;
	cout << "   =====    *          *    =====   =====    *          *    =====" << endl;
	cout << "   =====       * * *        =====   =====       * * *        =====" << endl;
	cout << "   =====   TEMPORARY IMAGE  =====   =====   TEMPORARY IMAGE  =====" << endl;
	cout << "   =====       "<< name << "      =====         =====       Tempest      =====" << endl;
	cout << "   ==============================   ==============================" << endl;	
	cout << "   ==============================   ==============================" << endl;
	cout << "   ===          HP="<<swar.hp<<"        ===   ===          HP="<<eone.hp<<"        ===" << endl;
	cout << "   ===        Damage="<<swar.atk<<"       ===   ===        Damage="<<eone.atk<<"      " << endl;		 
	cout << "   ==============================   ==============================" << endl;	
	cout << "   ===       1. Attack        ===   ==============================" << endl;
	cout << "   ==============================   ==============================" << endl;
	cout << "   ==============================   ==============================" << endl;
    while (eone.hp != 0) {
        std::cin >> action_choice;

        switch (action_choice) {
        case 1:
            eone.hp -= swar.atk;
        }
            std::cout << "You have succesfully attack Tempest" << std::endl;
            break;
    }	
}

void enemymage(){
	system("cls");
	cout << "   ==============================   ============================== " << endl;
	cout << "   ==============================   ============================== " << endl;
	cout << "   =====       * * *        =====   =====       * * *        =====" << endl;
	cout << "   =====     * __   __*     =====   =====     * __   __*     =====" << endl;
	cout << "   =====   *   O     O  *   =====   =====   *   O     O  *   =====" << endl;
	cout << "   =====   *            *   =====   =====   *            *   =====" << endl;
	cout << "   =====   *     ___    *   =====   =====   *     ___    *   =====" << endl;
	cout << "   =====    *          *    =====   =====    *          *    =====" << endl;
	cout << "   =====       * * *        =====   =====       * * *        =====" << endl;
	cout << "   =====   TEMPORARY IMAGE  =====   =====   TEMPORARY IMAGE  =====" << endl;
	cout << "   =====       "<< name << "      =====	  	  =====       Tempest      =====" << endl;
	cout << "   ==============================   ==============================" << endl;	
	cout << "   ==============================   ==============================" << endl;
	cout << "   ===          HP="<<hp<<"        ===   ===          HP="<<eone.hp<<"        ===" << endl;
	cout << "   ===        Damage="<<atk<<"       ===   ===        Damage="<<eone.atk<<"   ===" << endl;		 
	cout << "   ==============================   ==============================" << endl;	
	cout << "   ===       1. Attack        ===   ==============================" << endl;
	cout << "   ==============================   ==============================" << endl;
	cout << "   ==============================   ==============================" << endl;
		int action_choice;
	  while (eone.hp != 0) {
        std::cin >> action_choice;

        switch (action_choice) {
        case 1:
            eone.hp -= atk;
			std::cout << "You have succesfully attack Tempest" << std::endl;
            break;
        }
            
    }	
}


void round_onemage(){
	system("cls");
	char answer;
	cout << "Are you ready for round one " << name << " or would like to change your fighetr? [y/n]";
	cin >> answer;
	if (answer == 'y' || answer == 'Y'){
	enemymage();
	}
	else if (answer == 'n' || answer == 'N'){
	fighter_type();
	}
	
}

void round_onewarrior(){
	system("cls");
	char answer;
	cout << "Are you ready for round one " << name << " or would like to change your fighetr? [y/n]";
	cin >> answer;
	if (answer == 'y' || answer == 'Y'){
	enemywarrior();
	}
	else if (answer == 'n' || answer == 'N'){
	fighter_type();
	}
	
}
void fighter_mage(){
	system("cls");
	char mage_choice;
	cout << "   ==============================   " << endl;
	cout << "   ==============================   " << endl;
	cout << "   =====       * * *        =====   " << endl;
	cout << "   =====     *        *     =====   " << endl;
	cout << "   =====   *   O     O  *   =====   " << endl;
	cout << "   =====   *   =     =  *   =====   " << endl;
	cout << "   =====   *      _     *   =====   " << endl;
	cout << "   =====    *          *    =====   " << endl;
	cout << "   =====       * * *        =====   " << endl;
	cout << "   =====   TEMPORARY IMAGE  =====   " << endl;
	cout << "   =====         MAGE       =====   " << endl;
	cout << "   ==============================   " << endl;	
	cout << "   ============ "<< name <<" =============   " << endl;  //<<<<< tanggalin na natin toh guysuuuu notis meh 
	cout << "   =========== HP="<<hp<<" ===========   " << endl;
	cout << "   ========= Damage="<<atk<<" ==========   " << endl;	
	cout << "   ==============================   " << endl;		//stats	 	 
	cout << "   ==============================   " << endl;	
	cout << "   ==============================   " << endl << endl;	
	char answer;
	cout << "Choose this type?[y/n]";
	cin >> answer;
	if (answer == 'n' || answer == 'N'){
	fighter_type();
	}
	else if (answer == 'y' || answer == 'Y'){
	round_onemage();
	}	
	else if (answer != 'y' || answer != 'n'){
	cout << "wrong input";
}
}
void fighter_warior(){
	system("cls");
	char warrior_choice;
	cout << "   ==============================   " << endl;
	cout << "   ==============================   " << endl;
	cout << "   =====       * * *        =====   " << endl;
	cout << "   =====     *        *     =====   " << endl;
	cout << "   =====   *   O     O  *   =====   " << endl;
	cout << "   =====   *   =     =  *   =====   " << endl;
	cout << "   =====   *      _     *   =====   " << endl;
	cout << "   =====    *          *    =====   " << endl;
	cout << "   =====       * * *        =====   " << endl;
	cout << "   =====   TEMPORARY IMAGE  =====   " << endl;
	cout << "   =====       WARRIOR      =====   " << endl;
	cout << "   ==============================   " << endl;	
	cout << "   =========== HP="<<swar.hp<<" ===========   " << endl;
	cout << "   ========= Damage="<<swar.atk<<" ==========   " << endl;	
	cout << "   ==============================   " << endl;		//stats	 	 << endl;	
	cout << "   ==============================   " << endl << endl;	
	char answer;
	cout << "Choose this type?[y/n]";
	cin >> answer;
	if (answer == 'y' || answer == 'Y'){
	round_onewarrior();;
	enemywarrior();
	}
	else if (answer == 'n' || answer == 'N'){
	fighter_type();
	}
		
}


void fighter_type(){
	system("cls");
	int fighter_choice;
	cout << "==================="<< endl;
	cout << "What class are you?"<< endl;
	cout << "1. Warrior"<< endl;
	cout << "2. Mage" << endl;
	cout << "==================="<< endl;
	cout << "  >> ";
	cin >> fighter_choice;
	if(fighter_choice == 1){
		fighter_warior();
	}else if(fighter_choice == 2){
		fighter_mage();
	}
	
}
void startmenu(){
	int menu_choice;
	cout << "   ==============================   " << endl;
	cout << "   ==============================   " << endl;
	cout << "   =====       * * *        =====   " << endl;
	cout << "   =====     *        *     =====   " << endl;
	cout << "   =====   *   O     O  *   =====   " << endl;
	cout << "   =====   *   ;     ;  *   =====   " << endl;
	cout << "   =====   *      _     *   =====   " << endl;
	cout << "   =====    *          *    =====   " << endl;
	cout << "   =====       * * *        =====   " << endl;
	cout << "   =====   CRYING MONSTER   =====   " << endl;
	cout << "   =====      THE GAME      =====   " << endl;
	cout << "   ==============================   " << endl;
	cout << "   ==============================   " << endl;	
	cout << "   =====         MENU       =====   " << endl;
	cout << "   =====    1.Start Game    =====   " << endl;
	cout << "   =====       2.Exit       =====   " << endl;
	cout << "   ==============================   " << endl;	
	cout << "   ==============================   " << endl;	
	cout << "             >> ";
	cin >> menu_choice;
	if (menu_choice == 1){
		cout << "Enter player name: ";
		cin >> name;
		cout << endl << "WELCOME " << name << "!";
		system ("pause>0");
	}else if (menu_choice == 2){
		exit(0);
	}else{
		system ("cls");
		startmenu();
	}
}
void yn_check(){
	cout << "to be filled";
}


