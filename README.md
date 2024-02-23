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
#### AlexNet
![image](https://github.com/Ra00f1/Convolutional-Neural-Networks-Summary/assets/32569954/0651433d-ced9-4a65-91bd-7fe9de5499ad)
####  VGG-16
- Smaller and easier compared to other networks
- Conv Layers: has the same filter size(3x3), stride of 1, and "same" padding
- Max-Pool: 2x2 and stride 2
![image](https://github.com/Ra00f1/Convolutional-Neural-Networks-Summary/assets/32569954/f133ea64-99fc-476d-8895-a78c8d7acdc1)

### ResNet


