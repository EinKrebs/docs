---
title: "Определение языка текста"
description: "Определение языка, на котором написан заданный текст. Ответ возвращается в виде кода языка."
---

# Определение языка текста

{% include [speechkit-v1-disclaimer.md](../../../_includes/speechkit-v1-disclaimer.md) %}

Определение языка, на котором написан заданный текст. Ответ возвращается в виде кода языка.

При работе с API Translate отправляйте данные для [аутентификации](/docs/translate/api-ref/authentication) в заголовке `Authorization` каждого запроса.

## Запрос {#request}

```
POST https://translate.{{ api-host }}/translate/v1/detect
```

### Параметры в теле запроса {#parameters-in-the-request-body}

Для всех параметров обязательно используйте URL-кодирование. Максимальный размер тела POST-запроса 30 КБ.

Параметр | Описание
----- | -----
`text` | Обязательный параметр.<br/>Текст, язык которого требуется определить, в кодировке UTF-8.
`hint` | Список наиболее вероятных языков (им будет отдаваться предпочтение при определении языка текста). Разделитель списка — запятая.
`folderId` | Обязательный параметр.<br/>Идентификатор вашего каталога.<br/>Подробнее о том, как узнать идентификатор каталога.


## Ответ {#response}

Ответ возвращается в формате JSON.

```json
{
    "language": <код_языка>
}
```


## Примеры {#examples}

### Пример запроса {#sample-request}

```httpget
export FOLDER_ID=<идентификатор_каталога>
export TOKEN=<IAM-токен>
curl -X POST \
     -H "Authorization: Bearer ${TOKEN}" \
     -d "folderId=${FOLDER_ID}" \
     --data-urlencode "text=привет мир" \
     "https://translate.{{ api-host }}/translate/v1/detect"
```

### Пример ответа {#response-example}

Ответ возвращается в формате JSON.

```json
{
    "language": "ru"
}
```

