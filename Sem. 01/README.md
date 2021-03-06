

##  Структури

Структурите в C++ се използват за групиране на елементи. Елементите, наричани още членове, могат да бъдат от различен тип и с различна дължина.
 ```c++
struct Box
{
	int height;
	int weight;
}
 ```

###  Деклариране на обекти от новия тип
 ```c++
Box b; //default values to height and weight

Box b2 = {3, 4} // height = 3, weight = 3;

Box b3;
b3.height = 13;
b3.weight = 14;
 ```
	
###  Подаване във функции
Ако няма да променяме обекта го подаваме по **константна референция.**
 ```c++
void calculcateArea(const Box& b)
{
    return b.height * b.weight;
}
```
   Може и само по **референция**, но тогава промените ще се отразят върху подадения аргумент.
   
 ```c++
void readBox(Box& b)
{
    cin >> b.height >> b.weight;
}
 ```
Може и да го подаваме по **копие**.
 ```c++
Box revertBox(Box b)
{
    int temp = b.height;
    b.height = b.weight;
    b.weight = temp;

    return b;
}
```
### Задачи

**Задача 1:** Въвежда се цяло число **N**  и после **N** тригъгълника в равнината, определени от 3 точки ( 6 координати).
Отпечатайте тригълниците **сортирани по лицата им.**
