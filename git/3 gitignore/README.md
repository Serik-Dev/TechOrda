# gitignore

При командной работе в одном репозиторий следует избегать добавления ненужных файлов. Например: файлы компиляции, временные файлы проекта, секретные токены и т.д.

`.gitignore` сообщает git, какие файлы и папки следует игнорировать, чтобы они не добавились в репозиторий.

### Полезное

- [Документация с примерами.gitignore](https://git-scm.com/book/ru/v2/%D0%9E%D1%81%D0%BD%D0%BE%D0%B2%D1%8B-Git-%D0%97%D0%B0%D0%BF%D0%B8%D1%81%D1%8C-%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D0%B9-%D0%B2-%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B9#r_ignoring)
- [Сборник .gitignore для разных проектов](https://github.com/github/gitignore)

### Задание

1. Добавить в свой репозитории `jusan-git` файл `.gitignore`, который игнорирует:

```
temp
```

2. Проверить работает ли `.gitignore`. Для этого создайте папку `temp` с любым файлом внутри и введите `git status`.
3. Убедиться что `temp` и его содержимое не входит в список изменений.
4. Загрузить изменения в github.
5. Прислать ссылку на репозиторий c указанием последнего коммита в URL. Например:

```
https://github.com/username/jusan-git/tree/5a1e0d9c4c864e13f0682bec96a9f19786fad711
```

---

### Ответ

В репозитории не должно быть папки `temp`. Файл `.gitignore`:

```
temp
```
d1953cd85b105d5f346e2ffb86a0fbf5cc3072d9
