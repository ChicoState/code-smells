A Refused Bequest is where you have a subclass which inherits from a parent class but does not use some of its parent class functionality/behaviors. The derived class refuses the behavior of the base class.

```java
class Government {
    protected double computeBaseTax() { //... }
    protected double addPersonalTax(double tax) { //... }
    public double getTax() {
        double tax = computeBaseTax();
        return addPersonalTax(tax);
    }
}

class Company extends Government {
    private double computeInitialTax() { //... }
    @Override 
    public double getTax() {
        double tax = computeInitialTax();
        return addPersonalTax(tax);
    }
}
```

Here the Company class refuses the behaviors of the Government class by not being able to use computeBaseTax().

found from [Stack Overflow](https://stackoverflow.com/questions/28271150/what-is-a-refused-bequest)


Context smells in software design can impair or disrupt the design and quality and make them hard to maintain and evolve. They violate good practices and design principles, affecting understanding, maintenance and promoting a negative impact on software quality and ease of evolution. 

found from [Preprints.org](https://webcache.googleusercontent.com/search?q=cache:a67NUQwOZWoJ:https://www.preprints.org/manuscript/201810.0059/v1/download+&cd=13&hl=en&ct=clnk&gl=us)

    Let’s say you have a sub class called “Class B” which inherits from a Super Class called “Class A”. Let’s also say that Class A contains the functions: Function 1, Function 2, Function 3, Function 4 and Function 5. If Class B only uses Function 1 and Function 2, you can consider making a new class called “Class C” from which Class A and Class B inherit. Class C would now contain Function 1 and Function 2 and Class A would not. 

found from [Refactoring Guru](https://refactoring.guru/smells/refused-bequest)
