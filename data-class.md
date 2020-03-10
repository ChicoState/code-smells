### Data Class

A Data class is an object that only has fields, and the getters and setters for those fields.

```{c++}
class User{
	private:
		int user_id;
		string username;
		string email;
	public:
		int get_id();
		void set_id();
		//ect...
}
```
Data classes are a problem since these classes end up just holding data that is used by other objects, but can't independently opperate on data they own. A data class could be improved by moving more of the functionallity that interacts with the data to the class with the data.