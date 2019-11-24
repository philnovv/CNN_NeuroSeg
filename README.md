Code and data used in publication [Accurate and robust segmentation of neuroanatomy in T1-weighted MRI by combining spatial priors with deep convolutional neural networks](https://doi.org/10.1002/hbm.24803)

## Prerequisites

* Python 3.6
* [MINC toolkit](https://bic-mni.github.io/)
* [pyminc](https://github.com/Mouse-Imaging-Centre/pyminc)
* [lasagne + theano](https://lasagne.readthedocs.io/en/latest/)

## Example code

Train a network:

```
python train_cnn.py -tr_ima yourTrainingImages.txt -tr_mask yourTrainingMasks.txt -model_name yourModelName -sampling_mask yourSamplingMask.mnc -num_labels yourLabelNumber

```

Apply it:

```
python apply_cnn.py -te_ima yourTrainingImages.txt -output_dir yourOutputDir -model_name yourModelName -sampling_mask yourSamplingMask.mnc -num_labels yourLabelNumber -positive_mask yourPositiveMask.mnc

```

## Details

See code comments for further details.