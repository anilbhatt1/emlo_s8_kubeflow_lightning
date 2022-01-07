# emlo_s8_kubeflow_lightning
### Added below PyTorch Lightning features to kubeflow pipeline

- Modified **pytorch_cifar10.yaml** file for the same.
![image](https://user-images.githubusercontent.com/43835604/148549790-0ae0ff71-fe0a-4128-a744-fe5183ab1f86.png)

### Following features were added:

- max_epochs=3 -> Train and validate for 3 epochs 
- accumulate_grad_batches=2 -> Perform backpropagation for 2 batches instead of every 1 batch
- overfit_batches=10 -> Select 10 batches & train/validate only for 10 batches across the 3 epochs. This is a debugging technique to see model is working properly.
- progress_bar_refresh_rate=2 -> Will show the progress for every 2 batches. Default is 1.
- flush_logs_every_n_steps=4 -> Will write the logs to disk every 4 batches. Default is 100. Chosen low number of 4 since only 10 batches are train/validated here.
- log_every_n_steps=2 -> Will log training on every 2 batches. Default is 10.

### Snapshot of training logs

- Log File (training) can be seen below

[pytorch_cifar10_v4_jan7_r1.txt](https://github.com/anilbhatt1/emlo_s8_kubeflow_lightning/files/7829055/pytorch_cifar10_v4_jan7_r1.txt)

- Snapshot of kubeflow run

![image](https://user-images.githubusercontent.com/43835604/148550789-f87399bf-3118-4ca5-b741-8a6e506889e4.png)

- Config of kubeflow run

![image](https://user-images.githubusercontent.com/43835604/148551444-3857db55-d60d-47ae-8176-ebc8a1480ab2.png)

- Snapshot of kubeflow training logs (same as txt file above) **Snap-1**

![image](https://user-images.githubusercontent.com/43835604/148551168-fa75f9b1-6c64-43b5-a73c-4a0afd3cf8c0.png)

- Snapshot of kubeflow training logs (same as txt file above) **Snap-2**

![image](https://user-images.githubusercontent.com/43835604/148551236-df493cfe-c99f-485e-acaf-0965d78f0b68.png)

- Snapshot of kubeflow training logs (same as txt file above) **Snap-3**

![image](https://user-images.githubusercontent.com/43835604/148551277-d5759f5f-5782-4b26-8a53-20525c93ef52.png)



