# Residual-Network-for-Digit-Recognition
This is a 50 layer ResNet built for recognition of Hand Digits


# The Problem of Very Deep Neural Networks

In recent years, neural networks have become much deeper, with state-of-the-art networks evolving from having just a few layers (e.g., AlexNet) to over a hundred layers.

The main benefit of a very deep network is that it can represent very complex functions. It can also learn features at many different levels of abstraction, from edges (at the shallower layers, closer to the input) to very complex features (at the deeper layers, closer to the output).

However, using a deeper network doesn't always help. A huge barrier to training them is vanishing gradients: very deep networks often have a gradient signal that goes to zero quickly, thus making gradient descent prohibitively slow.

More specifically, during gradient descent, as you backpropagate from the final layer back to the first layer, you are multiplying by the weight matrix on each step, and thus the gradient can decrease exponentially quickly to zero (or, in rare cases, grow exponentially quickly and "explode," from gaining very large values).

During training, you might therefore see the magnitude (or norm) of the gradient for the shallower layers decrease to zero very rapidly as training proceeds.

# Enter Res Nets
In ResNets, a "shortcut" or a "skip connection" allows the model to skip layers
</br>
![resnet](resnet.PNG)
</br>

ResNet blocks with the shortcut also makes it very easy for one of the blocks to learn an identity function. This means that you can stack on additional ResNet blocks with little risk of harming training set performance.

On that note, there is also some evidence that the ease of learning an identity function accounts for ResNets' remarkable performance even more than skip connections help with vanishing gradients.

Two main types of blocks are used in a ResNet, depending mainly on whether the input/output dimensions are the same or different:  the "identity block" and the "convolutional block."

##  Identity block

</br>
![Identity block](Identity block.PNG)

## Convolution block

</br>
![Convolution block](Convolution block.PNG)

## The 50 layer Residual Network

</br>
![Res Net 50](resnet50.PNG)

## Summary

</br>
![summary](summary.PNG)
</br>

## Signs Dataset
![signs](signs.PNG)


## Try your own image
The notebook provides an option to try your own image


