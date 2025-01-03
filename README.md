# RandomEnemyMovementTutorial
A written tutorial on how to program random enemy movement using C# in Unity.
This tutorial demonstrates how you program enemies to move in random directions, changing the angle of their directions randomly within a certain timeframe that can be set by the programmer.

1. Start by creating a new Unity project named RandomEnemyMovement, for this tutorial we will be using the 2D render pipeline so select this option when creating the project. Remember, as this is 2D, we will need to be using the 2D game object components throughout the tutorial.

2. Once the project is created and has loaded, right click on an empty space in the hierarchy and select (2D Object --> Sprites --> Circle) as shown below.
   ![image](https://github.com/user-attachments/assets/e3cf4b82-937b-4f30-91b3-335c09cd2ceb)

3. Then we will want to create a new C# script to attach to our game object. Right click on an empty space in the assets box and select (Create --> C# Script) it will prompt you to name the script so go ahead and name it "enemyMovement". This will create our C# 
   script 
   where we can begin programming the movement for our enemy.
   ![image](https://github.com/user-attachments/assets/da34a2bc-6c5b-4c56-8c64-8c0e95e8b0ea)

4. Before we start programming, it is good practice to name our game objects, so that our projects are easier to understand. Right click on Circle on the hierarchy and rename it to "enemy".

5. Open up on the C# script and we can begin programming. Delete the default notes in the script (// Start is called before the first frame update) and (// Update is called once per frame). We will also want to drag and drop the script in to the bottom of the inspector    of our enemy sprite.

   ![image](https://github.com/user-attachments/assets/5102ebb5-d471-474b-8cfd-632362a9ca3a)


7. We want to begin by creating our variables, writing them underneath the public class after the first square bracket. We are going to need 5: enemySpeed; minTime; maxTime; a Vector3 direction and timer;

8. All variables par from 1 will be float variables, the syntax is as follows:

   private float enemySpeed = 2f; (This will be the actual speed that our enemy will travel at;

   private float minTime = 1f; (This is the minimum time in seconds that our time limit will be before the enemy changes direction. in this case it is 1 second as 1f = 1 second. So there is a chance that the enemy will change       
   direction in 1 second)

   private float maxTime = 3f; (This is the maximum time in seconds before our enemy will change direction, so our enemy will change direction in a random time between 1 and 3 seconds).

   private Vector3 direction; (This sets a direction for our enemy to move in)

   private float timer; (The variable where our random time between 1 and 3 seconds will be stored)

   ![image](https://github.com/user-attachments/assets/82226e59-c486-4f48-b4ca-ec65a197ff76)


9. Once you have created your variables, navigate to the private void start() method where we will be writing our code within the square brackets. We will need to set a random direction for our enemy to travel in, so we will be using transform.translate which gets the game object to move and Random.insideUnitSphere which will set a random value for the direction variable.

10. The syntax is as follows:

 ![image](https://github.com/user-attachments/assets/510fe836-4c57-405f-abf2-b2f8fee4ccf3)

13. Within the square brackets of the update method, the syntax is as follows:
    transform.Translate(direction * enemySpeed * Time.deltaTime); (This allows the gameobject to move, it will move in a random direction at our set speed (enemySpeed) and also multiplied by Time.deltaTime which makes the game frame independent so it runs at the
    same frame rate on any computer.
    timer -= Time.deltaTime; (this causes the timer to decrease every second)

14. Now that we have our gameobject moving in a random direction, we will want it to change direction once the timer hits 0.

15. Within the same set of square brackets, we will be using an if statement. An if statement allows a certain set of code to run only if a certain condition or conditions are met. In our case we want our gameobject to change direction IF the timer reaches 0.

     ![image](https://github.com/user-attachments/assets/581bf86c-02a1-40c9-9332-fc798e9d7123)


    This will cause the enemy to change direction when the timer hits 0, whilst also resetting the timer to a random value within our minimum and maximum times.

17. Play test the scripts and tweak the variables to your liking.



    
