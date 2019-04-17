# ReciPic
Project contributors: basilchatha, smitp415, 

## Inspiration
An exorbitant amount of food is wasted every year in the U.S - something needs to be done. The issue is simple: nobody knows what to do with the food they have left over after using some of it. Our application gives users ideas on how to use the food they have left over by recommending them delicious recipes - our way of helping reduce the amount of wasted food in the world!

## What it Does
Users who have the ReciPic app will take photos of all of the ingredients they have/want to use. The app will then process the ingredient images with opencv to figure out what the user is trying to use. It then uses the keras extension of tensorflow to suggest a recipe that has the most ingredients in common with what the user sent in.

## How we Built it
We constructed an android app within android studio that will be responsible for taking and sending images via sockets. The images taken will then be sent to a python server and be run through an opencv classifier used to identify vegetables and produce a dictionary of all the ingredients that are present. After the dictionary is built, it is run through a comparison algorithm against a csv containing 12,000 recipes to find the recipe that a) has the most ingredients in common with the input and b) has the highest proportion of available ingredients (i.e. if two recipes have 4 ingredients in common with the input set, but one has half the needed ingredients as the other, the first recipe will be chosen). This data is then sent back to the app via another socket and displayed to the user.

## Accomplishment we're proud of
* Building an Android Studio application
* Actually establishing a connection and sending data from app to server
* Successfully processing and identifying images of vegetables
* Constructing a search algorithm that will produce, in our opinion, the best results for the given ingredients