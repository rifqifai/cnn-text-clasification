# CNN Text Clasification

Please visit [my blog post](https://rifqifai.com) for more detail.

## Intisari

Berkembang pesatnya informasi serta besarnya jumlah data teks dalam bentuk digital telah menjadi subjek penelitian yang penting dalam mengekstrak informasi dari data teks tersebut. Hal ini diperlukan suatu sistem otomatisasi yang dapat mengelola dan mengelompokkan data teks tersebut. Pengelompokan data teks dibutuhkan untuk mempermudah dan mempercepat pencarian suatu informasi. Dalam artikel ini bertujuan untuk mengklasifikasikan teks menggunakan convolutional neural network (CNN) berdasarkan polaritas positif dan negatif yang meliputi analisis sentimen dan klasifikasi pertanyaan. Dengan melakukan sedikit modifikasi arsitektur untuk dapat digunakan pada static vector. Berdasarkan hasil pengujian menunjukkan bahwa metode CNN dengan melakkukan sedikit tunning hyperparameter  dan static vector dapat meraih hasil yang sangat baik pada proses pengujian.


## Requirements

```bash
Library Tensorflow
Library Keras 
Library Numpy
```

## Training

Print parameters:

```bash
./train.py --help
```

```
optional arguments:
  -h, --help            show this help message and exit
  --embedding_dim EMBEDDING_DIM
                        Dimensionality of character embedding (default: 128)
  --filter_sizes FILTER_SIZES
                        Comma-separated filter sizes (default: '3,4,5')
  --num_filters NUM_FILTERS
                        Number of filters per filter size (default: 128)
  --l2_reg_lambda L2_REG_LAMBDA
                        L2 regularizaion lambda (default: 0.0)
  --dropout_keep_prob DROPOUT_KEEP_PROB
                        Dropout keep probability (default: 0.5)
  --batch_size BATCH_SIZE
                        Batch Size (default: 64)
  --num_epochs NUM_EPOCHS
                        Number of training epochs (default: 100)
  --evaluate_every EVALUATE_EVERY
                        Evaluate model on dev set after this many steps
                        (default: 100)
  --checkpoint_every CHECKPOINT_EVERY
                        Save model after this many steps (default: 100)
  --allow_soft_placement ALLOW_SOFT_PLACEMENT
                        Allow device soft device placement
  --noallow_soft_placement
  --log_device_placement LOG_DEVICE_PLACEMENT
                        Log placement of ops on devices
  --nolog_device_placement

```

Train:

```bash
./train.py
```

## Evaluating

```bash
./eval.py --eval_train --checkpoint_dir="./runs/1459637919/checkpoints/"
```

Replace the checkpoint dir with the output from the training. To use your own data, change the `eval.py` script to load your data.

## Reference

1. I. Pramudiono, “Pengantar Data Mining : Menambang Permata Pengetahuan di Gunung Data,” Kuliah Umum Ilmu Komputer.com, pp. 1–4, 2003.
2. LISA lab, “Deep Learning Tutorials,” Univ. Montr., pp. 27–28, 2015.
3. N. Kalchbrenner, E. Grefenstette, and P. Blunsom, “A Convolutional Neural Network for Modelling Sentences,” Dep. Comput. Sci. Univ. Oxford, pp. 655–665, 2014.
4. B. Pang and L. Lee, “A Sentimental Education: Sentiment Analysis Using Subjectivity Summarization Based on Minimum Cuts,” Proc. ACL, 2004.
5. S. Collobert, J. Weston, L. Bottou, M. Karlen, K. Kavukcuoglu, and P. Kuksa, “Natural Language Processing (Almost) from Scratch,” J. Mach. Learn. Res. 12, pp. 2493–2537, 2011.
