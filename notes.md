  - [Goal is to achieve as general a model as possible by making predictions for new data](#sec-1)
    - [Root Mean Square error is used as error function, the mean allows us to compare errors from datasets of different sizes and the root keeps the error within the same scale](#sec-1-1)
    - [A higher order polynomial contains all lower order polynomials as special cases. In that case shouldn't higher order polynomials provide better generalisation to fitting a dataset? We notice that as the order increases, the parameter values assume large +ve or -ve values. This happens because with the increased flexibility, the polynomial can easily fit to the random noise on the data. Hence the predictive power of the model decreases as the test errors shoot up. This is a case of **over-fitting**.](#sec-1-2)
    - [Larger the dataset, more complex the model that we can reliably fit to it. This is because the model has less chance of fitting to random noise between data points when there are many data points.](#sec-1-3)
    - [*Regularisation* can be used to control over-fitting](#sec-1-4)
  - [Probability Theory](#sec-2)
    - [Probability of an event is the fraction of times the event occurs out of the total number of trials in the limit that the number of trials approaches infinity](#sec-2-1)
    - [If events are mutually exclusive and exhaustive, their probabilities sum to 1.](#sec-2-2)
    - [*Sum rule of probability* - how we marginalise out a random variable by summing over its states](#sec-2-3)
    - [*Product rule of probability* - joint probability is a product of the conditional probability and the marginal probability](#sec-2-4)
    - [Prior probability - available knowledge before making an observation](#sec-2-5)
    - [Posterior probability - prior updated with observation probability, normalised by the marginal of the observation](#sec-2-6)
    - [*independence* - joint probability factorises into a product of the marginals, p(A|B) = p(A)](#sec-2-7)

# Goal is to achieve as general a model as possible by making predictions for new data     :ML:<a id="sec-1"></a>

<span class="timestamp-wrapper"><span class="timestamp">[2019-01-04 Fri 13:36]</span></span>

## Root Mean Square error is used as error function, the mean allows us to compare errors from datasets of different sizes and the root keeps the error within the same scale<a id="sec-1-1"></a>

## A higher order polynomial contains all lower order polynomials as special cases. In that case shouldn't higher order polynomials provide better generalisation to fitting a dataset? We notice that as the order increases, the parameter values assume large +ve or -ve values. This happens because with the increased flexibility, the polynomial can easily fit to the random noise on the data. Hence the predictive power of the model decreases as the test errors shoot up. This is a case of **over-fitting**.<a id="sec-1-2"></a>

## Larger the dataset, more complex the model that we can reliably fit to it. This is because the model has less chance of fitting to random noise between data points when there are many data points.<a id="sec-1-3"></a>

## *Regularisation* can be used to control over-fitting<a id="sec-1-4"></a>

1.  Prevent parameters from shooting to high values, prevents fitting to random noise

2.  Add penalty term to loss function

3.  simplest penalty is sum of squares of weights, scaled by a parameter \[ \lambda \] which controls how much weight is given to the penalty term

4.  *Shrinkage*, *ridge regression* in case of quadratic regulariser, *weight decay* in case of neural networks

5.  the parameter needs to be tuned to data. It controls the degree of over-fitting

# Probability Theory     :ML:<a id="sec-2"></a>

<span class="timestamp-wrapper"><span class="timestamp">[2019-01-04 Fri 14:44]</span></span>

## Probability of an event is the fraction of times the event occurs out of the total number of trials in the limit that the number of trials approaches infinity<a id="sec-2-1"></a>

## If events are mutually exclusive and exhaustive, their probabilities sum to 1.<a id="sec-2-2"></a>

## *Sum rule of probability* - how we marginalise out a random variable by summing over its states<a id="sec-2-3"></a>

## *Product rule of probability* - joint probability is a product of the conditional probability and the marginal probability<a id="sec-2-4"></a>

## Prior probability - available knowledge before making an observation<a id="sec-2-5"></a>

## Posterior probability - prior updated with observation probability, normalised by the marginal of the observation<a id="sec-2-6"></a>

## *independence* - joint probability factorises into a product of the marginals, p(A|B) = p(A)<a id="sec-2-7"></a>
