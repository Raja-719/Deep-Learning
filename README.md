EfficientNetB0 function
keras.applications.EfficientNetB0(
    include_top=True,
    weights="imagenet",
    input_tensor=None,
    input_shape=None,
    pooling=None,
    classes=1000,
    classifier_activation="softmax",
    **kwargs
)
Instantiates the EfficientNetB0 architecture.

Reference

EfficientNet: Rethinking Model Scaling for Convolutional Neural Networks (ICML 2019)
This function returns a Keras image classification model, optionally loaded with weights pre-trained on ImageNet.

For image classification use cases, see this page for detailed examples.

For transfer learning use cases, make sure to read the guide to transfer learning & fine-tuning.

Note: each Keras Application expects a specific kind of input preprocessing. For EfficientNet, input preprocessing is included as part of the model (as a Rescaling layer), and thus keras.applications.efficientnet.preprocess_input is actually a pass-through function. EfficientNet models expect their inputs to be float tensors of pixels with values in the [0-255] range.

Arguments

include_top: Whether to include the fully-connected layer at the top of the network. Defaults to True.
weights: One of None (random initialization), "imagenet" (pre-training on ImageNet), or the path to the weights file to be loaded. Defaults to "imagenet".
input_tensor: Optional Keras tensor (i.e. output of layers.Input()) to use as image input for the model.
input_shape: Optional shape tuple, only to be specified if include_top is False. It should have exactly 3 inputs channels.
pooling: Optional pooling mode for feature extraction when include_top is False. Defaults to None.
None means that the output of the model will be the 4D tensor output of the last convolutional layer.
avg means that global average pooling will be applied to the output of the last convolutional layer, and thus the output of the model will be a 2D tensor.
max means that global max pooling will be applied.
classes: Optional number of classes to classify images into, only to be specified if include_top is True, and if no weights argument is specified. 1000 is how many ImageNet classes there are. Defaults to 1000.
classifier_activation: A str or callable. The activation function to use on the "top" layer. Ignored unless include_top=True. Set classifier_activation=None to return the logits of the "top" layer. Defaults to 'softmax'. When loading pretrained weights, classifier_activation can only be None or "softmax".
