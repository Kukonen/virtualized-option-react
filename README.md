# Тестовое задание для компании ИНФИНАЙТ СИНЕРДЖИ

### Запуск приложения

для запуска клиента требуется написать в консоли:
``` cmd
cd client
npm run start
```

для запуска сервера требуется написать в консоли:
``` cmd
cd server
npm run dev
```

### Особая реализация

Для обработки 1000000 элементов в запросе было использована техника виртуализации

Виртуализации подвергнут компонент Select в файле client/src/components/Select/select.tsx

После загрузки данных с сервера мы
- выделяем некое заранее заданое число отображаемых элементов BASE_OPTION_LENGTH
- при скроле до конца блока или до начала происходит добавление ближайших элементов и удаление элементов с противоположной стороны блока

Реализация изменения элементов происходит в функции ``` scrollEvent ```