Starfighter and Dreadnought are two spaceships from the popular science fiction film series, Star Wars. Let's imagine that you're building a game based on these 2 spaceships, maybe a space shooting game.

Begin by creating two classes for **Starfighter** and **Dreadnought**.

Next, make another class named **GameObject** for defining the properties and methods common for all game objects. Game object refers to any object that is part of the game, such as spaceships, rocks, etc.

Since all game objects have health points, define a property of type *double* in *GameObject* called *healthPoint* and two properties of type *int* called *x* and *y* for holding info about the position. 
Set health point to 100 and x and y to 0 by default.
Make accessors and mutators (getters and setters) for all properties.
Make a constructor which takes x and y as arguments.

*Starfighter* and *Dreadnought* must inherit from *GameObject.*
Write constructors for both the classes which takes x and y as arguments and passes them to the parent class's constructor.
For both classes, make a property of type int called *fuel.* and make a getter for it.
Make a method called *consumeFuel* which reduces the value of *fuel* by the amount provided as argument.

We want to categorize all fuel consumers into one group. To do so, make an interface called **FuelConsumer** which mandates its implementors to have the method *consumeFuel.*

*Starfighter* and *Dreadnought* are fuel consumers, make them both implement the interface *FuelConsumer.*

Make a class called **Rock** which inherits from *GameObject* too and has a constructor which does the same task as that of *Starfighter* and *Dreadnought*.

In the main method of a testing class called **Run**, make an array for holding 7 game objects (instances of *GameObject*). Populate the array, keeping instances of *Rock* in the positions 0-2, *Starfighter* in positions 3-4 and *Droidnought* in positions 5-6 of the array.

For testing each GameObject, make a method called *testGameObjecct* in *Run* which accepts any *GameObject* as argument, displays its x and y position, healthPoint and tests whether the object is a fuel consumer or not (use "obj instanceof FuelConsumer" code for this purpose).
Back in the main method, write a loop which feeds items of the array you created to the *testGameObject* method.