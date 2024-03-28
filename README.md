## This is the project of the chapter "Denoising Diffusion" of the course "Deep Generative models" suggested by the technical university of Munich.

In this project, you will implement a denoising diffusion model to generate MNIST digits. The main idea is that a sufficiently powerful model learns to remove a bit of noise from a noisy sample. 
By iterating this model on a sample drawn from pure noise, one can generate samples from the training data distribution.

Generating reasonable samples with diffusion requires more advanced architectures than a simple MLP or CNN stack. To let you focus on implementing the core algorithm, we provide you with two
model architectures:

A simple convolutional resnet
A small U-net variant
The former requires less compute and can get you some results even with CPU training in a few minutes. However, in our experience the resnet model will only generate strokes and blotches 
without the global structure of a digit because of the limited receptive field of the model. If you have a GPU or a bit more time on your hands, you can change the configuration to train a U-net.
This takes roughly 5-10x as long but can yield some actual digits if you train it long enough.
