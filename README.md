# AI Self-Driving Car

# The Environment
The environment is compltely build using kivy webapp.Kivy is a free and open source Python framework, used for the development of applications like games, or any kind of mobile app. Check out the website here: https://kivy.org/#home 
<br>
<img src="https://user-images.githubusercontent.com/56478257/99615963-64115e00-2a42-11eb-861c-7fff5b743392.jpg" width="500" height="500" />
<br>
This black screen, which is the Kivy user interface, inside which you can build your games or apps.
White rectangle with three coloured dots in front of it. Well, that’s the car. The white rectangle represent our car and 3 little dots are the sensor of the car. On this map we will have the option to build roads, delimited by sand, which the car will have to avoid going through. So these 3 sensor detect sand in the map.
<br>
#### There are three buttons to click on at the bottom left corner of the screen, which are:
<br>
<ul>
<li>clear: removes all the sand drawn on the map</li>
<li>save: saves the weights (parameters) of the AI which is permanently trained</li>
<li>load: loads the last saved weights that were saved before during the training</li>
</ul>
<br>

# Defining the goal

We train our car to go from the upper left corner of the map, to the bottom right corner, we build road between these two spots which will be avoided by our car.
<br>
<p float="left">
<img src="https://user-images.githubusercontent.com/56478257/99616996-56f56e80-2a44-11eb-9f7e-5f7e86ef9075.jpg" width="400" height="400" />
<img src="https://user-images.githubusercontent.com/56478257/99617196-cec39900-2a44-11eb-8d1a-8dfa1351f919.jpg" width="400" height="400" />
</p>
<br>
Now we can clearly formulate a goal, to train the self-driving car to make round trips between the Airport and Downtown. As soon as it reaches the airport, it will then have to go to Downtown, and as soon as it reaches Downtown, it will then have to go to the Airport. More than that, it should be able to make these round trips along any road connecting these two locations. It should also be able to cope with any obstacles along that road it has to avoid.
<br>
<br>

# The Rewards
To define the system of rewards, we have to know these 2 case first:
<br>
<ul>
<li>In which cases do we give the AI a good reward? How good for each case?</li>
<li>In which cases do we give the AI a bad reward? How bad for each case?</li>
</ul>
<br>
Hence, based on this goal and above cases:
<br>
<ul>
1.	We give the AI a good reward when it gets closer to the destination.<br>
2.	We give the AI a bad reward when it gets further away from the destination.<br>
3.	We give the AI a bad reward if it’s about to drive onto some sand.<br>
</ul>






