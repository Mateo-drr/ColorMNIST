# ColorMNIST
Code to recreate the Color MNIST dataset used in Invariant Risk Minimization - https://arxiv.org/pdf/1907.02893.pdf

This code was taken from https://colab.research.google.com/github/reiinakano/invariant-risk-minimization/blob/master/invariant_risk_minimization_colored_mnist.ipynb?authuser=2#scrollTo=EwUoQZCyvs6T and it was updated and compared to the actual implementation from the paper.

To use the code simply do the following:

    import CMNIST as dl

Create datasets for training and test environments

    train_dataset_1 = dl.ColoredMNIST(root=path, env='train1', transform=transform)
    train_dataset_2 = dl.ColoredMNIST(root=path, env='train2', transform=transform)
    test_dataset = dl.ColoredMNIST(root=path, env='test', transform=transform)
    
Create data loaders

    train_loader_1 = torch.utils.data.DataLoader(train_dataset_1, batch_size=bsize, shuffle=True,pin_memory=True)
    train_loader_2 = torch.utils.data.DataLoader(train_dataset_2, batch_size=bsize, shuffle=True)
    test_loader = torch.utils.data.DataLoader(test_dataset, batch_size=bsize, shuffle=False)
