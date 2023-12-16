# CS769HW5

# Installation
Clone this repository
'git clone'
Install Python 3.8.1, and ask the original author for access to the datasets and checkpoint
- Pretrained model: panglao_pretrain.pth
- Datasets: panglao_10000.h5ad, Zheng68K.h5ad
- Gene embedding: gene2vec_16906.npy
***
- dist_finetune_fewshot.py: run scBERT fine-tuning on 10%, 25%, 50%, 75%, and 100% of the training data
- dist_finetune.py: used to run fine-tuning (cell type annotation) for scBERT, an example command line call:
  
'''
python dist_finetune.py --model_name finetune_seed2021 --data_path <path to preprocessed h5ad for fine-tuning> --model_path <path to pre-trained model> --world_size=1 --seed=2021 --epochs=10 --grad_acc=1 --batch_size=32 --pos_embed_g2v
'''

  

