This GitHub contains work for my thesis titled "Evaluating player off-the-ball movement in football with reinforcement learning". To perform this work I had access to full tracking data for 9 youth games (x and y positions for each of the 22 players at 10 frames per second) and some player touch data. 

**The code in this work was not written with the intent of convenience for those looking to emulate the same work, as such object oriented programming is rarely used and strong assumptions on the format of the data may be done.**

The explanation of the purpose of each file is as follows:

**Data_Treatment** - This contains the bulk of the code for this work: Transforming the raw data into position, velocity and acceleration dataframes to be used, determining ball position, extracting pass datasets to train the pressure model and PCM, extracting the pressure variables for each pass, the entirety of the code regarding the PCM as well as preparing the data for RL and creating visualizations.

**Filter** - This contains the code of the filter that is applied to all raw positional data before anything else is done with it.

**GetBall** - This is a text file with code to obtain the ball position that can be pasted into Data_Treatment. The ball position files are however already made available in the Processed Data folder (the dfb files).

**code_transform** - This contains a bit of code that transforms the ball touch data in a way that rotates the pitch by 180 degrees in games that required it (so that team 1 is always attacking left to right).

**visuais** - This contains code from https://github.com/Friends-of-Tracking-Data-FoTD/LaurieOnTracking to aid with visualizations.

**RL** - This contains all the code regarding the Reinforcement Learning models, including setting up a generator and a DQN implementation.

the .pt files contain the final models.

As for the folders, naturally the PressureModel folder contains code regarding the Pressure model and the xGModel folder contains code for the xG model. Raw Data contains the initial data for this work and processed data contains for convenience the data obtained after going through all the steps of data treatment.

Visualizations are also included in the Videos folder.
