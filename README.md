# chainer-char-rnn-tiny
Modified yusuketomoto's [chainer-char-rnn](https://github.com/yusuketomoto/chainer-char-rnn) to run with Chainer2.0

## Requirement
- [Chainer2.0](https://github.com/pfnet/chainer)
```
$ pip install chainer=="2.0.2"
```

## Train
Start training the model using `train.py`, for example

```
$ python train.py
```

The `--data_dir` flag specifies the dataset to use. By default it is set to `data/tinyshakespeare` which consists of a subset of works of Shakespeare.

**Your own data**: If you'd like to use your own data create a single file `input.txt` and place it into a folder in `data/`. For example, `data/some_folder/input.txt`.



## Sampling
Given a checkpoint file (such as those written to cv) we can generate new text. For example:
```
$ python sample.py \
--vocabulary data/tinyshakespeare/vocab.bin \
--model cv/some_checkpoint.chainermodel \
--primetext some_text --gpu -1
```

## References
- Original Chainer implementation: https://github.com/yusuketomoto/chainer-char-rnn
- Original implementation: https://github.com/karpathy/char-rnn
