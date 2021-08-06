# Training Dataset

## NOTE

Data TBA! Expected release on 9 August 2021 (23:55 GMT+7)
We're currently checking our data format.

## Description

This folder contains the data used to train our system in the paper

To recall, this data captures a single colloquial transformation, therefore, the data does *not* alyways contain formal-informal pairs. Instead, it is possible to have informal-informal pair.

Consider the following case of word `temen2`, which is constructed from `teman-teman`.
In such case, we have to apply 2 transformations as follow:

```
1. teman-teman + space-dash -> teman2
2. teman2 + sound-alter -> temen2
```

Therefore, you will also find a pair of `teman2; temen2; sound-alter` in the dataset, despite both being informal words.

If you are looking for end-to-end formal-informal Indonesian dictionary, you can access here: TBA.


## Data CSV file format

Sample data

```
no,transformed,original-for,transformation
41,vid,video,shorten
```

### Column Definition

- `no` : Index number from the original data. If it is `x`, that means that we (annotator) added it manually to increase amount of data.
- `transformed`: Transformed word
- `original-for`: Original word which is already **transformed from the formal word** or the **formal word itself**. It will be transformed to its colloquial form in the `transformed` column.
- `transformation`: Word Formation Type. You can read our paper to see more details.
