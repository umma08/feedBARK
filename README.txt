Feedback Classifier v0.1

This signal generator creates a direct digital audio feedback path from a sine wave or external audio input. 

This signal is analysed using the bark~ analyser Max/MSP external, which creates 25 feature coefficients that may be sent to the Wekinator machine learning application. 

This is the first stage (v0.1) of a self-monitoring and self-stabilising feedback generator. 

The intended goal is to create a machine able to find a stable self-feedback state, given any audio input. 

Included is a Max/MSP patch (tested in Version 6.1.10), the necessary bark~ external, and a standalone Max/MSP application which runs on Apple Mac OSX 10.6+.

The extractor works with the default setting of the Wekinator - if you wish to control Wekinator from the GUI, please ensure that the "Enable OSC control of GUI" selection is ticked in the Actions menu of Wekinator.

Have fun!

http://github.com/umma08/feedback_classifier

http://wekinator.org

http://web.media.mit.edu/~tristan/maxmsp.html
 
http://cnmat.berkeley.edu/downloads

email:
robinrenwick@hotmail.com