# python-project
Colour Detection using Pandas &amp; OpenCV

In this color detection Python project, we are going to build an application through which you can automatically get the name of the color by clicking on them. 
So for this, we will have a data file that contains the color name and its values. Then we will calculate the distance from each color and find the shortest one.

Taking an image from the user
We are using argparse library to create an argument parser

3. Next, we read the CSV file with pandas
The pandas library is very useful when we need to perform various operations on data files like CSV. pd.read_csv() reads the CSV file and loads it into the 
pandas DataFrame. We have assigned each column with a name for easy accessing.

4. Set a mouse callback event on a window
First, we created a window in which the input image will display. Then, we set a callback function which will be called when a mouse event happens.

5. Create the draw_function
It will calculate the rgb values of the pixel which we double click. The function parameters have the event name, (x,y) coordinates of the mouse position, etc. 
In the function, we check if the event is double-clicked then we calculate and set the r,g,b values along with x,y positions of the mouse.

6. Calculate distance to get color name
We have the r,g and b values. Now, we need another function which will return us the color name from RGB values. To get the color name, we calculate a distance(d) 
which tells us how close we are to color and choose the one having minimum distance.

Our distance is calculated by this formula:

d = abs(Red – ithRedColor) + (Green – ithGreenColor) + (Blue – ithBlueColor)

7. Display image on the window
Whenever a double click event occurs, it will update the color name and RGB values on the window.

Using the cv2.imshow() function, we draw the image on the window. When the user double clicks the window, we draw a rectangle and get the color name to draw 
text on the window using cv2.rectangle and cv2.putText() functions.

8. Run Python File
The beginner Python project is now complete, you can run the Python file from the command prompt. Make sure to give an image path using ‘-i’ argument.


Output:

Double click on the window to know the name of the pixel color

Summary
In this Python project with source code, we learned about colors and how we can extract color RGB values and the color name of a pixel. 
We learned how to handle events like double-clicking on the window and saw how to read CSV files with pandas and perform operations on data. 
This is used in numerous image editing and drawing apps.
