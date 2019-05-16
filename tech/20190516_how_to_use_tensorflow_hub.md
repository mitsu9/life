# TensorFlow Hubの使い方

## 環境
TensorFlow 1.7以上が必要

```
pip install "tensorflow>=1.7.0"
pip install tensorflow-hub
```

## 使い方
```py
import tensorflow_hub as hub

# 必要なmoduleを取得する
module = hub.Module("xxxxxxx")

# moduleに合わせたinputsを入れるとoutputsが得られる
inputs = xxx
outputs = module(inputs)
```

## 例
BERTを使ってtokenizeしてみた

```py
from bert.tokenization import FullTokenizer
import tensorflow_hub as hub

bert_module =  hub.Module(BERT_MODEL_HUB)
tokenization_info = bert_module(signature="tokenization_info", as_dict=True)
vocab_file, do_lower_case = sess.run(
    [
        tokenization_info["vocab_file"],
        tokenization_info["do_lower_case"],
    ]
)
tokenizer = FullTokenizer(vocab_file=vocab_file, do_lower_case=do_lower_case)
token = tokenizer.tokenize('こんにちは、今日の天気はいかがでしょうか？')
print(token)
```

## 参考
- [TensorFlow Hubから学習済みモデル(Inception-v3)を利用する](https://qiita.com/shu-yusa/items/8ae5326ff55f9dd674c7)
- [Googleのbertを利用してみました〜！](http://developers.goalist.co.jp/entry/bert_introduction)
