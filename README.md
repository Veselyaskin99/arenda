# Аренда автотранспорта в прокат

Цель программы – повышение качества процесса аренды ТС, повышение эффективности работы сотрудников
## Диаграмма размещений 

![](https://github.com/Veselyaskin99/README/blob/main/1f.png)

На диаграмме размещения изображены узлы выполнения программных компонентов, а также объектов. Показано, что приложение, установленное на компьютере пользователя взаимодействует с сервером, который содержит в себе базу данных.

## Диаграмма компонентов

![](https://github.com/Veselyaskin99/README/blob/main/1.png)

На данной диаграмме изображены все компоненты: клиентское приложение, Работники, клиенты, платежи, контракты и автомобили. Эти компоненты взаимодействуют друг с другом с помощью интерфейсов. 

## Диаграмма интерфейсов

![](https://user-images.githubusercontent.com/74318083/101732870-d8e32f80-3af8-11eb-98f7-3bb29485c485.png)

### Список всех интерфейсов:


- **[IClient](https://github.com/Veselyaskin99/README/blob/main/IClient.md)**<br>
- **[IWorker](https://github.com/Veselyaskin99/README/blob/main/IWorker.md)**<br>
- **[IContract](https://github.com/Veselyaskin99/README/blob/main/IContract.md)**<br>
- **[IPay](https://github.com/Veselyaskin99/README/blob/main/IPay.md)**<br>
- **[ITS](https://github.com/Veselyaskin99/README/blob/main/ITS.md)**



# Меню

![](https://user-images.githubusercontent.com/74318083/101327940-5bc27b00-38aa-11eb-81fb-1aa85895f9dd.png)
**[Код формы "Меню"](https://github.com/Veselyaskin99/arenda/blob/main/Workers)**
    
# Форма "Сотрудники"
![](https://user-images.githubusercontent.com/74318083/101329685-a9d87e00-38ac-11eb-8a22-d3df0d493ea9.png)
### Функционал:
- В textbox можно ввести Имя и в таблице найдется нужный менеджер;
- Кнопка "Добавить сотрудника"(Отображается форма добавления сотрудника);
- Кнопка "Редактировать / просмотр"(Позволяет открыть форму, с полной информацией о сотруднике, где можно ее редактировать;
- При двойном нажатии на строку в таблице, откроется форма с полной информацией о сотруднике, где можно ее редактировать;
- Кнопка "Удалить сотрудника" (Позволяет удалить сотрудника из БД).
## Поиск сотрудника
![](https://user-images.githubusercontent.com/74318083/101329711-b52ba980-38ac-11eb-8c90-c2ad14e3b5b8.png)



**[Код формы "Сотрудники"](https://github.com/Veselyaskin99/arenda/blob/main/Workers)**

# Форма "Добавить сотрудника"
![](https://user-images.githubusercontent.com/74318083/101329720-b8269a00-38ac-11eb-8a2f-90c0da5626f2.png)
### Функционал:
- При нажатии на кнопку "Добавить" добавляет нового сотрудника в БД.



**[Код формы "Добавить сотрудника"](https://github.com/Veselyaskin99/arenda/blob/main/AddWorker)**

# Форма "Текущий сотрудник"
![](https://user-images.githubusercontent.com/74318083/101329699-b1982280-38ac-11eb-8678-39d0d4a3c2ac.png)
### Функционал:
- На форме "Текущий сотрудник" в datagridView отображаются контракты заключенные выбранным сотрудником;
- Возможно редактирование информации о сотруднике.



**[Код формы "Текущий сотрудник"](https://github.com/Veselyaskin99/arenda/blob/main/currentWorker)**

# Форма "Клиенты"
![](https://user-images.githubusercontent.com/74318083/101335143-c2986200-38b3-11eb-9563-db4340475d32.png)
### Функционал:
- Кнопка "Добавить клиента"(Отображается форма добавления клиента);
- Кнопка "Редактировать / просмотр"(Позволяет открыть форму, с полной информацией о клиенте, где можно ее редактировать;
- При двойном нажатии на строку в таблице, откроется форма с полной информацией о клиенте, где можно ее редактировать;
- Кнопка "Удалить клиента" (Позволяет удалить клиента из БД).



**[Код формы "Клиенты"](https://github.com/Veselyaskin99/arenda/blob/main/Clients)**
# Форма "Добавить клиента"
![](https://user-images.githubusercontent.com/74318083/101335110-b6aca000-38b3-11eb-9b29-d4a964dd3b82.png)
### Функционал:
- При нажатии на кнопку "Добавить" добавляет нового клиента в БД.



**[Код формы "Добавить клиента"](https://github.com/Veselyaskin99/arenda/blob/main/Addclient)**
# Форма "Текущий клиент"
![](https://user-images.githubusercontent.com/74318083/101335151-c62be900-38b3-11eb-84b8-3cbd00bb0318.png)
### Функционал:
- На форме "Текущий клиент" в datagridView отображаются контракты заключенные выбранным клиентом;
- Возможно редактирование информации о клиенте.



[Код формы "Текущий клиент"](https://github.com/Veselyaskin99/arenda/blob/main/Clients)
# Форма "Договора"
![](https://user-images.githubusercontent.com/74318083/101341410-02634780-38bc-11eb-9016-a9fe006fb66e.png)
### Функционал:
- В textbox можно ввести дату и в таблице найдется нужный договор;
- Кнопка "Добавить контракт"(Отображается форма добавления договора);
- При двойном нажатии на строку в таблице, откроется форма с полной информацией о договоре;
## Поиск договора
![](https://user-images.githubusercontent.com/74318083/101341424-08592880-38bc-11eb-80ff-f29e10ade875.png)


[Код формы "Договора"](https://github.com/Veselyaskin99/arenda/blob/main/Contracts)
[Код формы "Добавить сотрудника"](https://github.com/Veselyaskin99/arenda/blob/main/Addclient)
# Форма "Текущий договор"
![](https://user-images.githubusercontent.com/74318083/101341421-05f6ce80-38bc-11eb-96f0-15b65804c431.png)
### Функционал:
- Отображается информация о договоре



[Код формы "Текущий договор"](https://github.com/Veselyaskin99/arenda/blob/main/CurrenContract)
# Форма "Добавить договор"
![](https://user-images.githubusercontent.com/74318083/101341474-1a3acb80-38bc-11eb-97ab-4ffad808524c.png)
### Функционал:
-При нажатии на кнопку "Добавить" добавляет новый договор в БД.
# Форма "Платежи"
![](https://user-images.githubusercontent.com/74318083/101344128-f8434800-38bf-11eb-808d-3d6423cb5529.png)
### Функционал:
- В textbox можно ввести дату и в таблице найдется нужные платежи;
- При двойном нажатии на строку в таблице, откроется форма с полной информацией о договоре.
## Поиск платежа
![](https://user-images.githubusercontent.com/74318083/101344132-fb3e3880-38bf-11eb-9810-15fe36aba6e6.png)


**[Код формы "Платежи"](https://github.com/Veselyaskin99/arenda/blob/main/Payes)**
# Форма "Автомобили"
![](https://user-images.githubusercontent.com/74318083/101348459-9f2ae280-38c6-11eb-8641-c641bfa438fc.png)
### Функционал:
- При выборе строки, фотография ТС отображается в pictureBox;
- При нажатии кнопки "Добавить ТС"(Открывается форма добавления ТС);
- При нажатии кнопки "Удалить" Автомобиль удаляется из БД.



[Код формы "Автомобили"](https://github.com/Veselyaskin99/arenda/blob/main/TS)
# Форма "Добавить ТС"
![](https://user-images.githubusercontent.com/74318083/101348477-a7831d80-38c6-11eb-805f-5bfcf320f2b0.png)
### Функционал:
- Добавляет Автомобиль в ДБ;
- Нажав кнопку "Поиск" можно выбрать фотографию из Компьютера.
## Выбор фотографии
![](https://user-images.githubusercontent.com/74318083/101348467-a18d3c80-38c6-11eb-924d-92f779eebe19.png)



**[Код формы "Добавить ТС"](https://github.com/Veselyaskin99/arenda/blob/main/AddTS)**
# Форма "Статистика"
![](https://user-images.githubusercontent.com/74318083/101745470-2914be80-3b06-11eb-877b-a64e022de5e8.png)
### Функционал:
- Позволяет посмотреть количество сданных в аренду автомобилей менеджером;
- Позволяет посмотреть количество вырученных денег за определенный промежуток времени.



**[Код формы "Статистика](https://github.com/Veselyaskin99/arenda/blob/main/Statistic)**
