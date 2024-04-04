# Variables & Symbols:

- $x, y, z$ : Variables - A variable is a symbol that represents a quantity
- $i, j, k$ : Indices - Indices are used to index elements in a vector, matrix, or tensor
- $n, m$ : Dimensions - The number of rows and columns in a matrix
- $N$ : Dimension - The number of elements in a vector, matrix, or tensor
- $a, b, c$ : Constants - A constant is a symbol that represents a fixed value
- $\pi$ : Pi - Represents the ratio of the circumference of a circle to its diameter
- $e$ : Euler's number - Represents the base of the natural logarithm
- $\delta$ : Delta - Represents the difference between two values
- $\epsilon$ : Epsilon - Represents a small quantity, approaching zero
- $\sum$ : Sigma - Summation over a collection of elements
- $\prod$ : Product - Product over a collection of elements

# Numerical Objects:

- $x$ : a scalar - A single number.
- $\mathbf{x}$ : a vector - An ordered array of numbers
- $\mathbf{X}$ : a matrix - An ordered 2D array of numbers
- $\mathsf{X}$ : a tensor - An ordered n-dimensional array of numbers
- $\mathbf{I}$ : an identity matrix - A square matrix with ones on the diagonal (from top left to bottom right) and zeros elsewhere
- $x_i$ : the $i$-th element of a vector
- $[\mathbf{X}]_{ij}$ : the element of a matrix at row $i$ and column $j$

# Set Theory:

- $\mathcal{X}$ : a set - A set is a collection of elements
- $\mathbb{Z}$ : a set of integers - A set of integers is a collection of whole numbers, including both positive and negative integers
- $\mathbb{Z}^+$ : a set of positve integers, excluding zero
- $\mathbb{R}$ : a set of real numbers - A set of real numbers is a collection of numbers that include both positive and negative numbers, as well as zero
- $\mathbb{R}^n$ : a set of $n$-dimensional vectors of real numbers
- $\mathbb{R}^{a\times b}$ : The set of matrices of real numbers with $a$ rows and $b$ columns
- $|\mathcal{X}|$ : The cardinality (number of elements) of set $\mathcal{X}$
- $\mathcal{A}\cup\mathcal{B}$ : union of sets $\mathcal{A}$ and $\mathcal{B}$
- $\mathcal{A}\cap\mathcal{B}$ : intersection of sets $\mathcal{A}$ and $\mathcal{B}$
- $\mathcal{A}\setminus\mathcal{B}$ : set subtraction of $\mathcal{B}$ from $\mathcal{A}$ (contains only those elements of $\mathcal{A}$ that are not in $\mathcal{B}$)

# Functions and Operators:

- $f(\cdot)$ : a function
- $\log(\cdot)$ : the natural logarithm (base $e$)
- $\log_2(\cdot)$ : logarithm to base $2$
- $\exp(\cdot)$ : exponential function
- $\mathbf{1}(\cdot)$ : the indicator function; evaluates to $1$ if the boolean argument is true, and $0$ otherwise
- $\mathbf{1}_{\mathcal{X}}(z)$ : the set-membership indicator function; evaluates to $1$ if the element $z$ belongs to the set $\mathcal{X}$, and $0$ otherwise
- $\mathbf{(\cdot)}^\top$ : transpose of a vector or a matrix
- $\mathbf{X}^{-1}$ : the inverse of a matrix $\mathbf{X}$
- $\odot$ : Hadamard (elementwise) product
- $[\cdot, \cdot]$ : concatenation
- $\|\cdot\|_p$ : $\ell_p$ norm
- $\|\cdot\|$ : $\ell_2$ norm
- $\langle \mathbf{x}, \mathbf{y} \rangle$ : inner (dot) product of vectors $\mathbf{x}$ and $\mathbf{y}$
- $\stackrel{\textrm{def}}{=}$ : an equality asserted as a definition of the symbol on the left-hand side

# Calculus:

- $\frac{dy}{dx}$ : derivative of $y$ with respect to $x$
- $\frac{\partial y}{\partial x}$ : partial derivative of $y$ with respect to $x$
- $\nabla_{\mathbf{x}} y$ : gradient of $y$ with respect to $\mathbf{x}$
- $\int_a^b f(x) \;dx$ : definite integral of $f$ from $a$ to $b$ with respect to $x$
- $\int f(x) \;dx$ : indefinite integral of $f$ with respect to $x$

# Probability and Information Theory:

- $X$ : a random variable
- $P$ : a probability distribution
- $X \sim P$ : $X$ is a random variable with distribution $P$
- $P(X=x)$ : the probability of the event where $X$ takes the value $x$
- $P(X \mid Y)$ : the conditional probability of $X$ given $Y$
- $p(\cdot)$ : a probability density function (PDF) associated with distribution $P$
- ${E}[X]$ : the expected value of $X$
- $X \perp Y$ : $X$ and $Y$ are independent
- $X \perp Y \mid Z$ : $X$ and $Y$ are conditionally independent given $Z$
- $\sigma_X$ : the standard deviation of $X$
- $\textrm{Var}(X)$ : the variance of $X$ equal to $\sigma_X^2$
- $\textrm{Cov}(X, Y)$ : the covariance of $X$ and $Y$
- $\rho(X, Y)$ : the Pearson correlation of $X$ and $Y$, equals $\frac{\textrm{Cov}(X, Y)}{\sigma_X \sigma_Y}$
- $H(X)$ : entropy of $X$
- $D_{\textrm{KL}}(P\|Q)$ : he KL-divergence (or relative entropy) from distribution $Q$
 to distribution $P$