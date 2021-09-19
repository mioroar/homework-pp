# homework-pp
домашка пп номер 1
Задание «Имя». Написать программу, которая выводит на экран Ваше имя

#include <iostream>

using namespace std;
int main()
{
    char name[256];
    setlocale(0,"");
    cout << "Введи свое имя" << endl;
    cin >> name;
    cout << "Вау, твое имя - " << name << endl;

}


Задание «Арифметика». Ввести с клавиатуры два числа и найти их сумму, разность, произведение и, если
возможно, частное от деления одного на другое.

using namespace std;
int main()
{
    float a,b;
    setlocale(0,"");
    cout<<"Введи а"<<endl;
    cin>> a;
    cout<<"Введи б"<<endl;
    cin>> b;
    cout<< "Сумма будет "<< a + b<<endl;
    cout<< "Разность будет "<< a - b<<endl;
    cout<< "Произведение будет "<< a * b<<endl;
    if (b!=0){
        cout<< "Частное будет "<< a / b<<endl;
    }
    else{
        cout<< "Частного не будет "<<endl;
    }
}


Задание «Уравнение». Для любых введенных с клавиатуры b и c решить уравнение вида bx + c = 0.

#include <iostream>

using namespace std;
int main()
{
    float b,c;
    setlocale(0,"");
    cout <<"Введи b" <<endl;
    cin >> b;
    cout <<"Введи c" <<endl;
    cin >> c;
    if (b==0){
        cout<<"А все икса нет,решения тоже, не вводи 0" <<endl;
    
    }
    else{
        if (c!=0) {
            cout<<"Решение уравнения: x = "<< -1*c / b<< endl;
        }
        else{
            cout<<"Решение уравнения: x = "<< 1/b << endl;
        }
    }
}


Задание «Еще уравнение». Для любых введенных с клавиатуры a, b и c решить уравнение вида
ax^2 + bx + c = 0.

#include <iostream>
#include <cmath>
 
using namespace std;
 
int main() { 
  double a, b, c,d;
  cout << "Введи a" << endl;
  cin >> a;
  cout << "Введи b" << endl;
  cin >> b;
  cout << "Введи c" << endl;
  cin >> c;
  d = sqrt(b*b - 4 * a * c);
  if (a == 0) {
      if (b == 0) {
          cout << "Нет решений.";
      } else {
          if (c == 0) {
              cout << "X = " << 0 <<endl;
          } else {
              cout << "X = " << -c / b <<endl;
          }
      }
  } else {
      if (b == 0) {
          if (c == 0) {
              cout << "X = " << 0 <<endl;
              }
          } else {
              if (-c / a > 0) {
                  cout << "X = " << sqrt(-c / a) <<endl;
              } else {
                   cout << "Нет решений";
              }
          }
      } else {
          if (c == 0) {
              cout<< "X1 = 0." << endl << "X2 = " << -b/a <<endl;
          } else {
              if (b * b - 4 * a * c > 0) {
                  cout << "X1 = " << (-b + d) / (2 * a) << endl << "X2 = " << (-b - d) / (2 * a) <<endl;
              } else if (d == 0) {
                  cout << "X = " << -b / (2 * a) <<endl;
              } else {
                  cout << "Нет решений";
              }
          }
      }
  }
}


Задание «Лампа со шторой». В комнате светло, если на улице день и раздвинуты шторы или если включена
лампа. Ваша программа должна, в зависимости от времени суток и состояния лампы и штор, отвечать на вопрос, светло
ли в комнате.


#include <iostream>
using namespace std;
 
int main() { 
  bool day, shtora, lamp;
  cout << "Ответы 1-да или 0-нет" << endl;
  cout << "Сейчас день?" << endl;
  cin >> day;
  cout << "Шторы закрыты?" << endl;
  cin >> shtora;
  cout << "Лампа горит?" << endl;
  cin >> lamp;
  if ((day + shtora == 2) || lamp == 1) {
      cout << "Светло";
  } else {
      cout << "темно как в пещере";
  }
}
