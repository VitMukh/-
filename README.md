Лабораторна ном. 1 «КЛАСИ І ОБ'ЄКТИ В С++». Відповіді на запитання
1. Навести приклад опису класу, визначення об’єкта.
Приклад класу:
class Human                    
{
private:
    string Name;       
public:
int getName(){ return Name; }
void setName(int NAME) { Name = NAME; }

Приклад визначення об’єкта:
   Human El_Human;
   Human El_Kolya (“Mykola”) 

2. Чи обов’язково в описі класу повинні міститись конструктор і
деструктор?
Ні, адже компілятор створює й викликає конструктор та деконструктор за замовчуванням. Але цим варто користуватися лише в простих класах та програмах.
3. Скільки може бути в класі конструкторів і деструкторів?
Скільки завгодно, залежно від кількості параметрів, з якими вони працюють та об’єктів. 
4. Коли викликається конструктор і деструктор?
При ініціалізації та знищенні об’єкту. 
5. Що таке конструктор за замовчуванням?
Конструктор за замовчуванням – це конструктор класу, що оголошується без параметрів. Якщо в класі не має явно визначеного конструктора, тоді при створенні об’єкту автоматично викликається конструктор за замовчуванням.

ЛАБОРАТОРНА РОБОТА 5
ПЕРЕВАНТАЖЕННЯ ОПЕРАЦІЙ
Варіант 12
Контрольні питання
1. Як можна викликати операцію-функцію?
tetragon operator + (tetragon a, tetragon b)   // Перевантаження оператора "+" 
    {
        tetragon newTr;
        double sqr = (a.edge * a.edge) + (b.edge * b.edge);
        newTr.edge = sqrt(sqr);
        return newTr;
    }

2. Чи можна змінити кількість операндів перевантаженої операції?
Не можна змінити кількість операндів перевантаженого оператора. Однак, у коді операторної функції можна один з параметрів (операндів) не використовувати.

3. Чи всі оператори мови С ++ можуть бути перевантажені?
Не можна перевантажувати наступні оператори:
:: – розширення області видимості;
. (крапка) – вибір члена класу або структури;
* – доступ за покажчиком;
?: – тернарний оператор ?:.

4. Якими двома різними способами визначаються перевантажені операції?
Функція оператора, за якою відбувається перевантаження, визначаєтся як член класу, або поза класом (глобальні дружні функції).
5. Чи всі операції можна перевантажити за допомогою глобальної
дружньої функції?
Ні. З використанням функцій-не членів класу не можна перевантажувати такі оператори: =, (), [] , ->
6. У яких випадках операцію можна перевантажити тільки глобальної
функцією? 
У випадку, коли для бінарного оператору повинно бути два операнда.
7. У яких випадках глобальна операція-функція повинна бути дружньою?
Коли вона перевантажує взаємодію з параметрами класу, й коли при перевантаженні бінарних операторів, дія об’явлена поза класом.

