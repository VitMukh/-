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

Лабораторна робота 6
Ієрархія класів
Варіант 12

Контрольні питання
1. У чому полягає принцип спадкування?
Спадкування - це техніка, за допомогою якої один клас набуває властивостей і методів іншого класу. Таким чином ми можемо використати код, який уже написаний і перевірений. 
Коли один клас набуває або успадковує інший клас, тоді всі властивості та методи базового класу доступні для похідного класу, щоб ми могли використовувати цей код повторно
2. Як називається клaс, який yспaдкoвyється?
Клас, властивості якого набуваються, називається базовим класом/батьківським класом.
3. Як називається клaс, який yспaдкoвyє?
Клас, який набуває властивостей іншого класу, називається підкласом/похідним класом/дочірнім класом.
4. Наведіть приклади бaгaтopiвнeвої iєpapxiї клaсiв
5. Для чого використовується спeцифiкaтop protected?
Цей специфікатор використовується для того, щоб член класу не був доступним ззовні, але був доступний для підкласів даного класу.


6. Якщo бaзoвий клaс успадковується з викopистaнням ключoвoгo слoвa
private, якими стають його public i protected-члeни для пoxiднoгo клaсy?
Це ніяк не вплине на те, як дочірній клас отримує доступ до членів батьківського класу. Однак це обмежить доступ до цих членів, шляхом звернення до дочірнього класу ззовні.
7. Що таке мнoжиннe спадкування?
Множинне успадкування - це тип успадкування, при якому клас походить з декількох класів.


Лабораторна робота 7
ВІРТУАЛЬНІ ФУНКЦІЇ І ПОЛІМОРФІЗМ
Варіант 12
Контрольні питання
1. Наведіть приклади поліморфізму з повсякденного життя.
Приклад – використання предметів не лише для одної операції. В чашці можна крім води заварювати чай, або розігрівати суп.
2. Чи може конструктор бути віртуальним?
Так. Ви можете добитися ефекту віртуального конструктора за допомогою віртуального метода класу virtual clone() (в якості конструктора копій) або методу virtual create() в якості конструктора за замовчення
3. Чи може деструктор бути віртуальним?
Так. Деструктори не успадковуються, але можуть бути віртуальними.
4. Який клас називається абстрактним?
Абстрактні класи реалізують один з принципів ООП – поліморфізм. В абстрактному класі можна описати абстрактні методи та властивості. Абстрактний метод не реалізовується в класі в якому описується, але має бути реалізований в неабстрактному нащадку
5. Коли клас називають поліморфним?
Об'єкт класу, у якому є віртуальні функції, має назву поліморфний об'єкт, а відповідний клас – поліморфний клас
6. Чи можна створити об’єкт (екземпляр) абстрактного класу?
Ні. В абстрактному класі можна описати абстрактні методи та властивості.
7. Чи можна створити вказівник на об’єкт (екземпляр) абстрактного класу?
Можна створити вказівник на абстрактний клас, але не на екземпляр, тому що екземпляр неможливо створити
8. Дайте визначення чисто віртуальної функції
virtual const char* math() {}

Лабораторна робота 9
Створення консольних додатків С#
Контрольні питання:
1)Наведіть узагальнений синтаксис оголошення змінної мовою C#.
Int k;
2)Наведіть узагальнений синтаксис ініціалізації змінної на мові C#.
Int k = 5;
3)Дайте означення типу даних.
Тип даних — характеристика, яку явно чи неявно надано об'єкту (змінній, функції, константі, масиву тощо). Тип даних визначає множину припустимих значень, формат їхнього збереження, розмір виділеної пам'яті та набір операцій, які можна робити над даними.
4)          На які два різновиди поділяють усі типи у мові C#?
Прості (цілочисленні, символьні, тд.) та складні (покажчики, строки, списки)
5)Які типи належать до типів посилань?
Object, string
6)Назвіть та опишіть прості типи мови C#.
Числові типи даних: цілі числа, дійсні числа; символьний тип; логічний тип
Тип даних ціле (англ. integer) не може зберігати дробову частину числа. Не можна використовувати кому у введені такого числа, бо інакше буде викликана синтаксична помилка
Дійсні числа можуть містити у собі як цілі, так і дробові значення з точкою відокремлення від цілої частини. 
Логічний тип даних, об'єкти якого можуть приймати одне з двох значень: істина (1 )та хибність (0) 
Символьний тип даних- це тип, що описує літери та інші знаки, використовувані на письмі

