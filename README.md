# module_3_4
Самостоятельная работа по уроку "Произвольное число параметров"
Данный код определяет функцию `single_root_words`, которая ищет слова в переданном наборе, содержащие заданное корневое слово и, в то же время, проверяет, является ли данное корневое слово частью каких-либо других слов. Функция принимает два типа аргументов: обязательный аргумент `root_word` и произвольное количество других слов (`*other_words`), которые передаются в виде кортежа.
def single_root_words(root_word, *other_words):
    same_words = []
    for i in other_words:
        if root_word.lower() in i.lower():
            same_words.append(i)
            continue
        elif i.lower() in root_word.lower():
            same_words.append(i)
            continue
    return same_words
result1 = single_root_words('rich', 'richiest', 'orichalcum', 'cheers', 'richies')

result2 = single_root_words('Disablement', 'Able', 'Mable', 'Disable', 'Bagel')

print(result1)

print(result2)
