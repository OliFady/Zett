---
kindle-sync:
  bookId: "3449"
  title: Deep Learning - Goodfellow, Bengio
  author: Unknown Author
  highlightsCount: 101
tags:
  - Artificial-Intelligence
  - AI
  - Books
  - tech
---
# Deep Learning - Goodfellow, Bengio
## Metadata
* Author: Goodfellow, Bengio

## Highlights
Each piece of information included in the representation of the patient is known as a feature. — location: [186]() ^ref-24010

---
Deep learning solves this central problem in representation learning by introducing representations that are expressed in terms of other, simpler representations. Deep learning allows the computer to build complex concepts out of simpler concepts — location: [236]() ^ref-57614

---
To summarize, deep learning, the subject of this book, is an approach to AI. Specifically, it is a type of machine learning, a technique that allows computer systems to improve with experience and data. According to the authors of this book, machine learning is the only viable approach to building AI systems that can operate in complicated, real-world environments. Deep learning is a particular kind of machine learning that achieves great power and flexibility by learning to represent the world as a nested hierarchy of concepts, with each concept defined in relation to simpler concepts, and more abstract representations computed in terms of less abstract ones — location: [291]() ^ref-58258

---
The earliest predecessors of modern deep learning were simple linear models motivated from a neuroscientific perspective. These models were designed to take a set of n input values x1,..., xn and associate them with an output y. These models would learn a set of weights w1,..., wn and compute their output f (x, w) = x 1w1 + ■ ■ ■ + xn wn. This first wave of neural networks research was known as cybernetics, — location: [360]() ^ref-6733

---
the perceptron (Rosenblatt, 1958, 1962) became the first model that could learn the weights defining the categories given examples of inputs from each category. The adaptive linear element (ADALINE), which dates from about the same time, simply returned the value of f (x) itself to predict a real number (Widrow and Hoff, 1960), and could also learn to predict these numbers from data. — location: [372]() ^ref-53322

---
Most neural networks today are based on a model neuron called the rectified linear unit — location: [401]() ^ref-49781

---
The central idea in connectionism is that a large number of simple computational units can achieve intelligent behavior when networked together. This insight applies equally to neurons in biological nervous systems and to hidden units in computational models. — location: [428]() ^ref-41992

---
In the context of reinforcement learning, an autonomous agent must learn to perform a task by trial and error, without any guidance from the human operator. DeepMind demonstrated that a reinforcement learning system based on deep learning is capable of learning to play Atari video games, reaching human-level performance on many tasks — location: [603]() ^ref-26306

---
Scalars: A scalar is just a single number, in contrast to most of the other objects studied in linear algebra, which are usually arrays of multiple numbers. We write scalars in italics. We usually give scalars lower-case variable names. — location: [695]() ^ref-9411

---
Vectors: A vector is an array of numbers. The numbers are arranged in order. We can identify each individual number by its index in that ordering. Typically we give vectors lower case names written in bold typeface, such as x. The elements of the vector are identified by writing its name in italic typeface, with a subscript. The first element of x is x!, the second element is x2 and so on — location: [700]() ^ref-14444

---
A matrix is a 2-D array of numbers, so each element is identified by two indices instead of just one. We usually give matrices upper-case variable names with bold typeface, such as A. If a real-valued matrix A has a height of m and a width of — location: [719]() ^ref-14339

---
Tensors: In some cases we will need an array with more than two axes. In the general case, an array of numbers arranged on a regular grid with a variable number of axes is known as a tensor. — location: [738]() ^ref-41799

---
In order for this product to be defined, A must have the same number of columns as B has rows. If A is of shape m x n and B is of shape n x p, then C is of shape m x p. — location: [766]() ^ref-37925

---
Hadamard product, and is denoted as A 0 B. The dot product between two vectors x and y of the same dimensionality is the matrix product xTy. We can think of the matrix product C — AB as computing Ci;j as the dot product between row i of A and column j of B. — location: [775]() ^ref-16898

---
To describe matrix inversion, we first need to define the concept of an identity matrix. An identity matrix is a matrix that does not change any vector when we multiply that vector by that matrix. — location: [813]() ^ref-13925

---
The structure of the identity matrix is simple: all of the entries along the main diagonal are 1, while all of the other entries are zero — location: [818]() ^ref-48840

---
In order for the matrix to have an inverse, we additionally need to ensure that Eq. 2.11 has at most one solution for each value of b. — location: [890]() ^ref-50508

---
Together, this means that the matrix must be square, that is, we require that m = n and that all of the columns must be linearly independent. A square matrix with linearly dependent columns is known as singular — location: [894]() ^ref-63730

---
AA-1 = I. — location: [900]() ^ref-53558

---
The L1 norm is commonly used in machine learning when the difference between zero and nonzero elements is very important. Every time an element of x moves away from 0 by e, the L1 norm increases by e. We sometimes measure the size of the vector by counting its number of nonzero elements. Some authors refer to this function as the “L0 norm,” but this is incorrect terminology. The number of non-zero entries in a vector is not a norm, because scaling the vector by a does not change the number of nonzero entries. The L1 norm is often used as a substitute for the number of nonzero entries. — location: [924]() ^ref-5996

---
A symmetric matrix is any matrix that is equal to its own transpose: A = A T. — location: [956]() ^ref-57485

---
A random variable is a variable that can take on different values randomly. We typically denote the random variable itself with a lower case letter in plain typeface, and the values it can take on with lower case script letters. For example, x1 and x2 are both possible values that the random variable x can take on. For vector-valued variables, we would write the random variable as x and one of its values as x. — location: [1322]() ^ref-52896

---
The most commonly used distribution over real numbers is the normal distribution, also known as the Gaussian distribution: — location: [1489]() ^ref-30853

---
One of these functions is the logistic sigmoid: 1 ״(x) = 1 + exp(-x)30'3) — location: [1600]() ^ref-63401

---
The Bernoulli distribution is a distribution over a single binary random variable. It is controlled by a single parameter 0 £ [0,1], which gives the probability of the random variable being equal to 1. — location: [1470]() ^ref-2511

---
3.11 Bayes’ Rule We often find ourselves in a situation where we know P(y | x) and need to know P(x | y). Fortunately, if we also know P(x), we can compute the desired quantity using Bayes’ rule: P(x | y) (3.42) P(x)P(y | x) P(y) — location: [1641]() ^ref-484

---
One form of rounding error that is particularly devastating is underflow. Underflow occurs when numbers near zero are rounded to zero. Many functions behave qualitatively differently when their argument is zero rather than a small positive number. For example, we usually want to avoid division by zero — location: [1850]() ^ref-11489

---
Overflow occurs when numbers with large magnitude are approximated as to or —to. Further arithmetic will usually change these infinite values into not-a-number values. — location: [1856]() ^ref-58270

---
One example of a function that must be stabilized against underflow and overflow is the softmax function. The softmax function is often used to predict the probabilities associated with a multinoulli distribution. The softmax function is defined to be softmax(®)! = nexp(xi)— . (4.1) j=1 exP(X) — location: [1857]() ^ref-32623

---
The function we want to minimize or maximize is called the objective function or criterion. When we are minimizing it, we may also call it the cost function, loss function, or error function. — location: [1895]() ^ref-21089

---
When f' (x) = 0, the derivative provides no information about which direction to move. Points where f'(x) = 0 are known as critical points or stationary points. A local minimum is a point where f (x) is lower than at all neighboring points, so it is no longer possible to decrease f (x) by making infinitesimal steps. — location: [1913]() ^ref-26070

---
Some critical points are neither maxima nor minima. These are known as saddle points — location: [1926]() ^ref-64083

---
A point that obtains the absolute lowest value of f (x) is a global minimum. It is possible for there to be only one global minimum or multiple global minima of the function. It is also possible for there to be local minima that are not globally optimal — location: [1927]() ^ref-64755

---
We therefore usually settle for finding a value of f that is very low, but not necessarily minimal — location: [1932]() ^ref-3929

---
Optimization algorithms may fail to find a global minimum when there are multiple local minima or plateaus present. In the context of deep learning, we generally accept such solutions even though they are not truly minimal, so long as they correspond to significantly low values of the cost function — location: [1945]() ^ref-10182

---
where e is the learning rate, a positive scalar determining the size of the step. We can choose e in several different ways. A popular approach is to set e to a small constant. Sometimes, we can solve for the step size that makes the directional derivative vanish. Another approach is to evaluate f (x — eVxf (x)) for several values of e and choose the one that results in the smallest objective function value. This last strategy is called a line search. — location: [1964]() ^ref-6246

---
Most deep learning algorithms are based on an optimization algorithm called stochastic — location: [2236]() ^ref-37590

---
An example is a collection of features that have been quantitatively measured from some object or event that we want the machine learning system to process. We typically represent an example as a vector x E Rn where each entry xi of the vector is another feature. For example, the features of an image are usually the values of the pixels in the image — location: [2701]() ^ref-53479

---
Transcription: In this type of task, the machine learning system is asked to observe a relatively unstructured representation of some kind of data and transcribe it into discrete, textual form. For example, in optical character recognition, the computer program is shown a photograph containing an image of text and is asked to return this text in the form of a sequence of characters (e.g., in ASCII or Unicode format). Google Street View uses deep learning to process address numbers in this way (Goodfellow et al., 2014d). Another example is speech recognition, where the computer program is provided an audio waveform and emits a sequence of characters or word ID — location: [2291]() ^ref-38511

---
Machine translation: In a machine translation task, the input already consists of a sequence of symbols in some language, and the computer program must convert this into a sequence of symbols in another language. This is commonly applied to natural languages, such as to translate from English to French. — location: [2300]() ^ref-62686

---
computer program sifts through a set of events or objects, and flags some of them as being unusual or atypical. An example of an anomaly detection task is credit card fraud detection. By modeling your purchasing habits, a credit card company can detect misuse of your cards. If a thief steals your credit card or credit card information, the thief’s purchases will often come from a different probability distribution over purchase types than your own. — location: [2320]() ^ref-15023

---
Synthesis and sampling: In this type of task, the machine learning algorithm is asked to generate new examples that are similar to those in the training data. Synthesis and sampling via machine learning can be useful for media applications where it can be expensive or boring for an artist to generate large volumes of content by hand. For example, video games can automatically generate textures for large objects or landscapes, — location: [2326]() ^ref-19876

---
Density estimation or probability mass function estimation: In the density estimation problem, the machine learning algorithm is asked to learn a function pmode1 : Rn ^ R, where Pm0de1 (x) can be interpreted as a probability density function (if x is continuous) or a probability mass function (if x is discrete) on the space that the examples were drawn from. To do such a task well (we will specify exactly what that means when we discuss performance measures P), the algorithm needs to learn the structure of the data it has seen. It must know where examples cluster tightly and where they are unlikely to occur. Most of the tasks described above require that the learning algorithm has at least implicitly captured the structure of the probability distribution. Density estimation allows us to explicitly capture that distribution. — location: [2345]() ^ref-18783

Clustering

---
Some machine learning algorithms do not just experience a fixed dataset. For example, reinforcement learning algorithms interact with an environment, so there is a feedback loop between the learning system and its experiences — location: [2426]() ^ref-22386

---
build a system that can take a vector x E Rn as input and predict the value of a scalar y E R as its output. In the case of linear regression, the output is a linear function of the input. Let y be the value that our model predicts y should take on. We define the output to be y = w Tx (5.3) where w E Rn is a vector of parameters. Parameters are values that control the behavior of the system. In this case, wi is the coefficient that we multiply by feature xi before summing up the contributions from all the features. We can think of w as a set of weights that determine how each feature affects the prediction. If a feature xi receives a positive weight wi, then increasing the value of that feature increases the value of our prediction y. If a feature receives a negative weight, then increasing the value of that feature decreases the value of our prediction. If a feature’s weight is large in magnitude, then it has a large effect on the prediction. If a feature’s weight is zero, it has no effect on the prediction — location: [2462]() ^ref-60815

---
MSEtest =- ||y(test) - y(test) |2, (5.5) m so the error increases whenever the Euclidean distance between the predictions and the targets increases. — location: [2488]() ^ref-49304

---
It is worth noting that the term linear regression is often used to refer to a slightly more sophisticated model with one additional parameter—an intercept term b. In this model y _ wTx + b (5.13) so the mapping from parameters to predictions is still a linear function but the mapping from features to predictions is now an affine function. This extension to affine functions means that the plot of the model’s predictions still looks like a line, but it need not pass through the origin. Instead of adding the bias parameter b, one can continue to use the model with only weights but augment x with an extra entry that is always set to 1. The weight corresponding to the extra 1 entry plays the role of the bias parameter. We will frequently use the term “linear” when referring to affine functions throughout this book — location: [2521]() ^ref-893

---
One immediate connection we can observe between the training and test error is that the expected training error of a randomly selected model is equal to the expected test error of that model. Suppose we have a probability distribution p(x,y) and we sample from it repeatedly to generate the train set and the test set. For some fixed value w, the expected training set error is exactly the same as the expected test set error, because both expectations are formed using the same dataset sampling process — location: [2565]() ^ref-62098

---
Underfitting occurs when the model is not able to obtain a sufficiently low error value on the training set. Overfitting occurs when the gap between the training error and test error is too large. — location: [2576]() ^ref-58578

---
We can control whether a model is more likely to overfit or underfit by altering its capacity. Informally, a model’s capacity is its ability to fit a wide variety of functions. Models with low capacity may struggle to fit the training set. Models with high capacity can overfit by memorizing properties of the training set that do not serve them well on the test set. One way to control the capacity of a learning algorithm is by choosing its hypothesis space, the set of functions that the learning algorithm is allowed to select as being the solution. For example, the linear regression algorithm has the set of all linear functions of its input as its hypothesis space. We can generalize linear regression to include polynomials, rather than just linear functions, in its hypothesis space. Doing so increases the model’s capacity — location: [2578]() ^ref-17746

---
Regularization is any modification we make to a learning algorithm that is intended to reduce its generalization error but not its training error. — location: [2761]() ^ref-8190

---
Most machine learning algorithms have several settings that we can use to control the behavior of the learning algorithm. These settings are called hyperparameters. The values of hyperparameters are not adapted by the learning algorithm itself — location: [2775]() ^ref-38025

---
This applies to all hyperparameters that control model capacity. If learned on the training set, such hyperparameters would always choose the maximum possible model capacity, resulting in overfitting (refer to Fig. 5.3). For example, we can always fit the training set better with a higher degree polynomial and a weight decay setting of A = 0 than we could with a lower degree polynomial and a positive weight decay setting. To solve this problem, we need a validation set of examples that the training algorithm does not observe — location: [2783]() ^ref-29023

---
Specifically, we split the training data into two disjoint subsets. One of these subsets is used to learn the parameters. The other subset is our validation set, used to estimate the generalization error during or after training, allowing for the hyperparameters to be updated accordingly. The subset of data used to learn the parameters is still typically called the training set, even though this may be confused with the larger pool of data used for the entire training process. The subset of data used to guide the selection of hyperparameters is called the validation set. Typically, one uses about 80% of the training data for training and 20% for validation. Since the validation set is used to “train” the hyperparameters, the validation set error will underestimate the generalization error, though typically by a smaller amount than the training error. After all hyperparameter optimization is complete, the generalization error may be estimated using the test set. — location: [2792]() ^ref-13462

---
These procedures are based on the idea of repeating the training and testing computation on different randomly chosen subsets or splits of the original dataset. The most common of these is the k-fold cross-validation procedure, shown in Algorithm 5.1, in which a partition of the dataset is formed by splitting it into k non-overlapping subsets. The test error may then be estimated by taking the average test error across k trials. On trial i, the i-th subset of the data is used as the test set and the rest of the data is used as the training set. One problem is that there exist no unbiased estimators of the variance of such average error estimators (Bengio and Grandvalet, 2004), but approximations are typically used — location: [2808]() ^ref-25314

---
One of the most influential approaches to supervised learning is the support vector machine (Boser et al., 1992; Cortes and Vapnik, 1995). This model is similar to logistic regression in that it is driven by a linear function wT x + b. Unlike logistic regression, the support vector machine does not provide probabilities, but only outputs a class identity. The SVM predicts that the positive class is present when wTx + b is positive. Likewise, it predicts that the negative class is present when wT x + b is negative. One key innovation associated with support vector machines is the kernel trick. The kernel trick consists of observing that many machine learning algorithms can be written exclusively in terms of dot products between examples — location: [3286]() ^ref-13493

---
After replacing dot products with kernel evaluations, we can make predictions using the function f (x) = b + a ik(x, x(i)). — location: [3303]() ^ref-53505

---
model in the new transformed space. The kernel trick is powerful for two reasons. First, — location: [3308]() ^ref-38271

---
The kernel trick is powerful for two reasons. First, it allows us to learn models that are nonlinear as a function of x using convex optimization techniques that are guaranteed to converge efficiently. This is possible because we consider ^ fixed and optimize only a, i.e., the optimization algorithm can view the decision function as being linear in a different space. Second, the kernel function k often admits an implementation that is significantly more computational efficient than naively constructing two ^(x) vectors and explicitly taking their dot product. In some cases, x) can even be infinite dimensional, — location: [3308]() ^ref-65124

---
The most commonly used kernel is the Gaussian kernel k(u, v) = N (u — v ;0 , a2I) — location: [3320]() ^ref-62268

---
of the min kernel over the integers. We can think of the Gaussian kernel as performing a kind of template matching. A training example x associated with training label y becomes a template for — location: [3326]() ^ref-63837

---
We can think of the Gaussian kernel as performing a kind of template matching. A training example x associated with training label y becomes a template for class y. — location: [3327]() ^ref-30473

---
Each leaf requires at least one training example to define, so it is not possible for the decision tree to learn a function that has more local maxima than the number of training examples — location: [3377]() ^ref-48043

---
Another example of a simple representation learning algorithm is k-means clustering. The k-means clustering algorithm divides the training set into k different clusters of examples that are near each other. We can thus think of the algorithm as providing a k-dimensional one-hot code vector h representing an input x. If x belongs to cluster i, then hi = 1 and all other entries of the representation h are zero. The one-hot code provided by k-means clustering is an example of a sparse representation, — location: [3511]() ^ref-4677

---
The k-means algorithm works by initializing k different centroids {^(1),..., to different values, then alternating between two different steps until convergence. In one step, each training example is assigned to cluster i, where i is the index of the nearest centroid ^(i). In the other step, each centroid ^(i) is updated to the mean of all training examples x(j) assigned to cluster i. — location: [3523]() ^ref-3396

---
the main way to train large linear models on very large datasets. For a fixed model size, the cost per SGD update does not depend on the training set size m. In practice, we often use a larger model as the training set size increases, but we are not forced to do so. The number of updates required to reach convergence usually increases with training set size. However, as m approaches infinity, the model will eventually converge to its best possible test error before SGD has sampled every example in the training set. Increasing m further will not extend the amount of training time needed to reach the model’s best possible test error. From this point of view, one can argue that the asymptotic cost of training a model with SGD is O( 1) as a function of m. — location: [3584]() ^ref-38271

---
Prior to the advent of deep learning, the main way to learn nonlinear models was to use the kernel trick in combination with a linear model. Many kernel learning algorithms require constructing an m x m matrix Gi,j = k(x(i), x(j)). Constructing this matrix has computational cost O (m2), which is clearly undesirable for datasets with billions of examples — location: [3589]() ^ref-3084

---
Many machine learning problems become exceedingly difficult when the number of dimensions in the data is high. This phenomenon is known as the curse of dimensionality. Of particular concern is that the number of possible distinct configurations of a set of variables increases exponentially as the number of variables increases. — location: [3644]() ^ref-23245

---
Among the most widely used of these implicit “priors” is the smoothness prior or local constancy prior. This prior states that the function we learn should not change very much within a small region. Many simpler algorithms rely exclusively on this prior to generalize well, and as a result they fail to scale to the statistical challenges involved in solving AI-level tasks. — location: [3677]() ^ref-57131

---
The smoothness assumption and the associated non-parametric learning algorithms work extremely well so long as there are enough examples for the learning algorithm to observe high points on most peaks and low points on most valleys of the true underlying function to be learned — location: [3727]() ^ref-62603

---
The answer to both of these questions is yes. The key insight is that a very large number of regions, e.g., O(2k), can be defined with O(k) examples, so long as we introduce some dependencies between the regions via additional assumptions about the underlying data generating distribution. In this way, we can actually generalize non-locally (Bengio and Monperrus, 2005; Bengio et al., 2006c). Many different deep learning algorithms provide implicit or explicit assumptions that are reasonable for a broad range of AI tasks in order to capture these advantages. — location: [3733]() ^ref-16215

---
the function to be learned is smooth enough and varies in few enough dimensions. In high dimensions, even a very smooth function can change smoothly but in a different way along each dimension. If the function additionally behaves differently in different regions, it can become extremely complicated to describe with a set of training examples. If the function is complicated (we want to distinguish a huge number of regions compared to the number of examples), is there any hope to generalize well? The answer to both of these questions is yes. The key insight is that a very large number of regions, e.g., O(2k), can be defined with O(k) examples, so long as we introduce some dependencies between the regions via additional assumptions about the underlying data generating distribution. In this way, we can actually generalize non-locally (Bengio and Monperrus, 2005; Bengio et al., 2006c). Many different deep learning algorithms provide implicit or explicit assumptions that are reasonable for a broad range of AI tasks in order to capture these advantages. — location: [3729]() ^ref-722

---
The core idea in deep learning is that we assume that the data was generated by the composition of factors or features, potentially at multiple levels in a hierarchy. Many other similarly generic assumptions can further improve deep learning algorithms. These apparently mild assumptions allow an exponential gain in the relationship between the number of examples and the number of regions that can be distinguished. — location: [3743]() ^ref-31997

---
A manifold is a connected region. Mathematically, it is a set of points, associated with a neighborhood around each point. From any given point, the manifold locally appears to be a Euclidean space. In everyday life, we experience the surface of the world as a 2-D plane, but it is in fact a spherical manifold in 3-D space. — location: [3749]() ^ref-21671

---
some — location: [3832]() ^ref-23733

---
These models are called feedforward because information flows through the function being evaluated from x, through the intermediate computations used to define /, and finally to the output y. There are no feedback connections in which outputs of the model are fed back into itself. — location: [3834]() ^ref-30719

---
Feedforward networks are of extreme importance to machine learning practitioners. They form the basis of many important commercial applications. For example, the convolutional networks used for object recognition from photos are a specialized kind of feedforward network. — location: [3839]() ^ref-15049

---
Feedforward neural networks are called networks because they are typically represented by composing together many different functions. The model is associated with a directed acyclic graph describing how the functions are composed together — location: [3842]() ^ref-25557

---
The training examples specify directly what the output layer must do at each point x; it must produce a value that is close to y. The behavior of the other layers is not directly specified by the training data. The learning algorithm must decide how to use those layers to produce the desired output, but the training data does not say what each individual layer should do. Instead, the learning algorithm must decide how to use these layers to best implement an approximation of f *. — location: [3853]() ^ref-50627

---
One way to understand feedforward networks is to begin with linear models and consider how to overcome their limitations. Linear models, such as logistic regression and linear regression, are appealing because they may be fit efficiently and reliably, either in closed form or with convex optimization. Linear models also have the obvious defect that the model capacity is limited to linear functions, so the model cannot understand the interaction between any two input variables. To extend linear models to represent nonlinear functions of x, we can apply the linear model not to x itself but to a transformed input ^(x), where ^ is a nonlinear transformation. Equivalently, we can apply the kernel trick — location: [3870]() ^ref-63469

---
One option is to use a very generic ^>, such as the infinite-dimensional ^ that is implicitly used by kernel machines based on the RBF kernel. If ^(x) is of high enough dimension, we can always have enough capacity to fit the training set, but generalization to the test set often remains poor — location: [3877]() ^ref-4404

---
local smoothness and do not encode enough prior information — location: [3880]() ^ref-60305

---
Another option is to manually engineer ^. Until the advent of deep learning, this was the dominant approach. This approach requires decades of human effort for each separate task, with practitioners specializing in different domains — location: [3881]() ^ref-4752

---
Clearly, we must use a nonlinear function to describe the features. Most neural networks do so using an affine transformation controlled by learned parameters, followed by a fixed, nonlinear function called an activation function. We use that strategy here, by defining h = g( WTx + c), where W provides the weights of a linear transformation and c the biases — location: [3941]() ^ref-31593

---
The rectified linear activation function. This activation function is the default activation function recommended for use with most feedforward neural networks. Applying this function to the output of a linear transformation yields a nonlinear transformation. However, the function remains very close to linear, in the sense that is a piecewise linear function with two linear pieces — location: [3989]() ^ref-12198

---
This means that neural networks are usually trained by using iterative, gradient-based optimizers that merely drive the cost function to a very low value, rather than the linear equation solvers used to train linear regression models or the convex optimization algorithms with global convergence guarantees used to train logistic regression or SVMs — location: [4026]() ^ref-39178

---
For feedforward neural networks, it is important to initialize all weights to small random values. The biases may be initialized to zero or to small positive values. — location: [4031]() ^ref-59045

---
Most modern neural networks are trained using maximum likelihood. This means that the cost function is simply the negative log-likelihood, equivalently described — location: [4057]() ^ref-55088

---
called mean absolute error. Unfortunately, mean squared error and mean absolute — location: [4115]() ^ref-35289

---
Unfortunately, mean squared error and mean absolute error often lead to poor results when used with gradient-based optimization. Some output units that saturate produce very small gradients when combined with these cost functions. This is one reason that the cross-entropy cost function is more popular than mean squared error or mean absolute error, even when it is not necessary to estimate an entire distribution p(y | x). — location: [4116]() ^ref-59708

---
Maximizing the log-likelihood is then equivalent to minimizing the mean squared error. — location: [4138]() ^ref-21415

---
A Bernoulli distribution is defined by just a single number. The neural net needs to predict only P(y = 1 | x). For this number to be a valid probability, it must lie in the interval [0, 1] — location: [4147]() ^ref-56223

---
We can think of the sigmoid output unit as having two components. First, it uses a linear layer to compute z = wTh + b. Next, it uses the sigmoid activation function to convert z into a probability. — location: [4160]() ^ref-13513

---
Any time we wish to represent a probability distribution over a discrete variable with n possible values, we may use the softmax function. This can be seen as a generalization of the sigmoid function which was used to represent a probability distribution over a binary variable. Softmax functions are most often used as the output of a classifier, to represent the probability distribution over n different classes — location: [4195]() ^ref-9948

---
The universal approximation theorem means that regardless of what function we are trying to learn, we know that a large MLP will be able to represent this function. However, we are not guaranteed that the training algorithm will be able to learn that function. Even if the MLP is able to represent the function, learning can fail for two different reasons. First, the optimization algorithm used for training may not be able to find the value of the parameters that corresponds to the desired function. Second, the training algorithm might choose the wrong function due to overfitting. Recall from Sec. 5.2.1 that the “no free lunch” theorem shows that there is no universally superior machine learning algorithm. Feedforward networks provide a universal system for representing functions, in the sense that, given a function, there exists a feedforward network that approximates the function — location: [4550]() ^ref-36092

---
backprop, allows the information from the cost to then flow backwards through the network, in order to compute the gradient. — location: [4661]() ^ref-49719

---
The term back-propagation is often misunderstood as meaning the whole learning algorithm for multi-layer neural networks. Actually, back-propagation refers only to the method for computing the gradient, while another algorithm, such as stochastic gradient descent, is used to perform learning using this gradient. Furthermore, back-propagation is often misunderstood as being specific to multilayer neural networks, but in principle it can compute derivatives of any function — location: [4664]() ^ref-10222

---
In the context of deep learning, most regularization strategies are based on regularizing estimators. Regularization of an estimator works by trading increased bias for reduced variance. An effective regularizer is one that makes a profitable trade, reducing variance significantly while not overly increasing the bias — location: [5224]() ^ref-31435

---
The best way to make a machine learning model generalize better is to train it on more data. Of course, in practice, the amount of data we have is limited. One way to get around this problem is to create fake data and add it to the training set. For some machine learning tasks, it is reasonably straightforward to create new fake data. This approach is easiest for classification. A classifier needs to take a complicated, high dimensional input x and summarize it with a single category identity y. This means that the main task facing a classifier is to be invariant to a wide variety of transformations. We can generate new (x, y) pairs easily just by transforming the x inputs in our training set — location: [5536]() ^ref-2284

---
Instead of running our optimization algorithm until we reach a (local) minimum of validation error, we run it until the error on the validation set has not improved for some amount of time. Every time the error on the validation set improves, we store a copy of the model parameters. When the training algorithm terminates, we return these parameters, rather than the latest parameters. — location: [5677]() ^ref-27125

Early stopping

---
In convolutional network terminology, the first argument (in this example, the function x )to the convolution is often referred to as the input and the second argument (in this example, the function w) as the kernel. The output is sometimes referred to as the feature map — location: [7773]() ^ref-21710

---
