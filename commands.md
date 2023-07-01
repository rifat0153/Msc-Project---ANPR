### Create a new environment

conda create --name tf python=3.9

### Tensforflow Gpu Installation with CUDA 11.2 as TF Windows Native only supports upto CUDA 11.2

conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1.0
conda install -c conda-forge cudatoolkit=10.2 cudnn=7.6.5
pip install --upgrade pip

### Anything above 2.10 is not supported on the GPU on Windows Native

pip install "tensorflow<2.11"

#### Verify the GPU setup:

python -c "import tensorflow as tf; print(tf.config.list_physical_devices('GPU'))"

If a list of GPU devices is returned, you've installed TensorFlow successfully.

### Install Pytorch with CUDA 11.2 as TF requires CUDA 11.2 on Windows Native

```bash
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```

Looking in indexes: https://download.pytorch.org/whl/cu118

conda install pytorch=1.8.2 torchvision torchaudio cudatoolkit=10.2 cudnn=7.6.5 -c pytorch -c conda-forge

### Common Git Commands

Ignore File Endings

git config --global core.autocrlf false
Ignore File Permissions

git config core.fileMode false
Ignore File Endings and File Permissions

git config --global core.autocrlf false && git config core.fileMode false
Reset Git Cache

git rm -r --cached . && git add .

```

```
