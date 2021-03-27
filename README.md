# Python Version Changes
## About
* No one likes to read long release notes to see what's new. 
* You also want a simple one stop shop to keep up with new python features to 
keep your skills sharp!
* Here is a simplified feature list which can be used as a reference for new features. 
* This doc promises to stay simple, clean, and easy to navigate. 
* More detailed release notes can be found as links to more detailed release pages.

## Contents
* [3.10](#Version-3.10)
* [3.9](#Version-3.9)
* [3.8](#Version-3.8)
* [3.7](#Version-3.7)
* [3.6](#Version-3.6)

---

## Version 3.10
[CONTENTS](#Contents) | [UP]() | [DOWN](#Version-3.9)
* Detailed Version Changes [here]()

---

## Version 3.9
[CONTENTS](#Contents) | [UP](#Version-3.10) | [DOWN](#Version-3.8)
* Detailed Version Changes [here]()

---

## Version 3.8
[CONTENTS](#Contents) | [UP](#Version-3.9) | [DOWN](#Version-3.7)
Detailed Version Changes [here](https://docs.python.org/3/whatsnew/3.8.html)
### **Assignment Expressions (Walrus Operator)**
* Assign varibles at the time of comparison. 
```python
# Before: 
list_length = len(someList)
if(list_length > 100):
    print(f"The list length is large: {list_length}")

# After:
if(list_length := len(someList)):
    print(f"The list length is large: {list_length}")

# Useful example:
if(results := re.findall(r'someMatch', dataString)):
    print(results)
```

### **Positional-only parameters**
* Use "/" to indicate that certain function input params are positional and cannot be 
used as keywords. 
```python
def showCar(make, model, /, year, miles, *, color, body_type):
    print(make, mode, year, miles, color, body_type)
```
* From above: 
    * params before "/" must be positional. (make, model)
    * params before "*" and after "/" can be either positional or keywords. (year, miles)
        * Usual rules apply (cannot use keywords before positional)
    * params after "*" must be keywords. (color, body_type)
```python
# Valid call to above function: 
showCar("Nissan", "Altima", year=2018, miles=50000, color="yellow", body_type='sedan')

# Invlid call to above function: 
showCar("Nissan", model="Altima", year=2018, miles=50000, color="yellow", body_type='sedan')
```


### **F-string "=" Support.**
* "{var=}" in f-strings expand to var=value text. 
```python
age = 25
print(f'{age=}')

# OUTPUT
age=25
```


---

## Version 3.7
[CONTENTS](#Contents) | [UP](#Version-3.8) | [DOWN](#Version-3.6)
* Detailed Version Changes [here]()

---

## Version 3.6
[CONTENTS](#Contents) | [UP](#Version-3.7) | [DOWN]()