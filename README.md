# GWC Intermediate Week6

Welcome back everyone! We hope you all had a great weekend, and are ready to learn something new. Before we get started, let's spend some time work on a challenge to recall your memory.

### Recap Exercise

Write a Python Module that contains a simple math function called `multiply2`. The function should:
* Take in an number
* Multiply it by 2
* print the number

Then save the module as `times2.py` and open a new file that:
* Imports the `times2.py` using `import`
* Call the multiply2 function with any input number

After you finish the exercise, raise your hand and let one of your TAs know before you move on to the next part!

Hint: [Click Here](https://sites.google.com/umn.edu/umngwcilw4/) if you want to revisit materials from last week.

## More Python
### Python Dictionaries

Last week we learnt how to write our own module, and how we can apply it to simple user interface for Chatbot. Today, we start learning a new data structure, dictionaries!

A dictionary is a collection of data which is unordered, changeable and indexed. In Python dictionaries are written with curly brackets, and they have keys and values.

* Take a look at the following code and think what it should return:
```
person = {
    "name": "Cindy",
    "age": 20,
    "pet": "cat"
}
print(person)
```
Now open your IDLE, create a new file and run the above code. Does the result match with what you think? Ask TAs for explanations and make sure you understand before going further.
___
### Easy Access
Now we have a dictionary called `person`, so how can we get the data within it? One good thing about dictionaries is that you can access the items of a dictionary by referring to its key name:
```
animal = person["pet"]
print(animal)
```
There is also a method called get() that will give you the same result:
```
animal = person.get("pet")
print(animal)
```
You may wonder if we can check if the key exists. This is actually similar to what we did using list, where the `in` operator is used.
Let's take a look at the example below:
```
bot = {
    "name": "Bob, the bot",
    "age": 1,
    "hobby": "talking"
}
print('What do you wanna learn about me?')
user_option = input('>>')
if(user_option in bot):
      print('My ', user_option,' is ', bot.get(user_option),'.')
else:
      print('Too much to tell!')
```
#### Exercise 1: Modify the above code to create another bot of your choice.
___
### Changable Values
Another advantage of using dictionaries is that the collection is changable. You can change the value of a specific item by referring to its key name. Look at the `person` dictionary again:
```
person = {
    "name": "Cindy",
    "age": 20,
    "pet": "cat"
}
person["pet"] = "penguin"

print(person)
```
Guess what? The collection has be updated! 

### Adding an new item
You can always add new items to the dictionaries. All you need to do is using a new index key and assigning a value to it. Here is an example:
```
person = {
    "name": "Cindy",
    "age": 20,
    "pet": "penguin"
}
person["color"] = "maroon"
print(person)
```
Now the `person` dictionary contain one more item!

### Removing an item
Sometimes you may just wanna get rid of some of the items from the dictionary. There are several methods to remove items from a dictionary:
