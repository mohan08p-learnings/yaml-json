# JSON & JSONPATH

Root element in dictionary is denoted by $.

{
    "car": {
        "color": "blue",
        "price": "$20000"
    }
    "bus": {
        "color": "red",
        "price": "$50000"
    }
}

Get car details

$.car

Get bus details

$.bus

Get car's color

$.car.color

Get bus's price

$.bus.price

NOTE: Output of all jsonpath query results in an array.

{
    "vehicles": {
        "car": {
            "color": "blue",
            "price": "$20000"
        }
        "bus": {
            "color": "red",
            "price": "$50000"
        }
    }
}

Get car details

$.vehicles.car

Get bus details

$.vehicles.bus

Get car's color

$.vehicles.car.color

Get bus's price

$.vehicles.bus.price


Quiz

#### 1. Develop a JSON path query to extract the expected output from the Source Data.
{
  "property1": "value1",
  "property2": "value2"
}

```
$.property1
```

#### 2. Develop a JSON path query to extract the bus details from the Source Data.
{
  "car": {
    "color": "blue",
    "price": "$20,000"
  },
  "bus": {
    "color": "white",
    "price": "$120,000"
  }
}

```
[
  {
    "color": "white",
    "price": "$120,000"
  }
]
```

#### 3. Dictionary in Dictionary
Develop a JSON path query to extract the price of the bus.
{
  "car": {
    "color": "blue",
    "price": "$20,000"
  },
  "bus": {
    "color": "white",
    "price": "$120,000"
  }
}

```
$.bus.price
```

#### 4. Dictionary in Dictionary
Develop a JSON path query to extract the price of the car.
{
  "vehicles": {
    "car": {
      "color": "blue",
      "price": "$20,000"
    },
    "bus": {
      "color": "white",
      "price": "$120,000"
    }
  }
}

```
$.vehicles.car.price
```

#### 5. List in Dictionary
Develop a JSON path query to extract data about the wheels of the car.
{
  "car": {
    "color": "blue",
    "price": "$20,000",
    "wheels": [
      {
        "model": "KDJ39848T",
        "location": "front-right"
      },
      {
        "model": "MDJ39485DK",
        "location": "front-left"
      },
      {
        "model": "KCMDD3435K",
        "location": "rear-right"
      },
      {
        "model": "JJDH34234KK",
        "location": "rear-left"
      }
    ]
  }
}

```
$.car.wheels
```

#### 6. List in Dictionary
Develop a JSON path query to extract data about the third wheel of the car.
{
  "car": {
    "color": "blue",
    "price": "$20,000",
    "wheels": [
      {
        "model": "KDJ39848T",
        "location": "front-right"
      },
      {
        "model": "MDJ39485DK",
        "location": "front-left"
      },
      {
        "model": "KCMDD3435K",
        "location": "rear-right"
      },
      {
        "model": "JJDH34234KK",
        "location": "rear-left"
      }
    ]
  }
}

```
$.car.wheels[2]
```

#### 7. List in Dictionary
Develop a JSON path query to extract the model of the third wheel of the car.
{
  "car": {
    "color": "blue",
    "price": "$20,000",
    "wheels": [
      {
        "model": "KDJ39848T",
        "location": "front-right"
      },
      {
        "model": "MDJ39485DK",
        "location": "front-left"
      },
      {
        "model": "KCMDD3435K",
        "location": "rear-right"
      },
      {
        "model": "JJDH3434KK",
        "location": "rear-left"
      }
    ]
  }
}

```
$.car.wheels[2].model
```

#### 8. List in Dictionary
Retreive all the payslip details of the employee.
{
  "employee": {
    "name": "john",
    "gender": "male",
    "age": 24,
    "address": {
      "city": "edison",
      "state": "new jersey",
      "country": "united states"
    },
    "payslips": [
      {
        "month": "june",
        "amount": 1400
      },
      {
        "month": "july",
        "amount": 2400
      },
      {
        "month": "august",
        "amount": 3400
      }
    ]
  }
}

```
$.employee.payslips
```

#### 9. List in Dictionary
Retreive the 3rd month's pay details of the employee.
{
  "employee": {
    "name": "john",
    "gender": "male",
    "age": 24,
    "address": {
      "city": "edison",
      "state": "new jersey",
      "country": "united states"
    },
    "payslips": [
      {
        "month": "june",
        "amount": 1400
      },
      {
        "month": "july",
        "amount": 2400
      },
      {
        "month": "august",
        "amount": 3400
      }
    ]
  }
}

```
$.employee.payslips[2]
```

#### 10. List in Dictionary
Retreive the 3rd month's pay amount of the employee.

```
$.employee.payslips[2].amount
```

#### 11. List in Dictionary
Give this a shot. Try to find Malala in the below list of Noble Prize Winners.
{
  "prizes": [
    {
      "year": "2018",
      "category": "physics",
      "overallMotivation": "\"for groundbreaking inventions in the field of laser physics\"",
      "laureates": [
        {
          "id": "960",
          "firstname": "Arthur",
          "surname": "Ashkin",
          "motivation": "\"for the optical tweezers and their application to biological systems\"",
          "share": "2"
        },
        {
          "id": "961",
          "firstname": "Gérard",
          "surname": "Mourou",
          "motivation": "\"for their method of generating high-intensity, ultra-short optical pulses\"",
          "share": "4"
        },
        {
          "id": "962",
          "firstname": "Donna",
          "surname": "Strickland",
          "motivation": "\"for their method of generating high-intensity, ultra-short optical pulses\"",
          "share": "4"
        }
      ]
    },
    {
      "year": "2018",
      "category": "chemistry",
      "laureates": [
        {
          "id": "963",
          "firstname": "Frances H.",
          "surname": "Arnold",
          "motivation": "\"for the directed evolution of enzymes\"",
          "share": "2"
        },
        {
          "id": "964",
          "firstname": "George P.",
          "surname": "Smith",
          "motivation": "\"for the phage display of peptides and antibodies\"",
          "share": "4"
        },
        {
          "id": "965",
          "firstname": "Sir Gregory P.",
          "surname": "Winter",
          "motivation": "\"for the phage display of peptides and antibodies\"",
          "share": "4"
        }
      ]
    },
    {
      "year": "2018",
      "category": "medicine",
      "laureates": [
        {
          "id": "958",
          "firstname": "James P.",
          "surname": "Allison",
          "motivation": "\"for their discovery of cancer therapy by inhibition of negative immune regulation\"",
          "share": "2"
        },
        {
          "id": "959",
          "firstname": "Tasuku",
          "surname": "Honjo",
          "motivation": "\"for their discovery of cancer therapy by inhibition of negative immune regulation\"",
          "share": "2"
        }
      ]
    },
    {
      "year": "2018",
      "category": "peace",
      "laureates": [
        {
          "id": "966",
          "firstname": "Denis",
          "surname": "Mukwege",
          "motivation": "\"for their efforts to end the use of sexual violence as a weapon of war and armed conflict\"",
          "share": "2"
        },
        {
          "id": "967",
          "firstname": "Nadia",
          "surname": "Murad",
          "motivation": "\"for their efforts to end the use of sexual violence as a weapon of war and armed conflict\"",
          "share": "2"
        }
      ]
    },
    {
      "year": "2018",
      "category": "economics",
      "laureates": [
        {
          "id": "968",
          "firstname": "William D.",
          "surname": "Nordhaus",
          "motivation": "\"for integrating climate change into long-run macroeconomic analysis\"",
          "share": "2"
        },
        {
          "id": "969",
          "firstname": "Paul M.",
          "surname": "Romer",
          "motivation": "\"for integrating technological innovations into long-run macroeconomic analysis\"",
          "share": "2"
        }
      ]
    },
    {
      "year": "2014",
      "category": "peace",
      "laureates": [
        {
          "id": "913",
          "firstname": "Kailash",
          "surname": "Satyarthi",
          "motivation": "\"for their struggle against the suppression of children and young people and for the right of all children to education\"",
          "share": "2"
        },
        {
          "id": "914",
          "firstname": "Malala",
          "surname": "Yousafzai",
          "motivation": "\"for their struggle against the suppression of children and young people and for the right of all children to education\"",
          "share": "2"
        }
      ]
    },
    {
      "year": "2017",
      "category": "physics",
      "laureates": [
        {
          "id": "941",
          "firstname": "Rainer",
          "surname": "Weiss",
          "motivation": "\"for decisive contributions to the LIGO detector and the observation of gravitational waves\"",
          "share": "2"
        },
        {
          "id": "942",
          "firstname": "Barry C.",
          "surname": "Barish",
          "motivation": "\"for decisive contributions to the LIGO detector and the observation of gravitational waves\"",
          "share": "4"
        },
        {
          "id": "943",
          "firstname": "Kip S.",
          "surname": "Thorne",
          "motivation": "\"for decisive contributions to the LIGO detector and the observation of gravitational waves\"",
          "share": "4"
        }
      ]
    },
    {
      "year": "2017",
      "category": "chemistry",
      "laureates": [
        {
          "id": "944",
          "firstname": "Jacques",
          "surname": "Dubochet",
          "motivation": "\"for developing cryo-electron microscopy for the high-resolution structure determination of biomolecules in solution\"",
          "share": "3"
        },
        {
          "id": "945",
          "firstname": "Joachim",
          "surname": "Frank",
          "motivation": "\"for developing cryo-electron microscopy for the high-resolution structure determination of biomolecules in solution\"",
          "share": "3"
        },
        {
          "id": "946",
          "firstname": "Richard",
          "surname": "Henderson",
          "motivation": "\"for developing cryo-electron microscopy for the high-resolution structure determination of biomolecules in solution\"",
          "share": "3"
        }
      ]
    },
    {
      "year": "2017",
      "category": "medicine",
      "laureates": [
        {
          "id": "938",
          "firstname": "Jeffrey C.",
          "surname": "Hall",
          "motivation": "\"for their discoveries of molecular mechanisms controlling the circadian rhythm\"",
          "share": "3"
        },
        {
          "id": "939",
          "firstname": "Michael",
          "surname": "Rosbash",
          "motivation": "\"for their discoveries of molecular mechanisms controlling the circadian rhythm\"",
          "share": "3"
        },
        {
          "id": "940",
          "firstname": "Michael W.",
          "surname": "Young",
          "motivation": "\"for their discoveries of molecular mechanisms controlling the circadian rhythm\"",
          "share": "3"
        }
      ]
    }
  ]
}

```
$.prizes[5].laureates[1]
```

#### 12. Retreive the first element in the list.
[
  "car",
  "bus",
  "truck",
  "bike"
]

```
$[0]
```

### 13. Retreive the first and 4th element in the list.

```
$[0,3]
```

Important
data
[
    12,
    43,
    23,
    45,
    1,
    6,
    89,
    49,
    33,
    90,
    77,
    65,
    42
]

get all numbers greater than 40
$[Check if each item in an array > 40]

Check if --> ?()

$[?(each item in the list > 40)]

each item in the list --> @

```
$[?(@ > 40)]
```

Similarly, we can use other operators as,
@ == 40
@ != 40
@ in [40, 43, 45]
@ nin [40, 43, 45]


#### JSON PATH - criteria
Get the model of rear-right wheel when you do not know the index.

{
  "car": {
    "color": "blue",
    "price": "$20,000",
    "wheels": [
      {
        "model": "KDJ39848T",
        "location": "front-right"
      },
      {
        "model": "MDJ39485DK",
        "location": "front-left"
      },
      {
        "model": "KCMDD3435K",
        "location": "rear-right"
      },
      {
        "model": "JJDH34234KK",
        "location": "rear-left"
      }
    ]
  }
}

```
$.car.wheels[?(@.location == "rear-right")].model
```