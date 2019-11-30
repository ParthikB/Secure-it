# encryption

It's working now. I'm going somewhere with this.

Now this is what I've done so far:

1) Training data used : MNIST Digit Dataset

2) Created a fully connected layer network.
	> Number of nodes in the output layer = total no. of pixels/image
	> Using 'Sigmoid' instead of 'ReLU' as the activation function of every layer.

3) Training data:
	> x = digit image
	> y = digit image
	(Not using the classes because we don't need them, yet.)

4) Taking the final output from the layer, as well as the output of the 2nd layer.

5) Once the model is trained, now take any random digit image and pass it through the network with 'grads --> off'.

6) Now the network throws us two images, one is the final output and the other one is the output of the 2nd layer, which is the ENCRYPTED IMAGE.

7) Now, to test is that encrypted image is really the encryption of the digit we passed through the network, i.e, to DECRYPT the image, now we'll pass the image in the same network bu not from the first layer, instead from the third layer (of the next layer from which we took the encrypted image output from, in this case it is 2nd.)

8) The final output is really coming out to be the same digit. Few information is lost though, but this is the first version and many optimizations are still left!
