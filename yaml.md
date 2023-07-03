# YAML

#### Key Value Pair

Fruit: Apple
Vegetable: Carrot
Liquid: Water
Meat: Chicken

#### Array/Lists

Fruits:
- Orange
- Apple
- Banana

Vegetables:
- Carrot
- Methi
- Tomato

#### Dictionary/Map

Banana:
    Calories: 105
    Fat: 0.4g
    Carbs: 27g

Grapes:
    Calories: 62
    Fat: 0.3g
    Carbs: 16g

Dictionary - unordered collection
List - Ordered collection


Quiz

#### Dictionary in Dictionary
A dictionary employee is given. Add the remaining properties to it using information from the table below.

Key/Property	Value
name	        john
gender	        male
age	            24

```
employee:
    name: john
    gender: male
    age: 24
```

#### Dictionary in Dictionary in Dictionary
Now try adding the address information. Note the address is a dictionary

Key/Property	Value
name	        john
gender	        male
age	            24
address	        Key/Property	Value
                city	edison
                state	new jersey
                country	united states

```
employee:
    name: john
    gender: male
    age: 24
    address:
        city: edison
        state: new jersey
        country: united states
```

#### List of Dictionaries
We would like to add additional details for each item, such as color, weight etc. We have updated the first one for you. Similarly modify the remaining items to match the below data.

Fruit	Color	Weight
apple	red	    100g
apple	red	    90g
mango	yellow	150g

```
- 
    name: apple
    color: red
    weight: 100g
-   name: apple
    color: red
    weight: 90g
-   name: mango
    color: yellow
    weight: 150g
```

#### List of Dictionary
We would like to record information about multiple employees. Convert the dictionary employee to an array employees.

```
employees:
    - name: john
      gender: male
      age: 24
```

#### List of Dictionary in Dictionary
Now try adding the pay information. Remember while address is a dictionary, payslips is an array of month and amount

Key/Property	Value
name	        john
gender	        male
age	            24
address	        ...     
payslips        #	month	amount
                1	june	1400
                2	july	2400
                3	august	3400

```
employee:
    name: john
    gender: male
    age: 24
    address:
        city: edison
        state: 'new jersey'
        country: 'united states'
    payslips:
        - month: june
          amount: 1400
        - month: july
          amount: 2400
        - month: august
          amount: 3400
```

