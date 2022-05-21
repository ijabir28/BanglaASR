# Bangla Speech Recognition using deepspeech.pytorch


Implementation of Bangla Speech Recognition using DeepSpeech2 for PyTorch using [PyTorch Lightning](https://github.com/PyTorchLightning/pytorch-lightning).
## Install

Several libraries are needed to be installed for training to work. I will assume that everything is being installed in
an Anaconda installation on Ubuntu, with PyTorch installed.

Install [PyTorch](https://github.com/pytorch/pytorch#installation) if you haven't already.

```
pip install -r requirements.txt
pip install -e . # Dev install
```

## Training Commands

```bash
cd data/ && python bengali_asr.py && cd ..

python train.py +configs=bangla_asr
```

## Testing Commands

To evaluate the trained model on the test set:

```
python test.py model.model_path=models/deepspeech.pth test_path=bangla_asr_test_manifest.json
```
