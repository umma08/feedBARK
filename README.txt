FeedBARK v0.2

Project - FeedBARK is a feedback generating machine that seeks to create a stable and usable audio feedback environment using a choice of digitally generated signals, or direct microphone input. Wekinator's machine learning platform is implemented to monitor and govern the feedback process, with a user able to create a feedback state of their choosing. Wekinator is used to ensure that the state of the feedback in the audio system remains controlled. 

Inputs - BARK coefficients from an analysed audio signal, generated in Max/MSP with the help of the analyser~ external. Scaled, and sent as 25 discrete inputs to Wekinator. 

Outputs - Three Parameters are used to control feedback gain, feedback filter frequency cutoff, and feedback filter frequency quotient. 

Machine Learning Implementation- 
Wekinator was used to train a data set using a machine learning algorithm based on neural networks. Several different configurations of the neural network were tried in the design and development stage of the project, before I decided that a 3 layer neural network was effective enough for the project. The number of nodes per hidden layer was equal to the number of inputs. This meant that the system takes quite a bit of time to train, but it also provides a high degree of accuracy when extracting features from the input. You can simplify the system, and get similar results, but for the purposes of this project, i will use a 3 layer neural network. 

Most Significant Issue
There were two main hurdles that I faced in designing and developing the project. 

The first hurdle was when designing and developing this system was configuring the choice of inputs in such a way that it created interesting sounds without determining the way in which it would be used by a user. I want the system to be open enough for everyone to engage with (hence the microphone inout) but also restricted enough, so that simple feedback systems can be implemented quickly and easily. In the end I decided that I wanted the user to have the choice between five distinct types of audio input - sine wave, saw wave, triangle wave, pink noise, and microphone input. I felt that this was a good balance between deterministic and indeterministic use.

The second hurdle that I faced - which I cannot fix - is that the bark~ external that I use within the Max/MSP patch is relatively outdated. It would seem that it has not been updated for more modern operating systems, and this means that the patch will crash on these machines. While the patch does work on machines that run on MAC OSX 10.7 or earlier, I am not sure how it runs on any machines that are more modern that this. It would seem that the external causes this issue. I have a feeling it is a 32bit/64bit problem, and i am hoping that it might get fixed at some stage by the external developer. 

How could the Wekinator System be Improved
It would be nice if Wekinator sent a message via OSC when training of a data set was complete. This way, FeedBARK could become aware of when a Wekinator algorithm was ready to be run.

Hardware Configurations
I have included a Max/MSP patch for FeedBARK. An external analyser~ is required, and is included in the FeedBARK folder. There are some issues with compatibility specifically modern versions of OSX, which i am trying to get to the bottom of. From what I know, it is a problem with the external, and as I am not in control of this i cannot fix the problem. I tested this on 10.7.x with Max/MSP version 6.x. 

Instructions.
Open up the included Max/MSP patch. 
Open up the included Wekinator Project
The included Wekinator project is setup for Pink Noise input, and will find a stable feedback level given a generated pink noise signal. 
If you wish to create a stable feedback status given any other input, you will need to train Wekinator yourself.
The way in which this is done is by configuring Wekinator to understand when the system is running too 'hot' or too 'cold' - and then to adjust parameters so that an in-between state is found. 
The method of doing this is shown with the provided video documentation. 






