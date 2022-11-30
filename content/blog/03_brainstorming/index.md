---
title: "Brainstorming of Locomotion and Interaction Techniques"
date: 2022-11-17T08:47:11+01:00
draft: false
summary: "As the goal of this course, we are supposed to implement a locomotion and an interaction technique in VR.
I did some brainstorming and collected ideas."
---

As the goal of this course, we are supposed to implement a locomotion and an interaction technique in VR.
An already implemented environment can be used for this purpose (see figure TODO). The environment includes a parcours which needs tobe navigated and coins that need to be collected. Additionally, there are several stops within the parcours where the user needs to move and rotate an object to fit into a predefined shape. The code for the parcours can be found here (TODO).

[TODO figure/screenshots]

## Examples of Locomotion Techniques and Metaphors
* Teleportation (e.g., pointing, throwing an object or using a clone)
* Arm swinging
* Walking in place
* Skiing
* Climbing
* Swinging around
* Flying
* Swimming
* Rowing (e.g., canoe, kayak)
* Driving a vehicle (e.g., by car, boat, bike...)
* Poses and gestures using hand tracking

## Idea 1: The Flash
This design combines the approaches of 'Freedom Walking' and 'Ninja Running' which can be found in the [Locomotion Vault](https://locomotionvault.github.io/).
#### Scenario
The user is in the role of the 'Flash' and tries to move as quickly as possible in the environment by walking in place.
Slow walking results in small movements and fast walking including swinging of the hands results in big movements.
As this technique is quite fatiguing, a 'super speed mode' is added. By holding the hands behind the back, the user moves without additional walking. Depending on how much the user is leaning forward, the movement gets faster or slower. This way, it is possible to combine accuracy and speed.

To enhance the game further and to reduce motion sickness, the environment can be blurred while the user is in 'super speed mode'. It is also possible to adjust the design of the virtual hands to look more like the costume of Flash.

To track the swinging and movement of the player's arm, the controllers need to be used for the implementation. Nevertheless, it is difficult for this metaphor to implement the interaction task using a different technique than simply using the controllers.

[TODO picture]

#### Advantages & Disadvantages
Advantages:
* Reduces motion sickness
* Easy to learn since natural movements are used
* Accuracy and speed are combined

Disadvantages:
* Fatiguing, therefore the 'super speed mode' is added
* Difficult to design a creative technique for the interaction task

## Idea 2: Pacman
This design is similar to 'Walking Hands' which can be found in the [Locomotion Vault](https://locomotionvault.github.io/).

#### Scenario
The approach of 'Walking Hands' enables interaction in confined spaces. Nevertheless, the movement does not feel natural and is therefore comparably slow and difficult. As an alternative, my idea is to use the metaphor of Pacman (or a crocodile). The user moves his hand like shown in the picture below to mimic 'eating like Pacman'. When closing the hand, the user is moving forward. Either the orientation of the hand or the direction of view can be used to determine the direction of movement.

As this technique is prone to motion sickness, it might be useful to add a third person perspective. The user can then 'zoom out' of the scene in case of not feeling good.

Nevertheless, the metaphor of Pacman is very limited in terms of possible gestures. The interaction task could be implemented using simple hand tracking, but this would not be very creative and would not fully fit the metaphor.

[TODO picture]

#### Advantages & Disadvantages
Advantages:
* Can be used in confined spaces
* Users only need to learn the gestures and not the button assignments of the controllers which might be easier for less experienced users
* Less fatiguing compared to bigger gestures/movements

Disadvantages:
* The metaphor of Pacman provides only a limited number of gestures that fit into the metaphor (especially for the interaction task)
* Might still be fatiguing if movement should be fast
* Prone to motion sickness

## Idea 3: Hovercar
This design is similar to 'Flying Vehicle', 'Vehicle VR' and 'Driving' which can be found in the [Locomotion Vault](https://locomotionvault.github.io/).

#### Scenario
The idea is to give the user the impression of flying through a futuristic city using a hovercar. The user determines the direction of movement using a virtual steering wheel. The speed and flying height can be controlled using the buttons of the controllers. As many people already know how to drive a vehicle, this metaphor is very intuitive and easy to learn. At the same time, the users can practice their driving skills and reaction speed in a game environment.

To solve the interaction task, the users can select and move the object using a laserpointer. To rotate the object, the users rotate the steering wheel. While this approach fits into the metaphor, the rotation can only be performed on one axis instead of all three axes. Therefore, either an idea on how to change the axis is needed or a more inaccurate result needs to be accepted.

Furthermore, this technique is also likely to cause motion sickness. To mitigate this problem, a third person perspective can be added.

[TODO picture]

#### Advantages & Disadvantages
Advantages:
* Intuitive to learn as most users already know how to drive a vehicle
* No fatigue as the user performs only limited movements

Disadvantages:
* Rotation by using the steering wheel within the interaction task is only performed on one axis
* Prone to motion sickness
