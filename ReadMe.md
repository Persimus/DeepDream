
# Deep dream for pictures and video frames
Hello this code is for creating Deep Dream pictures and video frames for total newbies that do not know Python, like myself.

I will try to explain how to setup this code run for normal people who have not touched code in their life.

But first I want give due regards to sentdex, his YouTube channel can be found [here](https://www.youtube.com/user/sentdex) as almost all of this code us his and and it can be found [here](https://pythonprogramming.net/deep-dream-python-playing-neural-network-tensorflow/) I only changed tiny bit of it and writing this instructions to make it so everyone would be able to experiment with it.

# Prerequisites 
These instructions are for Windows 10, so keep it in mind.

Download these:
Anaconda v 3.7: https://www.anaconda.com/distribution/ 
Visual Studio Code: https://code.visualstudio.com/

# Setup
We will need some setup to be able to run our code 

## Anaconda

 1. Open "Anaconda Navigator" application that was installed with your anaconda project
 2. Go to "Environments" tab
 3. Press "Create"
 4. Make sure that in Packages Python is selected and version is 3.7, give your desired name to application environment and click create
 5. Select your newly created environment
 6. Go to "Home" tab in "Anaconda Navigator" and press "Launch" button at VS Code (Visual Studio Code should be installed)

Now we can continue with Visual Studio Code Setup
**Every time you want to launch Visual Studio Code do it from "Anaconda Navigator" so that we would not have any issues with incorrect environment setup**

## Visual Studio Code 

 1. Press "Open folder..." link/button and select folder where you have
    downloaded this code and press "Select Folder" button
 2. The file structure should appear at the left side of the window, select "dream_image.py" file
 3.  On the left bottom corner you should see a text reading Python version and environment name you have created in Anaconda Navigator, if not press on the text and select it in the popup. 
 4. Press a green play button in  top right corner of the window, you should see "ModuleNotFoundError: No module named 'matplotlib'" error in the terminal, if you see no error and program is working you are in luck and it magically works and you can play with it, otherwise we need to continue
 5. Now we will need to download the dependencies for the code write the following commands in terminal window and wait till they are complete installing (it might take some time):
- pip install matplotlib
- pip install tensorflow==1.14
- pip install Pillow
- pip install scipy

Now you should be able to run the program

# How to use
**Do this only after the setup is complete!**

Add .jpg file or multiple files into input directory.

Run the code using Visual Studio Code using these steps:

 1. Select dream_image.py file in Visual Studio Code file explorer
 2. On the left bottom corner you should see a text reading Python version and environment name you have created in Anaconda Navigator, if not press on the text and select it. 
 3.  Press a green play button on Visual Studio Code top right corner

Console should start running and if everything goes okay you should see a message telling that the program has started processing the image and when it is finished console will say which files it has processed. 

After all images are processed a "Done" messages will be printed.
You can check your files in output directory. **Warning if you are rerunning the process the old files will be deleted**

## Configurations

 Update number to change the dream type:

    layer_tensor = model.layer_tensors[1]

Update these to change the parameters of the dream:

    num_iterations=20, step_size=1.0, rescale_factor=0.5, num_repeats=8, blend=0.2 

