Ссылки разделяются на внутренние и внешние. Внутренние ссылки ведут на ресурсы внутри сайта. Внешние ссылки ведут на ресурсы на чужих сайтах. Ссылки могут быть оформлены как в формате **Markdown** так и в формате **HTML**.

## Внешние ссылки

Ссылки на _внешние сайты_ потенциально небезопасны и могут ухудшить SEO.
Чтобы защитить ваш сайт и не навредить SEO оформляйте ссылки на внешние сайты в формате **HTML** и всегда добавляйте атрибут `rel="nofollow noreferrer noopener"`.

А добавление аттрибута `target="_blank"` заставит браузер открыть сторонний сайт в новой вкладке, а не просто уведет пользователя с вашего сайта.

### Примеры

:heavy_check_mark: хорошо:

```html
<a href="http://untrusted-site.com/" target="_blank" rel="nofollow noreferrer noopener">
  Что-то на чужом сайте
</a>
```

:x: плохо:

```markdown
[Что-то на чужом сайте](http://untrusted-site.com/)

<a href="http://untrusted-site.com/">Что-то на чужом сайте</a>
```
### Беклинки

Исключением являются ссылки на страницы из чужих сайтов, которым вы доверяете, с правильно оформленными **беклинками** на ваш сайт.

:bulb: **Беклинки** очень важны для SEO.

Оформлять такие ссылки надо так:

```html
<a href="http://rada.com.ua/rus/catalog/62609/"
  target="_blank" rel="noopener">
  Компания "Снежный Барс"
</a>
```


Более подробно в [рекомендациях](https://developers.google.com/style/links-external) от Google.

## Внутренние ссылки

Внутренние ссылки предназначены для осуществления перехода между страницами внутри сайта.

:bulb: Для того, чтобы в будущем было легче отслеживать переходы по внутренним ссылкам сайта в **Google Analytics**  всегда добавляйте косую черту `/` (слеш) в конце ссылки.

Примеры ссылок на ресурсы английской версии сайта.
Так как в настройках сайта язык `en` задан главным, то префикс языка к пути не добавляется.

```markdown
[Home](/)

[My awesome project](/my-awesome-project/)
```

Ссылки на все русскоязычные ресурсы сайта начинаются с префикса языка `/ru/`.

```markdown
[Главная](/ru/)

[Мой красивый проект](/ru/my-awesome-project/)
```

Ссылки на все украиноязычные ресурсы сайта начинаются с префикса языка `/uk/`.

```markdown
[Головна](/uk/)

[Мій чудовий проект](/uk/my-awesome-project/)
```


Markdown позволяет вставлять ссылки в формате HTML.

```html
<a href="/">Home</a>

<a href="/my-awesome-project/">My awesome project</a>


<a href="/ru/">Главная</a>

<a href="/ru/my-awesome-project/">Мой красивый проект</a>


<a href="/uk/">Головна</a>

<a href="/uk/my-awesome-project/">Мій чудовий проект</a>
```