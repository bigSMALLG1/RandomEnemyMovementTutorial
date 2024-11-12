# RandomEnemyMovementTutorial
A written tutorial on how to program random enemy movement using C# in Unity
This tutorial demonstrates how you program enemies to move in random directions, changing the angle of their directions randomly within a certain timeframe that can be set by the programmer.

1. Start by creating a new Unity project named RandomEnemyMovement, for this tutorial we will be using the 2D render pipeline so select this option when creating the project.

2. Once the project is created and has loaded, right click on an empty space in the hierarchy and select (2D Object --> Sprites --> Circle) as shown below.
   ![image](https://github.com/user-attachments/assets/e3cf4b82-937b-4f30-91b3-335c09cd2ceb)

3. Then we will want to create a new C# script to attach to our game object. Right click on an empty space in the assets box and select (Create --> C# Script) it will prompt you to name the script so go ahead and name it "enemyMovement". This will create our C# script 
   where we can begin programming the movement for our enemy.
   ![image](https://github.com/user-attachments/assets/da34a2bc-6c5b-4c56-8c64-8c0e95e8b0ea)

4. Before we start programming, it is good practice to name our game objects, so that our projects are easier to understand. Right click on Circle on the hierarchy and rename it to "enemy".

5. Open up on the C# script and we can begin programming. Delete the default notes in the script (// Start is called before the first frame update) and (// Update is called once per frame).

6. We want to begin by creating our variables. We are going to need 5: enemySpeed; minTime; maxTime; a Vector3 direction and timer;

7. All variables par from 1 will be float variables, the syntax is as follows:

   private float enemySpeed = 2f; (This will be the actual speed that our enemy will travel at;

   private float minTime = 1f; (This is the minimum time in seconds that our time limit will be before the enemy changes direction. in this case it is 1 second as 1f = 1 second. So there is a chance that the enemy will change       
   direction in 1 second)

   private float maxTime = 3f; (This is the maximum time in seconds before our enemy will change direction, so our enemy will change direction in a random time between 1 and 3 seconds).

   private Vector3 direction; (This sets a direction for our enemy to move in)

   private float timer; (The variable where our random time between 1 and 3 seconds will be stored)


9. 

10. 
