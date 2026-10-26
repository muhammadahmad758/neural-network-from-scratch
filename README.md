# A Neural Network From Scratch
This was written for my blog post [Machine Learning for Beginners: An Introduction to Neural Networks](https://victorzhou.com/blog/intro-to-neural-networks/).

## Usage

Install [numpy](http://www.numpy.org/), the only dependency, if you need to:

```bash
$ pip install numpy
```

Then, run it with no arguments:

```bash
$ python network.py
```

You can also [run this code in your browser](https://repl.it/@vzhou842/An-Introduction-to-Neural-Networks).

## More

You may also be interested in [a Convolutional Neural Network (CNN) implemented from scratch in Python](https://github.com/vzhou842/cnn-from-scratch), which was written for my [introduction to CNNs](https://victorzhou.com/blog/intro-to-cnns-part-1/).

---

## My Changes in This Fork

This is a learning fork by **Muhammad Ahmad Farooq**, a BS Artificial Intelligence student at FUUAST Islamabad. The original project is by Victor Zhou — see the link at the top of this README. This fork keeps the original code, comments, and the MIT license, and adds the changes below so I can experiment with the network and learn how it behaves.

### What I changed

- **Configurable training:** `train()` now accepts `learn_rate` and `epochs` as parameters instead of hard-coded values (defaults are unchanged: 0.1 and 1000).
- **Command-line options:** the demo now runs through `main()`, so the settings can be changed without editing the code:

  ```bash
  $ python network.py --epochs 500 --learn-rate 0.05 --seed 42
  ```

- **Reproducible runs:** the new `--seed` option fixes the random starting weights, so the same command gives the same result every time — important for comparing experiments fairly.
- **Accuracy report:** after training, the script prints the training accuracy (what percentage of the training examples the network classifies correctly, using 0.5 as the cutoff), not just the loss.

### What I learned from this change

- *Epochs* and *learning rate* are hyperparameters: small changes to them visibly change how fast the loss falls and how confident the final predictions are.
- Without a fixed seed, the same code gives slightly different results on every run, because the starting weights are random.
- Loss alone does not tell the whole story — an accuracy figure is easier to understand and compare.
