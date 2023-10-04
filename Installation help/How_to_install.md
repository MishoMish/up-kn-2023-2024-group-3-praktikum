# Как да инсталираме VS Code и компилатор за C++ на Windows

## 1) Изтеглете Visual Studio Code от този [линк](https://code.visualstudio.com/download)

## 2) Инсталирайте extension-a за C/C++

След като инсталирате и отворите VS Code в панела Extension View (Ctrl + Shift + X) потърсете 'c++' и инсталирайте 'C/C++' by Microsoft (препоръчително е да инсталирате и 'C/C++ Extension Pack')

![Image](https://code.visualstudio.com/assets/docs/cpp/cpp/cpp-extension.png)

## 3) Инсталирайте Mingw-w64 компилаторът за C++

Първо, инсталирайте MSYS2 от този [линк](https://www.msys2.org/) и следвайте инструкциите от сайта, за да инсталирате Mingw-w64 компилатора. Не затваряйте терминала, отворен през MSYS2, след инсталацията.

## 4) Инсталирайте Mingw-w64 toolchain

В терминала отворен през MSYS2 изпълнете следната команда:
```bash
pacman -S --needed base-devel mingw-w64-x86_64-toolchain
```
Продължете с предложената конфигурация (default).

## 5) Добавете пътя към bin папката на Mingw-w64 към PATH променливата на вашата система

За да го направите, следвайте долните стъпки:
- В Windows search bar-a потърсете: 'Edit environment variables for your account'
- Натиснете на 'Environment Variables...'
- Изберете Path variable във вашите System variables и натиснете Edit
- Натиснете New и добавете пътя към папката, в която инсталирахте Mingw-w64. По подразбиране пътят е: C:\msys64\mingw64\bin
- Натиснете OK, за да запазите промените. Затворете и отворете наново всички терминали, ако имате отворени. 

## 6) Проверете дали инсталацията е била успешна

За да проверите дали инсталацията е била успешна, отворете нов терминал и напишете тези 3 команди:

```bash
gcc --version

g++ --version

gdb --version
```

- Ако резултата на всяка от тях е версията на конкретния ресурс, то всичко е било успешно.
- Ако не получавате очаквания резултат проверете отново PATH променливата на вашата система. Ако имате проблем само с gdb (това е дебъгера), отворете терминал през MSYS2 и напишете следната команда:
```bash
pacman -S mingw-w64-x86_64-gdb
```

## 7) Как да компилирате и изпълните .cpp файл

За да компилирате и изпълните вашия .cpp файл, отворете терминал през VS Code (Ctrl + /) и напишете:
```bash
g++ {name_of_your_file}.cpp -o {exe_name}.exe && {exe_name}.exe
```
Командата се състои от 2 части, разделени от &&. Първата част компилира файла и създава изпълним файл с името, което му подадете. Втората част изпълнява файла (тази част може да се различа в зависимост от терминала: понякога трябва пред името на файла да сложите './'). Ако не получавате правилен резултат изпълнете двете части поотделно.

## КОПИРАНО ОТ [линк](https://github.com/fmi-lab/up-kn-2023-2024-group-3-seminar)