# Resnet18-for-cifar10
## project: Resnet18 for cifar10 with pytorch
### Homework: Tuning a hyper-parameter and analyzing its effects on performance and writing a README.md to report your findings.
    对于此次作业，我选取了epoch和LR两个超参数进行实验分析。首先介绍所选取的两个超参数的含义：epoch是指迭代轮数，即遍历数据集的次数；LR是手动给定的学习率
    实验分别进行了四次，每次epoch和LR的取值组成都不同，分别如下：
      1、epoch = 10, LR = 0.01
      2、epoch = 10, LR = 0.001
      3、epoch = 20, LR = 0.01
      4、epoch = 20, LR = 0.001
    经过分析每次实验的epoch准确度和最佳准确度来设置更好的超参数值，结论如下：
      1、当epoch不变，而减少学习率时，模型拟合较慢，epoch = 10的时候LR = 0.01效果更好，而epoch = 20的时候LR = 0.001效果更好(因为迭代轮数增加，模型训练次数增加，使模型更加拟合数据),
    epoch = 10, LR = 0.001时效果最差，模型欠拟合。
      2、当LR不变，而增加迭代轮数时模型表现会提升， 但是提升不算特别明显，而且超过20个epoch后，模型开始往过拟合的方向发展。
    最后经过实验分析，得出了较好的超参数组合，即epoch = 20, LR = 0.001, 每个epoch的精度如下：
      EPOCH=001,Accuracy= 53.080%
      EPOCH=002,Accuracy= 69.380%
      EPOCH=003,Accuracy= 73.820%
      EPOCH=004,Accuracy= 79.410%
      EPOCH=005,Accuracy= 79.730%
      EPOCH=006,Accuracy= 82.140%
      EPOCH=007,Accuracy= 79.750%
      EPOCH=008,Accuracy= 81.440%
      EPOCH=009,Accuracy= 85.110%
      EPOCH=010,Accuracy= 86.680%
      EPOCH=011,Accuracy= 84.860%
      EPOCH=012,Accuracy= 86.640%
      EPOCH=013,Accuracy= 87.920%
      EPOCH=014,Accuracy= 86.950%
      EPOCH=015,Accuracy= 87.270%
      EPOCH=016,Accuracy= 88.900%
      EPOCH=017,Accuracy= 87.500%
      EPOCH=018,Accuracy= 89.260%
      EPOCH=019,Accuracy= 88.890%
      EPOCH=020,Accuracy= 88.950%
    其中最好的结果在第18个epoch，即EPOCH=018,Accuracy= 89.260%, 综上可以得出，超参数的搭配非常考究，不仅需要相关基础知识，还要进行很多实验，必须理论结合实践才可以找到更优秀的超参数设置。
