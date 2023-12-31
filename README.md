# Predatory Simulation of Animals

## Demo
![Simulation](https://github.com/JCQuacode/Predatory-Simulation/assets/122890528/984ceffa-0c62-412a-bbe2-c5eecc54712f)


## Description
This program simulates the predatory relationship of cats and snake with birds. Here, the birds are the prey.

- The animals move about on the window.
- Although visually it seems like a 2D space, in actuality, there are moving in a 3D space.
- Every animal has a speed with which they move.
- Every animal has a range in which the other animals may fall into.
- Birds and Snake have a smell and hear property with which they can store the animals they have smelt.
- Cats and Snakes move to the nearest bird in the plane.
- If the bird is within the range of the snake or the cat, the bird is eaten and it dissappears from the screen.
- This simulation keeps going until all the birds have been eaten.

## Movement and Ranges
### Cats (C)
- Range: 8
- Speed: 16

### Snakes (S)
- Range: 3
- Speed: 14

### Birds (B)
- Move in a random (-10, 10) along the X axis.
- Move in a random (-10, 10) along the Y axis.
- Move in a random (-2, 2) along the Z axis.

## Classes
### Animal class
- Its subclasses: Cat, Snake and Bird
- Superclass for other specific animal subclasses to inherit from.
- Contains shared animal attributes.
- Move method to move the birds indirectly by passing the dx, dy and dz to the Move() in Position.
- Other move methods to randomize the positions of the birds
- Methods to find the nearest bird and to check whether the otehr animal is in range
- ToString method to display their properties.
- Subclasses implement other methods to hear and smell.
- An animal hears if the other animal is travelling at a certain speed within a certain distance.
- An animal smells if the other animal is within a certain distance.
- Both hear and smell methods would store the animals in a double linked list.

### Position class
- The class defines the positions of the animals in a 3D space.
- It has x, y and z attributes.
- Methods to manipulate the positions of the animals: MoveTo(), DistanceBetween(), RandomPosition(), etc.

### DoublyLinkedList class
- Standard list with a few tweaks.
- A doubly linked list to store the names of the animals or the smelt/heard animals.
