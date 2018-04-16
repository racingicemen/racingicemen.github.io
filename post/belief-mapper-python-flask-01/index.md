> Porting Belief Mapper tool to Python and Flask

[Belief Mapper](https://github.com/antonow/belief-mapper) is an interactive tool for creating a visual
map of a user's beliefs. The project as it exists now is
    
* implemented in Ruby and Rails
* not actively maintained.

[PyBeliefMapper](https;//github.com/racingicemen) is a port of this project to Python and Flask. In this 
blog post, we will extract the structure of the existing app and look at the steps involved in mapping 
the belief of a user. This will help us in the implemenation of PyBeliefMapper.

# Static Relationships
![image](/static/belief-mapper-class-diagram.png)

Let us first elaborate the relationships between a ```User```, a ```Belief```, and a ```UserBelief```

A ```User``` has a:

* ```username```, which uniquely identifies the user
* ```answered_questions```, which is a list of ids of the questions the user has answered
* ```demographic```, the ```Demographic``` to which the user belongs

A ```Belief``` has a:

* ```name```, which uniquely identifies the belief
* ```definition```, a more detailed description of the belief
* ```resource```, ??? not sure what this means ???
* ```starred```, ??? not sure what this means ???
* ```category```, Category to which the Belief belongs

```BeliefStats``` looks at all the ```User```s that hold a certain ```Belief``` and records the average
conviction with which the users hold that belief.

**NOT SURE ABOUT THE ```Stat```, ```Comment``` AND ```Connection``` CLASSES**

<!-- A ```Belief``` belongs to exactly one ```Category```, while a ```Category``` might have one or more 
```Belief```s

![image](/static/category-belief.png)

Similarly, a ```User``` belongs to exactly one ```Demographic```, while a ```Demographic``` has multiple
```User```s

![image](/static/user-demographic.png)

Now for the fun part. A ```User``` holds a set of ```Belief```s, and each ```Belief``` has a score. The
user's belief is mapped based on this score

![image](/static/user-beliefs.png) -->