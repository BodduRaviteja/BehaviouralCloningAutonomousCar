# Project: Behavioural Cloning of  Autonomous Car

Here NVIDIA model is implemented and trained to predict the steering angle of each and every frame of a car on simulated track.

 UDACITY car simulator is used to train and validate the model on its default modes. The Flask-Socketio application(patch file) is used to establish the server-client communication between the model and simulator.

![Screenshot (68)](https://user-images.githubusercontent.com/65815640/118396495-191e7f00-b650-11eb-93b5-9f6bfbd52dc4.png) ![Screenshot (69)](https://user-images.githubusercontent.com/65815640/118396501-1de33300-b650-11eb-8656-5cbe94c280a1.png)

Patch file can be found in 'https://github.com/BodduRaviteja/BehaviouralCloningPatchfile.git'

After acquiring the data in the training mode read it into dataframe. The following pictures are before and after extracting the tail end of the images

![1](https://user-images.githubusercontent.com/65815640/118397111-c2ff0b00-b652-11eb-970f-ac409e6e4a1b.png)

![2](https://user-images.githubusercontent.com/65815640/118397110-c2667480-b652-11eb-8064-ae2eb9b1f91f.png)

By default most of the track is straight and obviously had baised results towards center. For our model to predict left and right steering angels threshold is set 

![3](https://user-images.githubusercontent.com/65815640/118397408-102fac80-b654-11eb-9bd8-83dbd06c340e.png)

and after that data is split into Training and Testing within that limit. 

![4](https://user-images.githubusercontent.com/65815640/118397795-1cb50480-b656-11eb-937e-f4cb5563c2c5.png)


In order to not to overload the model with large data to process lets process it as much as we can for Region of Interest.

![5](https://user-images.githubusercontent.com/65815640/118397620-37d34480-b655-11eb-88f0-5851324a15b0.png)

Then implement the model and adjust its parameters for best it

![6](https://user-images.githubusercontent.com/65815640/118397654-67824c80-b655-11eb-9f8d-9c2283eba9d7.png)

![Screenshot (64)](https://user-images.githubusercontent.com/65815640/118397662-6f41f100-b655-11eb-9c34-f464eb003110.png)

Finally save the model and use it to predict the angles.





