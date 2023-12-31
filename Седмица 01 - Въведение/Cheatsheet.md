## СКЕЛЕТ НА ПРОГРАМА
```c++
#include <iostream>
//using namespace std;

int main() {
std::cout << "I <3 FMI";
return 0;
}
```

---
## ВХОД И ИЗХОД
### **cout <<**
Извеждане в конзолата:
```c++
cout << "This is C++ Programming";

cout<<"\n"; //нов ред
cout<<"\t"; //таб
cout<<"\\"; //добавя "\"
cout<<"\'"; //добавя "'"
cout<<"\0"; //null character
```
### **cin >>**
Приема потребителски вход от конзолата:
```c++
cin >> variable_name;
```

---
## ТИПОВЕ ПРОМЕНЛИВИ
### **char** - един символ
```c++
char variable;
```
### **int** - цяло число
```c++
int variable;
```
### **float** - число с плаваща стойност - единична точност
```c++
float variable;
```
### **double** - число с плаваща стойност - двойна точност
```c++
double variable;
```
### **boolean** - 0 or 1 / FALSE or TRUE
```c++
bool variable;
```
### **void** - липса на тип

## КОМЕНТАРИ
### КОМЕНТАРИ НА ЕДИН РЕД
```c++
// ТОВА Е ЗАКОМЕНТИРАН РЕД
```
### КОМЕНТАРИ НА ПОВЕЧЕ РЕДОВЕ
```c++
/*
ЗАКОМЕНТИРАНИ
СА 
НЯКОЛКО
РЕДА
*/
```

---
## МАТЕМАТИКА !!!
### **max(<число1>, <число2>)**
Връща по-голямото от двете числа.
```c++
cout << max(1, 100); // 100
```
### **min(<число1>, <число2>)**
Връща по-малкото от двете числа.
```c++
cout << min(1, 100); // 1
```
### **sqrt(<число>)**
Връща корен от числото.
```c++
#include <cmath>

cout << sqrt(169); // 13
```
### **ceil(<число>)**
Закръгляне към най-близко цяло число НАГОРЕ (ceiling = таван)
```c++
double a = ceil(1.0001); // 2
```
### **floor(<число>)**
Закръгляне към най-близко цяло число НАДОЛУ (floor = под)
```c++
double a = floor(1.99); // 1
```
### **pow(<число1>, <число2>)**
число1 НА СТЕПЕН число2
```c++
int a = pow(x, y);
```

---
## УСЛОВНИ ОПЕРАТОРИ
### **If** - АКО НЕЩО СИ, ТО НЕЩО СИ
```c++
if (<УСЛОВИЕ>) {
    // ИЗПЪЛНЯВАМЕ ПРИ ПРАВИЛНО <УСЛОВИЕ> 
    // ПРАВИЛНО = true
}
```
### **If-else** - АКО НЕЩО СИ, ТО НЕЩО СИ... АКО НЕ - ДРУГОТО
```c++
if (<УСЛОВИЕ>) {
    // ИЗПЪЛНЯВАМЕ ПРИ ПРАВИЛНО <УСЛОВИЕ>
} else {
    // ИЗПЪЛНЯВАМЕ ПРИ ГРЕШНО <УСЛОВИЕ>
}
```
### **If-else if** - ПОСЛЕДОВАТЕЛНА ПРОВЕРКА
```c++
if (<УСЛОВИЕ1>) {
    // ИЗПЪЛНЯВАМЕ ПРИ ПРАВИЛНО <УСЛОВИЕ1>
} else if (<УСЛОВИЕ2>){
    // ИЗПЪЛНЯВАМЕ ПРИ ПРАВИЛНО <УСЛОВИЕ2>
} else {
    // ИЗПЪЛНЯВАМЕ ПРИ ГРЕШНО <УСЛОВИЕ1> И <УСЛОВИЕ2>
}
```
### Тернален оператор
```c++
variable = (condition) ? expressionTrue : expressionFalse;
```
### **switch-case** - СПИСЪК ОТ УСЛОВИЯ
```c++
switch (<НЕЩО ЗА СРАВНЯВАНЕ>) 
{
case <ОПЦИЯ1>: 
    // ИЗПЪЛНЯВАМЕ ПРИ УСПЕШНО СРАВНЯВАНЕ С <ОПЦИЯ1>
break;
case <ОПЦИЯ2>: 
    // ИЗПЪЛНЯВАМЕ ПРИ УСПЕШНО СРАВНЯВАНЕ С <ОПЦИЯ2>
break;
...
default: 
    // ИЗПЪЛНЯВАМЕ ПРИ НЕУСПЕШНО СРАВНЯВАНЕ С ВСИЧКИ ГОРЕПОСОЧЕНИ ОПЦИИ
}
```

---
## ЦИКЛИЧНИ ОПЕРАТОРИ
### **while** Loop - докато условие = върти
Изпълнява вътрешния за него блок от код, докато условието е изпълнено.
```c++
while (<УСЛОВИЕ>)
{
    // ИЗПЪЛНЯВА СЕ ПРИ ИЗПЪЛНЕНО <УСЛОВИЕ>
}
```
### **do-while** ... while but with extra steps
Изпълнява се подобно на while, но ВИНАГИ се изпълнява **ПОНЕ ВЕДНЪЖ**.
```c++
do
{
    // ИЗПЪЛНЯВА СЕ ПОНЕ ВЕДНЪЖ И ПРИ ИЗПЪЛНЕНО <УСЛОВИЕ> ЗАПОЧВА ДА СЕ ИЗПЪЛНЯВА ОТНОВО
} while (<УСЛОВИЕ>);
```

### **for**
Използва се за итерация - най-често при обхождане на структури от данни (масиви и списъци).

инициализация = извършва се при началото на изпълнение на цикъла.
условие = до кога се изпълнява.
обновяване = какво се случва в края на всеки цикъл.
```c++
// for(инициализация; условие; обновяване)
for (int i = 0 ; i < count; i++)
{
    // ИЗПЪЛНЯВАЩ СЕ КОД
}
```
### **break**
Използва се за прекъсване на цикъл;
```c++
break;
```

## ЛОГИЧЕСКИ ОПЕРАТОРИ ТАБЛИЦА
| A | !A | B | !B | A\|\|B | A&&B |
|---|----|---|----|--------|------|
| 0 | 1  | 0 | 1  | 0      | 0    |
| 1 | 0  | 0 | 1  | 1      | 0    |
| 0 | 1  | 1 | 0  | 1      | 0    |
| 1 | 0  | 1 | 0  | 1      | 1    |