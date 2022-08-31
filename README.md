# yoga-82-scmcl-ypc

# Supervised Contrastive Multi-tasking learning For Hierarchical Yoga Pose Classification

This repository implements supervised contrastive loss in combination with cross entropy loss for yoga pose classification.

### Train:

This package needs an input txt file with the data list for training and testing. To initiate the stage-1 training, please use the below command.

 > python yoga_classification_training_scmcl_stage1.py -a effnetv2_s --epochs 300 --gpu-id 0 -c >path where checkpoints to be saved< --train-batch 15 --test-batch 2 --optuna_study_db sqlite:///./>path where optuna db to be saved<
 
 To initiate stage-2 training, please use the below command.
 
 > python yoga_classification_training_stage2.py -a effnetv2_s --epochs 300 --gpu-id 0 -c >path where checkpoints to be saved< --train-batch 26 --test-batch 13 --weights_load >path to the best model saved from stage-1<  --optuna_study_db sqlite:///./>path where optuna db to be saved<
 
 
### Architecture Overview:

Utilized training architecture overview is given here.
<img src="/images/training_methodology.jpg?" width="90%" >
  
The detailed network architecture information is given below:

<img src="/images/Table1.png?" width="70%" >

Building blocks used in the network architecture is described below:

<img src="/images/building_blocks.jpg?" width="60%" >

### Results:

Evaluation results comparison with SOTA methodologies is given in the below table:

<img src="/images/Table2.png?" width="70%" >

Ablation studies evaluation results is given in the below table:

<img src="/images/Table3.png?" width="70%" >

T-SNE results comparison with cross entropy loss is provided below:

<img src="/images/tsne_plot.jpg?" width="70%" >


For trained network models please contact the author.
