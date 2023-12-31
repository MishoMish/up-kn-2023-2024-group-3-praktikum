# **ТЕОРИЯ**
---
# *ЩО Е КОМПЮТЪР И ЩО Е ПРОГРАМА?*

## 1) Компютър: 
Устройство, което може да бъде програмирано да извършва последователност от аритметични и логически операции.

## 2) Програма:
Списък от инструкции отправени към компютъра, които трябва да дадат определен изходен резултат. Четима от човека част се нарича source code, от който програмите се компилират, дава възможност за изследване протичането на програмата.

---
## 3) Компилатор:
Програма, превеждаща даден изходен код (програма) до език от по-ниско ниво (машинен или асемблерен език). Компилираният код може да се изпълни на нашия компютър. Има две основни фази при създаване на кода: аналитична и синтезираща.

> *Аналитична*: 
Програмата се разбива на токени (ключови думи, идентификатори и оператори). Проверява се дали граматиката на езика е спазена (използва се
дървовидна структура). Проверява се дали токените са логически свързани помежду си (примерно дали променлива е дефинирана преди да бъде използвана).

> *Синтезираща*:
Създава се междинен код. Всичко се оптимизира (бързината или използването на оперативна памет се подобрява). Превежда се дървовидната структура,
ако всичко е минало успешно.

## 4) Интерпретатор: 
Програма, изпълняваща друга програма. Извършва се последователен анализ на командите от програмата ни, превежда се на машинен език и се изпълнява, тоест не превежда целия код само веднъж, както при компилатора, а при всяко извикване на програмата ни. Работи по-бавно от компилатора.

**Разлики между двете - при използване на *компилатор*, при всяка промяна в кода трябва да изчакаме *компилатора* да транслира всички файлове и да ги свърже. *Интерпретаторът* превежда само променената част от кода, което изисква значително по-малко време. Вече компилиран код се нуждае от по-малко време за стартиране, отколкото интерпретирането му, тоест *интерпретаторът* трябва отново да анализира всичко, докато компилираният код само изпълнява логическите операции в последователност.**

## 5) Азбука:
Крайна редица от допустими символи, с помощта на които се постигат основните конструкции на езика.

## 5) Синтаксис: 
Множество от правила, които определят образуването на основните конструкции на езика на база на азбуката му. Не всяка редица от символи е програма.

## 5) Семантика:
Правила, които определят как се изпълнява програмата в даден език за програмиране.

---
# *Нашата първа програма на C++!*

## Променливи и примитивни типове:

### Примитивни типове - примери:
> Целочислен тип (**int, short, long** ..)
> Числа с плаваща запетая (**double, float** ..)
> Булев тип (**bool**)
> Символен тип (**char**)

```c++
    int i;
    double d;
    bool b;
    char c;
```

### Инициализиране на променлива:
```c++
    int numberOfItems = 1;
    double pi = 3.14;
    bool isTrue = false;
    char gender = 'm';
```

## Присвояване на стойност:
```c++
    int something;
    something = 100;
```

## Въвеждане на променлива от стандартния вход:
```c++
    int initMe;
    std::cin >> initMe;
```

## Извеждане на променлива на стандартния изход:
```c++
    int printMe = 123;
    std::cout << printMe;
```

## Преобразуване на типове:
> Без загуба на информация:
 - **int -> double**
 - **bool -> int**

> Със загуба на информация:
 - **double -> int**
 - **int -> bool**

## Оператори.

- **Аритметични оператори**:
+, -, *, /, %, ++, - -,
- **Оператори за сравнение** (връщат bool):
==, <, >, <=, >=, !=
- **Оператори за присвояване**:
=, +=, -=, /=, *=, %=, &=, |= 
- **Логически оператори**:
&&, ||, !

| A | !A | B | !B | A\|\|B | A&&B |
|---|----|---|----|--------|------|
| 0 | 1  | 0 | 1  | 0      | 0    |
| 1 | 0  | 0 | 1  | 1      | 0    |
| 0 | 1  | 1 | 0  | 1      | 0    |
| 1 | 0  | 1 | 0  | 1      | 1    |