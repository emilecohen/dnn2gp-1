# From Deep Neural Network to Gaussian Process (dnn2gp)
![dnn2gp schema](https://github.com/team-approx-bayes/dnn2gp/blob/master/figures/dnn2gp_schema.png)

This repository contains code to reproduce results for the paper *Approximate Inference Turns Deep Networks into Gaussian Processes*

### Computing and Visualizing Linear Model and GP

### Reproducing Model Selection Experiments

The results are readily available in directory `/results` and can be reproduced by running
```bash
python marglik.py --name of_choice
```

This will produce both toy and real world experiments and save the corresponding measurements
to the results directory with a new filename. The plots can then be generated by running
```bash
python marglik_plots.py --name original  # use our result files
python marglik_plots.py --name of_choice  # use your result files
```

### Computing and Visualizing Kernels and Predictive Distribution

We use pre-trained models that are saved in the `/models` directory and are trained on 
either CIFAR-10 or MNIST. The plots produced in our paper can be reproduced by running
```bash
python kernel_predist.py
```
Further, the module `dnn2gp.kernel_distributions` allows to compute relevant quantities
for any pytorch neural network and corresponding data loader. If the full training set is
passed, the Laplace approximation can also be computed.

(TODO: add the structure and methods here with a short explanation)

### Requirements

python 3.x with `requirements.txt`.
