# Music-Generation-using-Deep-Learning
<b>Music Generation</b>

<b>Real World Problem</b>:
The objective of music generation is to explore deep learning regarding the field of music composition using artificial intelligence.
The case study focuses on generating music automatically using Recurrent Neural Networks(RNN).
We do not need to be an expert to generate music. Even non experts like me can generate a descent quality creative music using RNN.
Creating music was something unique to humans until now, but some great advancements have been made using deep learning.

<b>Objective</b>
Building a model that takes existing music data as input learns the pattern and generates "new" music.
The model-generated music need not be professional, as long as it is melodious and good to hear.
It cannot simply copy and paste from the training data. It has to learn the patterns from the existing music that is enjoyed by humans.
Now, what is music?
Basically, music is a sequence of musical components/events.
Input- Sequence of musical events/notes
Output- New sequence of musical events/notes
In this case study, I have limited myself to single instrument music. You can extend this to multiple instrument music.

<b>Music Representation</b>
Sheet music representation can be used for both single instrument and multi instrument.----> visual file
Abc - notation---- popular
MIDI---> popular
Mp3 ---> audio files ----> actual audio file In this case study, we will focus on abc notation as it is the simplest one and just uses alpha numeric character.

<b>Char-RNN Model (High-Level Overview)</b>
So, we have some domain knowledge by now and we need not be an expert. We'll now ground this in and know about char-RNN. Since our music is a sequence of characters, therefore our obvious choice will be RNNs.
There is a special type of RNN called "Char-RNN".
We will be using many to many RNN. Here, we will feed the RNN with our characters of the sequence one by one and it will out the next character in the sequence.

<b>Data Obtaining:</b>
Refer : http://abc.sourceforge.net/NMD
It says "ABC version of the Nottingham Music Database" which contains over 1000 folk tunes stored in a special text format.
Of course, it takes a lot of time to train the model with larger data like 1000 tunes. So I will use the jigs dataset which contains about 340 tunes.
You get a txt file with multiple tunes here.
Simply copy and paste into a txt file as input.txt.
Each tune is having a meta data section and music section.
