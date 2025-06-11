### starting with Deep learning 

## basic of ANN

<img src="ann1.png">

## ===>>

# 🔵 1. What is an Artificial Neural Network (ANN)?

An ANN is a computational model inspired by the human brain, built from layers of neurons (also called nodes or units), which learn to solve tasks (like classification or regression) by adjusting internal parameters.

## 🧠 2. Building Blocks of ANN

### 🔹 A. Neurons (Nodes)

A neuron receives inputs, applies weights and bias, computes a sum, applies an activation function, and outputs a signal.

**Formula:**

```
z = w1*x1 + w2*x2 + ... + wn*xn + b
a = activation(z)
```

- `x`: input features  
- `w`: weights  
- `b`: bias  
- `a`: output after activation  

### 🔹 B. Layers in ANN

- **Input Layer**:  
    Takes in the input data (e.g., image pixels, features).  
    No activation function applied here.

- **Hidden Layers (1 or more)**:  
    The intermediate layers where neurons learn patterns.  
    Most learning happens here.  
    Depth of the model = number of hidden layers.

- **Output Layer**:  
    Produces final output (e.g., class label or continuous value).  
    Often uses softmax for classification, or linear for regression.

---

## 🧮 3. Weights and Biases

| Component | Role |
|-----------|------|
| **Weights (w)** | Control the importance of each input feature. |
| **Bias (b)** | Helps the neuron shift the activation function left or right. |

✅ **Learnable**: Yes, these are the parameters the model adjusts during training using backpropagation.

---

## ⚙️ 4. Activation Functions

These introduce non-linearity so the model can learn complex patterns (like curves, edges, interactions).

| Activation | Formula | Use-case |
|------------|---------|----------|
| **Sigmoid** | `1 / (1 + e^-z)` | Binary classification (outputs between 0 and 1) |
| **Tanh** | `(e^z - e^-z)/(e^z + e^-z)` | Output between -1 and 1 |
| **ReLU** | `max(0, z)` | Default for hidden layers (fast and effective) |
| **Softmax** | `e^zi / sum(e^zj)` | Multiclass classification |

---

## 📉 5. Loss / Cost Function

Used to measure how well the model predictions match the true values.

| Task | Loss Function |
|------|---------------|
| **Regression** | Mean Squared Error (MSE): `(y - ŷ)^2` |
| **Binary Classification** | Binary Cross-Entropy |
| **Multi-Class Classification** | Categorical Cross-Entropy |

👉 During training, the model tries to minimize the loss.

---

## 🔁 6. Forward Propagation

The process of passing input through the network:

```
Input → Hidden Layer(s) → Output
```

Each layer:
- Applies weights and biases
- Activates using an activation function
- Passes result to the next layer

---

## 🔄 7. Backpropagation

The process of updating weights and biases based on the loss:
- Compute gradients using chain rule
- Use Gradient Descent or its variants (SGD, Adam, RMSprop)
- Update weights:  
    ```
    w = w - learning_rate * ∂Loss/∂w
    ```

---

## ⚖️ 8. Optimizer

An algorithm that updates weights to reduce loss.

Popular ones:
- **SGD (Stochastic Gradient Descent)**
- **Adam (Adaptive + Momentum-based)**
- **RMSprop**

---

## 🧮 9. Epochs, Batches, and Iterations

- **Epoch**: One full pass over the training data  
- **Batch**: Subset of data used in one forward/backward pass  
- **Iteration**: One update step = one batch processed  

---

## 🔍 10. Evaluation Metrics

| Type | Metric |
|------|--------|
| **Classification** | Accuracy, Precision, Recall, F1 Score |
| **Regression** | MAE, RMSE, R² Score |

---

## 🧠 Intuition

Imagine you're training a dog to recognize different balls (sizes, shapes, colors). With each attempt, the dog adjusts (like the ANN adjusts weights) to get better.

---

## 💡 Visualization of a 3-Layer ANN

```
Input Layer         Hidden Layer         Output Layer
[ x1 ] ----------> ( h1 ) ------------> [ y1 ]
[ x2 ] ----------> ( h2 ) ------------> [ y2 ]
[ x3 ] ----------> ( h3 )
```

Each arrow represents a weight, each `( )` is a neuron, and output is computed through activation functions.

## ANN in action 

### python Modules / frameworks for creating ANN 

<img src="ann2.png">

### installing tensorflow and keras 

```
pip install tensorflow keras

```
### Nuerons in layers 

<img src="layer1.png">

### ANN compile options 

<img src="layer2.png">

### LLM's are using specific kind of ANN -- Transformers 

<img src="layer3.png">

### More info about LLM 

<img src="layer4.png">

### fine tuning openai GPT model 

<img src="layer5.png">


