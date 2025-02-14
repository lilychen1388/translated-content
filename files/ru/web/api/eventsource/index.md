---
title: EventSource
slug: Web/API/EventSource
translation_of: Web/API/EventSource
---
{{APIRef("Websockets API")}}

`Интерфейс EventSource` используется для получения серверных событий (Server-sent events). Он устанавливает соединение с сервером по HTTP и получает события в формате text/event-stream без закрытия соединения.

Вы можете присвоить атрибуту `onmessage` JavaScript-функцию для получения нетипизированных сообщений (то есть сообщений без поля `event`). Вы так же можете вызвать функцию `addEventListener()` для обработки событий так же, как для любого другого источника событий.

См. [Using server-sent events](/en/Server-sent_events/Using_server-sent_events) для более детальной информации

## Методы

| `void close();` |
| --------------- |

## Свойства

| Attribute    | Type                                 | Description                                                                                                   |
| ------------ | ------------------------------------ | ------------------------------------------------------------------------------------------------------------- |
| `onerror`    | `nsIDOMEventListener`                | JavaScript-функция, вызываемая при появлении ошибки                                                           |
| `onmessage`  | `nsIDOMEventListener`                | JavaScript-функция, вызываемая при приходе сообщения без поля `event`                                         |
| `onopen`     | `nsIDOMEventListener`                | JavaScript-функция, вызываемая после открытия соединения                                                      |
| `readyState` | [`long`](/en/long)         | Состояние соединения, должно иметь одно из значений `CONNECTING`, `OPEN`, или `CLOSED`. **Только для чтения** |
| `url`        | {{ domxref("DOMString") }} | **Только для чтения**                                                                                         |

В дополнение к открытым атрибутам два внутренних атрибута, которые не открыты напрямую:

- reconnection time
  - : Это время в миллисекундах, используемое для определения продолжительности ожидания после неудачной попытки соединения до повторного соединения
- last event ID string
  - : По умолчанию пустая строка. Сервер может отправлять сообщение с полем `id` для установки этого значения.

## Константы

| Constant     | Value | Description                                                            |
| ------------ | ----- | ---------------------------------------------------------------------- |
| `CONNECTING` | `0`   | Соединение устанавливается                                             |
| `OPEN`       | `1`   | Соединение открыто, получение событий                                  |
| `CLOSED`     | `2`   | Соединение не устанавливается, закрыто, или произошла фатальная ошибка |

## Методы

### close()

Закрывает соединение, если оно существует и устанавливает атрибут `readyState` в значение `CLOSED`. Если соединение уже закрыто, этот метод ничего не делает.

```
void close();
```

###### Параметры

Нет

## Смотрите также

- {{ spec("https://html.spec.whatwg.org/multipage/comms.html#the-eventsource-interface","Server-Sent Events: The EventSource Interface","CR") }}
- [Using server-sent events](/en/Server-sent_events/Using_server-sent_events)

## Совместимость браузеров

{{Compat}}
