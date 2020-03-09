# Feature Envy

Methods that make extensive use of another class may belong in another class. Consider moving this method to the class it is so envious of.

```java
public class Phone {
    private final String unformattedNumber;
    public Phone(String unformattedNumber) {
        this.unformattedNumber = unformattedNumber;
    }
    public String getAreaCode() {
        return unformattedNumber.substring(0,3);
    }
    public String getPrefix() {
        return unformattedNumber.substring(3,6);
    }
    public String getNumber() {
        return unformattedNumber.substring(6,10);
    }
}
public class Customer...
    private Phone mobilePhone;
    public String getMobilePhoneNumber() {
        return "(" + 
            mobilePhone.getAreaCode() + ") " +
            mobilePhone.getPrefix() + "-" +
            mobilePhone.getNumber();
    }
```
Here Customer has to reach into Phone's data to format the number.
This formatting should be a feature of the phone class. 
(found from [Coding Horror](https://blog.codinghorror.com/code-smells/))
(found from [Code Smells](https://elearning.industriallogic.com/gh/submit?Action=PageAction&album=recognizingSmells&path=recognizingSmells/featureEnvy/featureEnvyExample&devLanguage=Java))



## Why is it considered harmful to software design?

* Requires high maintenance
* Difficult to enhance or extend features
* Reduces code readability and makes code hard to understand



## How should it be fixed?
* Move methods or fields
* Change methods so they perform one specific task at a time




