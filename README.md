# Devanagari_CNN
CNN on devanagari dataset attains 97.48% accuracy

## CNN architecture

The input of all the convnets is
fixed to 32x32 b/w image. The image is passed through
a series of convolution and max-pooling operations. Each
convolution operation contains a 3x3 kernel with stride 1 and
no spatial padding. Subsequently, the convolutional output is followed by a ReLU function. The ReLU functions
do not saturate while training the convnet and eventually
help avoid the vanishing gradient problem. A maxpooling
operation is used after every 3 Convolution
operations,to reduce the computational intensity of the architecture. A kernel/filter
size of 2x2 with a stride of 2 pixels is used in each max
pooling operation. The final convolution layer is followed by
2 fully connected layers. Subsequently, the convnet terminates
with a softmax layer. 
<p>
The Convnets are trained by optimizing on a cross-entropy
loss function using mini batch gradient descent and backpropagation. The batch size is set to 32, with a nestrov
momentum of 0.9. The learning rate is set to a constant
value of 0.001, i.e. this value is not altered during training. A
constant dropout of 0.2 is used, to prevent over-fitting. The
weights are randomly initialized with a standard deviation of
0.1. ConvNet is trained on 30 epochs.</p>

<p>
  In all the convnets, a series of convolution operations with
3x3 filters are used to generate an effective larger receptive
field of 5x5 or 7x7, instead of directly using a 5x5 or 7x7
filters. This is because two consecutive 3x3 filters produce an
effective receptive field of a 5x5 filter, but at the same time
reduce the number of parameters in the network. Similarly,
three consecutive 3x3 filters produce an effective receptive
field of a 7x7 filter, while reducing the number of parameters
in the network </p>
