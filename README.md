# 2048-rl

Deep Q-Learning Project to play 2048.

## Getting Started

Install [TensorFlow](https://www.tensorflow.org/versions/r0.8/get_started/index.html), python & pip.
Then, run:

```bash
pip install -r requirements.txt
```

To run the code, you'll need to update your `PYTHONPATH`:

```bash
source set_pythonpath.sh
```

Now, you should be able to run the tests:

```bash
py.test
```

## Source Code Structure

All python source code lives in `py_2048_rl`.

### game

This directory contains code to simulate the 2048 game itself.
For example, it provides a `Game` class that implements the game logic.
The `play` module defines the `Experience` class, a `play()` function and various strategies that can be passed as an argument to `play()`.

### learning

This directory contains all code that has to do with the Deep Q-Learning algorithm itself.
`model` defines the Neural Network; `learning` implements the Deep Q-Learning algorithm.

## Run Training

Step 1 is to set various parameters.
For example, you might want to adjust the training directory in `learning.py`, the `GAMMA` value in `experience_batcher.py` or model parameters & the learning rate in `model.py`.

Once that's done, you can simple run `python py_2048_rl/learning.py`.

## Analyzing the Model

You can use TensorBoard to monitor your Network training, simply by passing you train directory as the `--logdir` param.
Furthermore, have a look at `py_2048_rl/analisis.py` (for plotting a historgram of Q-Values) and `py_2048_rl/play_game.py` (for simulating a (number of) games given a particular model).
