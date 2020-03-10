# Divergent Change

## Definition

Divergent change is the opposite of Shotgun Surgery. It is when you make many changes to one class. 

## How to recognize divergent change

If you have to change your existing class structure just to add one more method. You shouldn't have to alter existing class methods to add another, if you have to modify any existing methods when adding a new method, this is a sign of divergent change.

## Example

This is an example of divergent code because if we want to add any additional items to the grocery list we have to completely refactor the code.

```c++
class Groceries {
    public:
        void printItems() {
            cout << item1;
            cout << item2;
            cout << item3;
        };

    private:
       string item1;
       string item2;
       string item3;
}

```

## Harmful to software design

It is harmful to software design because it will require lots of extra work to add additional functionality. 

## How to fix

Plan out design of classes and software to be specic to their use cases. Ensure there is no unrelated functions within any given class

## Sources

https://refactoring.guru/smells/divergent-change
https://sourcemaking.com/refactoring/smells/divergent-change