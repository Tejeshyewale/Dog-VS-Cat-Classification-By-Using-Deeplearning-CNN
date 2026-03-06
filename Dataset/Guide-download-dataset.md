# Dataset Download Guide (Kaggle)

This project uses a dataset hosted on Kaggle. Because large datasets cannot be stored directly on GitHub, follow the steps below to download the dataset locally.

## 1. Install Kaggle API

Install the Kaggle Python package:

```bash
pip install kaggle
```

## 2. Create Kaggle API Token

1. Go to [https://www.kaggle.com](https://www.kaggle.com)
2. Sign in to your account.
3. Click your profile icon → **Settings**.
4. Scroll to the **API** section.
5. Click **Create New API Token**.

A file named `kaggle.json` will be downloaded.

## 3. Configure Kaggle API

Move the API key to the Kaggle configuration folder:

```bash
mkdir ~/.kaggle
mv kaggle.json ~/.kaggle/
chmod 600 ~/.kaggle/kaggle.json
```

## 4. Download the Dataset

Use the following command to download the dataset:

```bash
kaggle datasets download -d <dataset-owner>/<dataset-name>
```

Example:

```bash
kaggle datasets download -d username/dataset-name
```

## 5. Extract the Dataset

Unzip the dataset file:

```bash
unzip dataset-name.zip
```

## 6. Expected Dataset Structure

For image classification projects, the dataset should follow this structure:

```
dataset/
 ├── train/
 │   ├── class1/
 │   ├── class2/
 │   └── class3/
 ├── test/
 │   ├── class1/
 │   ├── class2/
 │   └── class3/
```

Each class must be inside its own folder so that deep learning frameworks like TensorFlow or PyTorch can automatically assign labels.

## Note

Large datasets are not uploaded to GitHub repositories due to size limitations. Instead, this guide allows users to download the dataset directly from Kaggle.
