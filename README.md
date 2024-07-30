# CharacterTokenizer
Имплементация HF-совместимого символьного токенизатора для продуктов Den4ik Ebany Research

## Установка

```
pip install git+https://github.com/Den4ikAI/CharacterTokenizer.git
```

## Пример использования

```py
import chartk

tokenizer = chartk.CharacterTokenizer.from_pretrained('ruaccent/RUAccent-encoder')

prompt = "Я помню чудное"
encoded_prompt = tokenizer.encode(prompt, return_tensors='pt')
print(' | '.join(tokenizer.decode([t]) for t in encoded_prompt[0]))
```
