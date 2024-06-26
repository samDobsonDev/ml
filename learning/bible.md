# Resources

- [Let's build GPT: from scratch, in code, spelled out.](https://www.youtube.com/watch?v=kCc8FmEb1nY&t=30s)
- [Let's build the GPT Tokenizer](https://www.youtube.com/watch?v=zduSFxRajkE)

# Neural Networks

A Neural Network is a computational structure inspired by the human brain's neural networks. It consists of layers of neurons, which are mathematical functions that simulate the behavior of biological neurons. These neurons process inputs (data) using weights (importance of each input), biases (adjustment values to the neuron's output), and activation functions (which introduce non-linearity to the model) to produce outputs. Neural networks are used for both the training and inference phases of a model.

# Determining Weights and Biases

Biases and weights in a neural network are initially chosen randomly or through specific initialization methods before the training process begins. The choice of initial values can significantly affect the efficiency and effectiveness of the training process. Here's a brief overview of how biases and weights are chosen and adjusted:

## Initial Selection

- **Random Initialization:** Weights and biases can be initialized to small random numbers. This randomness helps to break symmetry, ensuring that neurons in the same layer can learn different patterns during training.
- **Zero Initialization:** While biases can be initialized to zeros (since their role is to shift the activation function), initializing weights to zero is generally avoided because it leads to symmetry where all neurons in a layer will learn the same features during training.
- **He and Xavier Initialization:** These are sophisticated methods designed to set the initial weights to values that consider the size of the previous layer, aiming to keep the signal (variance) in a reasonable range across layers. This helps in achieving a more stable and faster convergence during training.

## Adjustment During Training

- **Backpropagation:** Once the network is initialized and starts training, weights and biases are adjusted using an algorithm called backpropagation. In this process, the network makes predictions on the training data, and a loss function calculates the error of the predictions. The gradient of this error is then computed with respect to each weight and bias in the network.
- **Gradient Descent:** This is an optimization algorithm used to minimize the error by updating the weights and biases in the direction that most decreases the error. The size of the step taken in this direction is determined by a parameter called the learning rate.
- **Learning Rate:** A crucial hyperparameter that controls how much the weights and biases are adjusted during training. Too high a learning rate can cause the model to converge too quickly to a suboptimal solution, or even diverge. Too low a learning rate makes the training process very slow.

The process of adjusting weights and biases is iterative and continues for many epochs (passes through the training dataset) until the model achieves a satisfactory level of performance or until another stopping criterion is met. This iterative optimization refines the initial random or heuristically chosen values of weights and biases to values that minimize the loss function, thereby improving the model's predictions.

# Examples of Activation Functions

- ReLU (Rectified Linear Unit)
- Sigmoid
- Tanh (Hyperbolic Tangent)
- Softmax

# Training

## Stage 1 - Pretraining

Pretraining involves training the neural network on a large, general dataset to learn a broad understanding of the language or task at hand. This stage is resource-intensive and aims to develop a base model capable of general language understanding and generation.

## Stage 2 - Fine-Tuning

Fine-tuning is the process of adjusting the pre-trained model's parameters with a more specific dataset, such as high-quality Q&A conversations for an AI assistant. This stage is less resource-intensive than pretraining and allows for quick iterations to adapt the model to specific tasks or improve performance on certain data types.

# Inference

Inference refers to the process of using a trained model to make predictions or decisions based on new, unseen data. This process requires the trained model (including its parameters/weights) and a small amount of code that typically involves loading the model, preparing the input data in the format the model expects, executing the model with this input, and then processing the output for interpretation or further use.

# GPU Programming

The act of optimizing a given compute task to take advantage of the GPUs ability to process information in parallel, by dividing the task into smaller, more manageable pieces, and then processing each piece simultaneously on different GPU cores. This is a fundamental concept in parallel computing and is crucial for improving the efficiency and speed of data-intensive tasks, such as training neural networks. Methods to do this vary depending on the targeted GPU architecture. In the context of Machine Learning, libraries such as TensorFlow and PyTorch are essentially wrappers of numpy that are optimized to utilize the GPU. For example:
- **NVIDIA:** CUDA (Compute Unified Device Architecture)
- **AMD:** ROCm (Radeon Open Compute)
- **OpenCL:** Open Compute Language. Open standard for parallel programming across multiple platforms and architectures for non-graphics tasks. This is not to be confused with OpenGL, which is a graphics-specific API.

# Glossary

- **Neural Network:** A computational structure inspired by the structure of the human brain's neural networks, consisting of layers of neurons that process data.

- **Model:** In machine learning, a model refers to the combination of a specific neural network architecture and its trained parameters (weights and biases). The model embodies the knowledge learned from the training data. It's what you use to make predictions or decisions based on new, unseen data. Essentially, the model is the neural network plus its learned experience.

- **Parameters:** The weights and biases of a neural network.

- **Neuron:** A mathematical function in a neural network that simulates the behavior of biological neurons. These neurons receive input, processes them (typically via it's weight/weighted sum, then via an activation function), and produces an output.

- **Weights:** Parameters within a neural network that determine the importance of each input to a neuron's output. Think of weights as the influence each input has on a neuron's decision. If a weight is high, it means that particular input plays a bigger role in determining what the neuron will output.

- **Biases:** Parameters that adjust the output of a neuron, independent of its inputs, adding flexibility to the model. For each neuron there is typically 1 bias. Imagine biases as the nudge to make a neuron more likely to lean in a certain direction. It's like having a starting point before even looking at the inputs, ensuring neurons can activate even if all inputs are low or zero.

- **Activation Functions:** A mathematical function that introduces non-linearity into the neural network, allowing it to learn complex patterns.

- **Inference:** The process of "using" a trained model to make predictions or decisions based on new, unseen data.

- **Training:** The process of teaching a neural network to perform a task by adjusting its weights and biases, typically involving stages like pretraining and fine-tuning.

- **Pretraining:** The initial training phase where a neural network is trained on a large, general dataset to learn broad language or task understanding.

- **Fine-Tuning:** The subsequent training phase where a pre-trained model is further trained on a specific dataset to specialize in a particular task or improve performance on certain data types.

- **Tokenizer/Tokenization:** Converting a dataset or input in a sequence of integers, and vice versa. We do this so we can perform the mathematical operations to train the neural network, or to use the neural network during inference. In the case of inference, we can then convert the output of the model back into its original format.

- **Overfitting:** Occurs when a model learns the training data too well, capturing noise and outliers, which harms its performance on new data.

- **Hyperparameter:** Hyperparameters are the configuration settings used to structure the learning process of a neural network. Unlike parameters, which the model learns during training, hyperparameters are set prior to the training process and can significantly influence the performance and efficiency of the neural network. Examples include learning rate, number of epochs, and batch size. Adjusting these settings requires a careful balance to ensure the model learns effectively without overfitting or underfitting the training data.

- **Block Size/Chunk:** Refers to the size of data processed at one time, affecting memory usage and computational efficiency during training.

- **Loss:** The loss function quantifies the difference between the predicted tensor outputs of the model and the actual tensor output values. It serves as a guide for the optimization process, with the goal of training being to minimize this loss, indicating better model performance and accuracy.

- **Backpropagation:** A method used to update the model's parameters by calculating and distributing the error back through the network's layers.

- **Gradient Descent:** A fundamental optimization algorithm used in training neural networks, where the model parameters (weights and biases) are adjusted iteratively to minimize the error between the predicted output and the actual output. This process involves calculating the gradient (or derivative) of the loss function with respect to each parameter and moving the parameters in the direction that reduces the loss.

- **Autograd:** Autograd is a tool used in many machine learning libraries that automatically calculates the gradients of tensors, using Gradient Descent. It allows developers to easily compute derivatives, which are essential for optimizing neural networks through algorithms like backpropagation. Essentially, when you perform operations on tensors (multidimensional arrays of numbers) during model training, Autograd keeps track of these operations and automatically computes the gradients for you, simplifying the process of updating model parameters (weights and biases) to minimize the loss function. This automation makes the development of complex neural network models more straightforward and efficient.

- **Tensors:** A tensor is a multidimensional array of numbers. In the context of machine learning, tensors are often used to represent inputs, outputs, and intermediate results in a neural network. They are similar to arrays in mathematics, but they can be of any dimension and can be used to represent a wide range of data types, including images, text, and more.

- **Epochs:** One epoch represents one complete pass of the training dataset through the neural network during training. Multiple epochs are typically used to ensure the model accurately learns from the data. The exact number of epochs can vary, ranging from tens to hundreds or more, depending on the complexity of the model and the task the model is being trained for.

- **Non-linearity:** Non-linearity in a model means it can capture and represent complex patterns that aren't just straight lines or simple, direct relationships. In the context of machine learning, the "curve" metaphorically represents the intricate relationship between input data and the desired output, illustrating how neural networks can learn and model complex patterns and dependencies beyond simple linear mappings.

- **Backend:** In the context of machine learning libraries, the "backend" refers to the specific computational engine that executes the mathematical operations and data processing tasks required for training and running neural network models. Tinygrad, for instance, supports multiple backends, including GPU (OpenCL), C Code (Clang), LLVM, Metal (Mac), CUDA (NVIDIA GPUs), HSA. This flexibility allows users to choose the most suitable computational resource based on their project's requirements, optimizing performance and efficiency.

