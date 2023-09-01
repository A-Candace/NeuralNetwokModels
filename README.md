# NeuralNetwokModels
These are all the models (Graph Wavenet, FNN, RNN, CNN, Poisson GLM) used in the new study.

To run the Graph Wavenet:

The codes shown to get R2 for each node.

1. Create a folder on your PC

2. Upload all Python files into your folder
There are two data folders needed. I labeled them "timeseries 3" (predictors) and "timeseries 4" (response). These folders need to be in the folder with your Python files.

I used Anaconda and edited codes in Spyder. Follow these commands in the CMD.exe prompt.

1. python readcamelsRFNoNormalize3.py --seq 3 --addstatics --forcingtype timeseries3

2. python camel_linkpredictr23.py

3. python trainwavenetwur2eachbasin.py --retrain --L1Loss --seed 3031601 --addstatics --in_dim 19 --addaptadj --apt_size 10 --adjtype doubletransition --runtesting --forcingtype timeseries3 --latenttype full --learnrate 5e-4 --weight_decay 1e-5 --nepoch 30 --seq 3 --batch_size 30 --netlatent 15 --netcutoff 98 --hiddensize 19 --gcn_bool --similarity "euclidean" --nhid 19 --dropout 0.3 --clipnorm 1.0
