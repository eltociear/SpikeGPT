# SpikeGPT: Generative Pre-trained Language Model with Spiking Neural Networks

<p align="center" float="center">
  <img src="https://github.com/ridgerchu/SpikeGPT/blob/master/static/spikegpt.png"/>
</p>

SpikeGPT is a lightweight generative language model with pure binary, event-driven spiking activation units.

If you are interested in SpikeGPT, feel free to join our Discord by this [link](https://discord.gg/gdUpuTJ6QZ)!

This repo is inspired by the [RWKV-LM](https://github.com/BlinkDL/RWKV-LM).

## Training on Enwik8

1. Download the [enwik8 dataset](https://data.deepai.org/enwik8.zip).
2. Run `train.py`

## Inference with Prompt

You can choose to inference with your customized model or with our pre-trained model, our pre-trained model on BookCorpus is avaiable [here](https://huggingface.co/ridger/SpikeGPT-BookCorpus/blob/main/BookCorpus-SpikeGPT.pth). This model only trained 900M token on BookCorpus.

1. Modify the hyper-parameter of the network, which could be found in line 36-38 of the `run.py`:
```python
# For BookCorpus pre-trained model, you can change it if you trained your own model.
n_layer = 18
n_embd = 512
ctx_len = 1024
```
2. download our BookCorpus pre-trained model, and put it in thein the root directory of this repo.
3. Modify the  'context' variable in `run.py` to your custom prompt
4. Run `run.py`



## Citation


If you find SpikeGPT useful in your work, please cite the following source:

```
@article{zhu2023spikegpt,
        title = {SpikeGPT: Generative Pre-trained Language Model with Spiking Neural Networks},
        author = {Zhu, Rui-Jie and Zhao, Qihang and Eshraghian, Jason K.},
        journal = {arXiv preprint arXiv:2302.13939},
        year    = {2023}
}
```
