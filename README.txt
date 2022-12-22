
Colorectal cancer is a disease in which cells in the colon or rectum grow out of control. Sometimes it is called
colon cancer, for short. The colon is the large intestine or large bowel. The rectum is the passageway that 
connects the colon to the anus.

Sometimes abnormal growths, called polyps, form in the colon or rectum. Over time, some polyps may turn into 
cancer. Screening tests can find polyps so they can be removed before turning into cancer. Screening also helps
find colorectal cancer at an early stage, when treatment works best.

Vision Transformers (ViT; Dosovitskiy et al.) extract small patches from the input images, linearly project them, 
and then apply the Transformer (Vaswani et al.) blocks. The application of ViTs to image recognition tasks is 
quickly becoming a promising area of research, because ViTs eliminate the need to have strong inductive biases 
(such as convolutions) for modeling locality. This presents them as a general computation primititive capable 
of learning just from the training data with as minimal inductive priors as possible. ViTs yield great downstream
performance when trained with proper regularization, data augmentation, and relatively large datasets.

In the Patches Are All You Need paper (note: at the time of writing, it is a submission to the ICLR 2022 
conference), the authors extend the idea of using patches to train an all-convolutional network and demonstrate
competitive results. Their architecture namely ConvMixer uses recipes from the recent isotrophic architectures
like ViT, MLP-Mixer (Tolstikhin et al.), such as using the same depth and resolution across different layers in
the network, residual connections, and so on.


ConvMixer is very similar to the MLP-Mixer, model with the following key differences:

1. Instead of using fully-connected layers, it uses standard convolution layers.
2. Instead of LayerNorm (which is typical for ViTs and MLP-Mixers), it uses BatchNorm.

Two types of convolution layers are used in ConvMixer. (1): Depthwise convolutions, for mixing spatial locations
of the images, (2): Pointwise convolutions (which follow the depthwise convolutions), for mixing channel-wise 
information across the patches. Another keypoint is the use of larger kernel sizes to allow a larger receptive 
field.

S M Ahmed Hassan Shah