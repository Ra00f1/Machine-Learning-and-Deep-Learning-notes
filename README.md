# Convolutional-Neural-Networks-Summary
## Week 1
### Notes
f: Filter Size, s: Stride, p: Padding, n: Input Size, b: bias
- Filter Output Size: ((n + 2p - f) / s ) + 1
- Total Parameters: (n * f) + b
- Output after Max Pooling: ((n * f) / s) + 1
- Padding for "same" convolution: (f - s - 1) / 2 
## Week 2
### Classic Networks
#### -AlexNet
![image](https://github.com/Ra00f1/Convolutional-Neural-Networks-Summary/assets/32569954/0651433d-ced9-4a65-91bd-7fe9de5499ad)
####  -VGG-16
- Smaller and easier compared to other networks
- Conv Layers: has the same filter size(3x3), stride of 1, and "same" padding
- Max-Pool: 2x2 and stride 2
![image](https://github.com/Ra00f1/Convolutional-Neural-Networks-Summary/assets/32569954/f133ea64-99fc-476d-8895-a78c8d7acdc1)

### ResNet
ResNets are like normal networks but they have jumps every few layers which normally is either 2 or 3 layers and each one witj a jump is called a residual block.

One of experts I talked to explained it like this: while plain networks try to find which data the input resembles to, ResNets try to change the image into a data that it has worked with before.

#### Residual Block:     ![image](https://github.com/Ra00f1/Convolutional-Neural-Networks-Summary/assets/32569954/daf88f55-c510-4783-b1ea-9a414dfddcb7)

#### Residual Block Formula: ![image](https://github.com/Ra00f1/Convolutional-Neural-Networks-Summary/assets/32569954/44ce9aaa-9297-46b3-8e00-3310c0adb310)

![ResNet](https://github.com/Ra00f1/Convolutional-Neural-Networks-Summary/assets/32569954/42b42fdd-632b-4334-8063-69923e6e33b8)

# Notes
Loss function: Error for a single training example.

Cost function: Average of the loss functions of the entire training set.


