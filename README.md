# SPN
Implementation of learned index using spn

SPN Implementation :
i. Using the pandas module's pd.read_csv function, we download an integer dataset that we uploaded
in GitHub. A NumPy array is created from a dataframe using the to_numpy() method.

ii. train_data is used to train the SPN, and test_data is used to assess the effectiveness of the newly
trained model. Next, we read the train_data numpy array's form to determine how many variables
are included in the dataset, and we generate a Context object from the spn.structure.

iii. Base module, which details the kinds of parametric distributions to be applied in the SPN. For every
variable in the dataset, we used Gaussian distributions. The context of the variables' domains is
added using the add_domains method.

iv. The learn_parametric() function from the spn.algorithms.Learning.Wrappers is then used to learn
a parametric SPN.Module. The function returns an SPN model after accepting the training data
and the context object as parameters. The variables start_time and end_time are used to calculate
how long it took to assemble the SPN.

v. Using the plot_spn() function from the spn.io.Graphics module, we plot the learned SPN.
'basicspn.png' is the filename given to the plot's PNG representation.

vi. A log-likelihood computation for a certain SPN (Sum-Product Network) model and test dataset is
then timed and memory-tested.

References:
Anon. [2018] 2023. “SPFlow: An Easy and Extensible Library for Sum-Product Networks.”
