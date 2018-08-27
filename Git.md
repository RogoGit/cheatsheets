# Git

## Создание нового репозитория

В папке с кодом:

```
git init .
git add .
git commit -m "initial commit"
git remote add origin git@github.com:username/repo
git push origin master
```

## Алгоритм добавления коммита

```
git add . # добавить изменения
git status # проверить, что не добавил ничего лишнего
git commit -m "message"
git push origin master
если на этапе git push он отказывается (т.е. в репозитории есть новые коммиты), 
то я просто делаю git pull --rebase, затем опять git push
```

## Я сделал неудачный коммит и запушил его

```
git log --graph --decorate --oneline # смотрим SHA-1 id нашего неудачного коммита
(обычно 7 символов)
git revert SHA-1 # удаляем изменения неудавшегося коммита
git push origin master # push`им изменения
```

# ПИП. Лаба №1

## 1. Протокол HTTP. Структура запросов и ответов, методы запросов, коды ответов сервера, заголовки запросов и ответов.
```
HTTP (англ. HyperText Transfer Protocol — «протокол передачи гипертекста») — протокол прикладного уровня передачи данных (изначально — в виде гипертекстовых документов в формате «HTML», в настоящий момент используется для передачи произвольных данных). Основой HTTP является технология «клиент-сервер», то есть предполагается существование:
  - Потребителей (клиентов), которые инициируют соединение и посылают запрос;
  - Поставщиков (серверов), которые ожидают соединения для получения запроса, производят необходимые действия и возвращают обратно сообщение с результатом.
```