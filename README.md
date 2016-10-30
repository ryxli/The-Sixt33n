# THE SIXT33N

The SIXT33N is a mobile robot on 3 wheels (2 drivable) that moves around according to some input. It uses the MSP430 Launchpad as its guts with some circuitry for driving the motor and sensing through a microphone. It also runs on a 9V battery, so we don’t have to chase it around as it moves. In Micro and Frond End, we designed SIXT33N’s ear. The design uses a microphone front end circuit that converts audio and speech into a signal. The signal is then processed, to include applying some level shift, gain, and filtering higher frequencies (low pass filter circuit) to avoid aliasing. This is then sent to the Launchpad ADC.

SIXT33N recognizes 4 different voice commands. It will then move forward, slow down, turn left, and turn right based on these commands. Collected voice signals are projected into a lower dimensional subspace based on their principal components (PCA/SVD) and then classified based on a training model. If the classification is within a certain threshold, the command will trigger the controller to send an appropriate control input.

View the demo here: https://www.youtube.com/watch?v=nk3QCyXg5XI

More info: https://inst.eecs.berkeley.edu/~ee16b/sp16/proj/
