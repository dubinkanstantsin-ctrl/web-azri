# Как редактировать лэндинг AZRI

Весь редактируемый контент лежит в `content.js`.

`index.html` лучше не трогать без необходимости: там находится дизайн, сетка, стили и скрипт, который подставляет данные из `content.js`.

## Что менять чаще всего

- Заголовок первого экрана: `hero.title` и `hero.highlightedTitle`
- Подзаголовок первого экрана: `hero.text`
- Дата, время и формат: `hero.event`
- Картинка: `hero.image`
- Блок результатов: `results.items`
- Блок аудиторий: `audience.items`
- Программа урока: `program.items`
- Спикер и цифры доверия: `speaker`
- FAQ: `faq.items`
- Текст формы и endpoint AmoCRM: `registration`

## Как заменить картинку

1. Положите файл в папку `azri-webinar-assets`.
2. В `content.js` поменяйте путь:

```js
image: "azri-webinar-assets/new-image.png",
```

## Как подключить AmoCRM

В `content.js` найдите:

```js
amocrmEndpoint: "",
```

И вставьте webhook или backend endpoint:

```js
amocrmEndpoint: "https://example.com/amocrm-webhook",
```

## Как добавить новый пункт в список

Скопируйте один объект и добавьте запятую между элементами:

```js
{
  title: "Новый пункт",
  text: "Текст нового пункта.",
},
```

Не удаляйте кавычки, двоеточия и запятые. Если после правки страница не открывается, чаще всего проблема в пропущенной запятой или кавычке.
