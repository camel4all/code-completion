# Code-Completion
Pytorch version of [code completion with neural attention and pointer networks](https://arxiv.org/pdf/1711.09573.pdf)


## TO DO LIST:
- [ ] refactor preprocessing code
- [ ] add python to AST code
- [ ] config for preprocessing
- [ ] join training for type

## Requirments list:

- python3 >= 3.6
- torch >= 1.2, or tensorboadX for earlier versions
- pyyaml


## Instruction:

- run `python3 preprocess.py` for preprocessing
- run `CUDA_VISIBLE_DEVICES=id python3 train.py --config=path/to/config.yml` for training with specified config, list of available configscan be found at configs folder

## Results for python value prediction (acc@1):


model | vocab_size 1k | vocab_size 10k | vocab_size 50k
--- | --- | --- | ---
simple_lstm | 66.33 | 65.7 | 61.68, 1 epoch
attn_lstm | 64.95 | 65.77 | 63.15, 1 epoch
pointer_mixture | 66.62 | [67.05](https://www.dropbox.com/s/r69ksk7idd53s9n/epoch_0007.pth?dl=0) | [65.3, 3 epochs](https://www.dropbox.com/s/s40ruwonbeebpxm/epoch_0002.pth?dl=0)



## Examples:
Here will be examples of code generation
