Goal: design a universal test to evaluate the efficiency of ML algorithms such as: Normalization (batch norm), regularization (L1, L2, Dropout, data augmentation, early stopping), optimizer(gradient descent, adam, momentum)We also need a test for architectureUsing that test, we'll compile a table of efficiency for future reference.Specifications:
	* The base network should achieve about 95% accuracy because this test is to test the efficiency in final tweaks. Because to get to 95% is easy, you only need to make the network complicated enough
	* Test training time (until reaching plateau)
	* Test increase in accuracy
	* Test decrease in loss
	* The same random state
	* No learning rate tweaking because it make the training time difference meaningless

Nominations:
	* MNIST: chỉnh mãi thì được 97.2-99.5. Thấp hơn được thì đẹp. Architecture hiện tại rất đẹp, chỉ có 

Let's drop something:
*Drop training time
*Keep n_epochs fixed
*Only log accuracy and loss. Focus especially on loss
*So that, for my sake, it ends.

