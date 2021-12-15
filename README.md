# Mouse-Follow-Tutorial
A tutorial on how to get the player's direction to follow where the mouse is on the screen

# 1) The Setup
To start with the set up, create a 2D level and add a circle with a square as a child so that it's clear what direction is being faced:

![image](https://user-images.githubusercontent.com/91538155/146252082-63f012de-063f-4cb9-ad95-4cf452f41b27.png)

Next, create a pivot, make it a child of the circle, and then make the square a child object of the pivot:

![image](https://user-images.githubusercontent.com/91538155/146252217-3c63d991-2a0c-40c6-9e61-051c37d6dc97.png)

Get the moveemnt in, using this simple code that I explained more into in my Smooth Camera Tutorial, this time adapted for 2D:

![image](https://user-images.githubusercontent.com/91538155/146252386-42371504-1d7a-4141-b130-75f5a319ef5c.png)

# 2) Coding the Rotation
The player facing the direction of the mouse is all based on rotation. So, to start with, we need the following declarations:

![image](https://user-images.githubusercontent.com/91538155/146252735-8d3b42ef-6c6b-4ef1-8dc8-515717ac5d22.png)

The Camera is to find the position of the mouse, the Rigidbody is to locate the 2D position of the player, and the Transform is so that the game knows what to rotate.

Next, in void Start, we need references to the camera and the Rigidbody

![image](https://user-images.githubusercontent.com/91538155/146253012-d1382412-e982-40e7-ac0a-2da5b1dc6264.png)

Now, in void Update, we start with this line, which allows the game to track the position of the mouse on the screen:

![image](https://user-images.githubusercontent.com/91538155/146253135-dcd20f7a-2a6b-4e10-aefc-7cfef8085987.png)

Next, this line to get the direction from the player to the mouse so that the game knows how much to pivot based on where the player is:

![image](https://user-images.githubusercontent.com/91538155/146253241-f98bfa5d-de76-44a0-b4d6-59a2ad6d472e.png)

Then, we need this line to calculate the rotation of the player relative to the mouse position:

![image](https://user-images.githubusercontent.com/91538155/146253371-fe585597-1f14-4a86-8a20-e15fa1527eda.png)

And finally, this line applies the rotation to the player:

![image](https://user-images.githubusercontent.com/91538155/146253438-0bc4d2e1-8eaa-4f06-90d0-59c47e537cfa.png)

Now, in Unity, apply the Pivot game object to where it needs to be in the script, and when you move the square should point towards wherever the mouse is:

![image](https://user-images.githubusercontent.com/91538155/146253573-2ba64c7a-7e83-4032-9b94-ad11e48e2c6f.png)

# Congratulations, your player constantly faces the mouse!
