# Как распознать эмоции
![image](https://user-images.githubusercontent.com/91029600/137598882-82a750a2-e424-421c-9344-c5a70c5eea6b.jpeg)

 ## Анализ эмоций в тексте

В художественном или любом традиционном тексте мы считываем эмоции из слов и знаков препинанй @#$%^  
Это можно проанализировать, задав условия по поиску определенных слов или "!!!" при помощи :snake:

Но смысл текста с использованием эмодзи при помощи программы считать нельзя. Сравните

Отличное место

*или*

Отличное место :smirk:

## В каких областях эмодзи важнее всего?

+ Социальные сети

+ Отзывы

#### То есть если вам важно мнение аудитории, то придется читать эмодзи

## А в культурологии?

Все слышали, что я люблю музеи и хочу делать их лучше. Это невозможно без обратной связи. Часто эмодзи выполняют функцию эмоционального громоотвода в тексте, и их используют для подчеркивания основной мысли. Пожалуй, будет нелишним узнать, что именно в отзыве вызвало самую сильную эмоцию.

Если речь о том, чтобы привлекать школьную и студенческую аудиторию, то эмоджи могут стать фокусом опроса мнения, особенно не в городах-миллионниках.

Конечно, бывает так

![image](https://user-images.githubusercontent.com/91029600/137599207-03ab1ae9-41c1-4cba-8a5e-005f2c66e15b.jpeg)

Но чаще уже так (про Гараж)

![](Garage.jpg)

или так (про Пушкинский музей)

![](Gaarage.png)

Короче, в любой обратной связи появляются эмодзи. Как картинки они бывают сложными для быстрого считывания

![](Emoji PNG.png)

![image](https://user-images.githubusercontent.com/91029600/138304574-5ef49d18-c0d5-4529-afa3-673e76fa3dda.jpeg)


## Чем поможет библиотека Emoji?

При загрузке и обработке текста с эмодзи можно расшифровать их таким образом:

```
emoji.demojize("🤯")
:exploding_head:
```

Можно удалять эмоджи из текста, можно конвертировать эмоджи в смысл, можно текст конвертировать в эмоджи:

```
import emoji
def check_for_emoji(text):
    split_text=text.split()
    for i in split_text:
        if i in emoji.UNICODE_EMOJI:
            print("This is emoji:",i)
            print("The emoji means:",emoji.demojize(i))

text="Have a nice day 👍 :)"
check_for_emoji(text)
```

```
This is emoji: 👍
The emoji means: :thumbs_up:
```

То есть, вместо трудно различимой закорючки у вас в комментарии указан примерный смысл, который хотел вложить автор.

Почему примерный? Потому что иногда автор ничего не хочет сказать читателю.

![image](https://user-images.githubusercontent.com/91029600/137600123-c20961f6-b6b3-42cf-acbc-cbe2888f8907.jpeg)

_____________________________________________________________________________________________________________________

В коде показан пример, как можно "расшифровать" эмодзи, выделив его из текста

ссылка на код: [тут](https://colab.research.google.com/drive/19mAihYg-RKP2FH-9zOjMhSoIg6xjO3eq?authuser=1#scrollTo=XWso82XQ_DvM)



