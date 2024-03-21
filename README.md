# Embeddings4Disease

## Описание

TBA

## Содержание

- [Embeddings4Disease](#embeddings4disease)
  - [Описание](#описание)
  - [Содержание](#содержание)
  - [Установка](#установка)
  - [Использование](#использование)
    - [CLI для обучения](#cli-для-обучения)
    - [CLI для валидации](#cli-для-валидации)
  - [Дополнительные примеры](#дополнительные-примеры)
  - [Тесты](#тесты)

## Установка

Чтобы установить пакет из этого репозитория, достаточно написать в терминале:

```bash
!pip install git+https://github.com/windowsartesEmbeddings4Disease.git
```

Если каких-то изменений ещё нет в master-ветке, то можно установить пакет из любой другой ветки при помощи:

```bash
!pip install git+https://github.com/windowsartes/Embeddings4Disease.git@branch
```

Где «branch» - название нужной вам ветки.

Например, чтобы установить версию пакеты из ветки «development», нужно выполнить 

```bash
!pip install git+https://github.com/windowsartes/Embeddings4Disease.git@development
```

Помимо этого, в нашем проекте есть опциональные зависимости, например, для визуализации или использования архитектуры RoFormer. Чтобы установить какие-то опциональные зависимости, выполните следующую команду:

```bash
!pip install "Embeddings4Disease[optional dependencies] @ git+https://github.com/windowsartes/Embeddings4Disease.git
```

Где вместо «optional dependencies» перечислены через запятую названия наборов зависимостей. Их полный список вы можете найти в [pyptoject'е](./pyproject.toml).

Например, чтобы получить возможно использовать RoFormer и использовать проверку типов, линтер и автоформатор, нужно выполнить

```bash
!pip install "Embeddings4Disease[roformer,development] @ git+https://github.com/windowsartes/Embeddings4Disease.git
```

Установив модуль в своё виртуальное окружение, вы сможете использовать его, как любой другой устанавливаемый пакет, а также использовать cli.

## Использование

В нашем проекте есть cli в рамках которого реализованы утилиты для обучения и валидации моделей.
Скрипты будут сгенерированы и добавлены автоматически после установки пакеты в виртуальное окружение. Cli полностью работает на основе конфига, который вы ему подадите. Примеры различных конфигов вы можете найти [здесь](./config_examples/).

### CLI для обучения

Чтобы запустить обучение модели, выполните команду:

```bash
training *путь-до-конфига*
```

Путь до конфига следует указывать относительно той директории, из которой вы запускаете скрипт. Примеры конфигов для обучения с их подробным описанием вы найдёте [здесь](./config_examples/training/).

### CLI для валидации

Также нами реализован cli для валидации моделей:

```bash
validation *путь-до-конфига*
```

Как и при обучении, путь до конфиг-файла необходимо указывать относительно текущей директории. Примеры и описание вы можете найти [здесь](./config_examples/validation/)

## Дополнительные примеры

В [этом colab-блокноте](https://colab.research.google.com/drive/1xc87kcnBKP5s_thYbfkAgiiIgiNhzBY7?usp=sharing) вы найдёте пример использования cli для обучения модели с нуля.

А в [этом colab-блокноте](https://colab.research.google.com/drive/1UPCCeCHfk88UQ6eW-i-VtZ5sH2jmL9Jc?usp=sharing) вы найдёте пример использования валидации через cli.

## Тесты

CLI был полностью протестирован на Windows 11, Ubuntu 22.04 через WSL, Ubuntu 20.04 и в гугл-колабе.