Папка: `[CONTENT_DIR]/data/locales`

| Что                | Папка           | Имя файла            | Комментарий
| ------------       | --------------- | -------------------  | -------------------
| Главное меню       | ./main-nav      | main-nav.en.yaml     |
|                    |                 | main-nav.uk.yaml     |
|                    |                 | main-nav.ru.yaml     |
| Ссылки на соц.сети | ./social-links  | social-links.en.yaml | Facebook, Intagram и тд
|                    |                 | social-links.uk.yaml |
|                    |                 | social-links.ru.yaml |
| Адрес              | ./address       | address.en.yaml      | Официальное название организации, почтовый адрес, подробное описание контактов
|                    |                 | address.uk.yaml      |
|                    |                 | address.ru.yaml      |
| Переводы           | ./translations  | translations.en.yaml | Для внутреннего использования
|                    |                 | translations.uk.yaml |
|                    |                 | translations.ru.yaml |

## Главное меню

Список полей

|   Поле       | Описание
|---           |---
| to           | путь к странице без префикса языка, но со слешем в конце. Пример: `/contacts/`
| title        | название ссылки

## Ссылки на социальные сети

Ссылки на профили в соц.сетях отображаются в футере сайта в виде иконок.

Список полей

|   Поле       | Описание
|---           |---
| to           | ссылка на ваш профиль в социальной сети
| title        | всплывающая подсказка
| code         | код соц.сети


При наведении курсора мыши на иконку выводится всплывающая подсказка (поле **title**).


:warning: Поле **код** используется для построения SEO и для вывода иконки.

Для добавления соц.сетей, отличных от Instagram и Facebook, нужен программист.


## Адрес

Содержимое этого файла используется на странице "Контакты" и SEO.

Поле **e-mail** в виде списка, разделитель элементов списка запятая `,`.



Поле **telephone** в виде списка цифровых значений, разделитель элементов списка запятая `,`.

:bulb: Номер телефона допускает только цифры, без плюса спереди, без пробелов, скобок и прочих символов.

Пример содержимого:

```yaml
name: Your company name
alternateName: Your company name
legalName: Your company descriptin

postalAddress:
  streetAddress:
    - 1 Downing St., app.1
  addressLocality:  Odessa
  addressRegion: Odessa Region
  postalCode: 65000
  addressCountry: Ukraine
```

### Переводы

Переводы используются только в коде программы. Поэтому не предполагается их редактирование.

Если все же возникла такая потребность, то:

- Отредактируйте соответствующий `JSON` файл в папке `[CONTENT_DIR]/data/locales/translations/src/`.
- Зайдите в командную строку, перейдите в папку `[PROJECT_DIR]` и выполните команду `yarn trans`.
  Эта команда запустит javascript-скрипт, который преобразует файл c переводами из формата `JSON` в `YAML` (Вам потребуется предварительно установить на локальный компьютер **nodejs** и **yarn**).

  :bulb: Для автоматического обновления переводов во время `commit`-a потребуется дополнительно установить **husky** и **lint-staged**.
- выполните действия из раздела **[Публикация изменений](#публикация-изменений)**.