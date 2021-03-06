# Схема прецедентов
![](https://user-images.githubusercontent.com/74318083/102003162-aa569600-3d3e-11eb-9a18-8da71b5b8335.png)
## Описание прецедентов
#### Таблица 1 Описание прецедента "Просмотр списка клиентов"
Имя прецедента:	Просмотр списка клиентов<br>
Краткое описание:	Прецедент позволяет просматривать список всех клиентов<br>
Актёры:	Менеджер<br>
Предусловия:	Должен быть хотя бы один клиент. Если таковых нет, то пользователю предлагается создать нового клиента.<br>
Основной поток:	Выводится информация обо всех клиентах в виде таблицы<br>
Постусловия:	Если прецедент был успешно завершен, то пользователь может выполнять другие действия<br>
Альтернативные потоки:	—<br><br>

#### Таблица 2 Описание прецедента "Добавление клиента"
Имя прецедента:	Добавление клиента<br>
Краткое описание:	Прецедент позволяет добавлять новых клиентов<br>
Актёры:	Менеджер<br>
Предусловия:	Должен быть выполнен прецедент “Просмотр списка клиентов”<br>
Основной поток:	Открывается форма добавления нового клиента, куда заносятся все необходимые данные<br>
Постусловия:	Если прецедент был успешно завершен, то форма добавления клиента закрывается, и в БД добавляется новый клиент<br>
Альтернативные потоки:	Если имеются пустые поля, либо введены некорректные данные, то пользователю выдается сообщение об ошибке и дается возможность исправить данные<br><br>

#### Таблица 3 Описание прецедента "Редактирование данных о клиенте"
Имя прецедента:	Редактирование данных о клиенте<br>
Краткое описание:	Прецедент позволяет редактировать данные о клиенте<br>
Актёры:	Менеджер<br>
Предусловия:	Должен быть выполнен прецедент “Просмотр одного клиента”<br>
Основной поток:	Открывается форма редактирования клиента, где изменяются необходимые данные<br>
Постусловия:	Если прецедент был успешно завершен, то форма редактирования клиента закрывается, и измененные данные о клиенте сохраняются<br>
Альтернативные потоки:	Если имеются пустые поля, либо введены некорректные данные, то пользователю выдается сообщение об ошибке и дается возможность исправить данные<br><br>

#### Таблица 4 Описание прецедента "Фильтрация списка клиентов"
Имя прецедента:	Фильтрация списка клиентов<br>
Краткое описание:	Прецедент позволяет фильтровать списки клиентов<br>
Актеры:	Менеджер<br>
Предусловия:	Должен быть выполнен прецедент “Просмотр списка клиентов”<br>
Основной поток:	Фильтрует клиентов<br>
Постусловия:	Если прецедент был успешно завершен, то пользователь может выполнять другие действия<br>
Альтернативные потоки:	—<br><br>

#### Таблица 5 Описание прецедента " Просмотр одного клиента "
Имя прецедента:	Просмотр одного клиента<br>
Краткое описание:	Прецедент позволяет просмотреть данные выбранного клиента<br>
Актёры:	Менеджер<br>
Предусловия:	Должен быть выполнен прецедент “Просмотр списка клиентов”<br>
Основной поток:	Выводится вся информация о конкретном клиенте<br>
Постусловия:	Если прецедент был успешно завершен, то пользователь может выполнять другие действия<br>
Альтернативные потоки:	—<br><br>

#### Таблица 6 Описание прецедента " Просмотр истории клиента "
Имя прецедента:	Просмотр истории клиента<br>
Краткое описание:	Прецедент позволяет просмотреть историю клиента<br>
Актёры:	Менеджер<br>
Предусловия:	Должен быть выполнен прецедент «Просмотр одного клиента»<br>
Основной поток:	Выводится список арендованных машин этим клиентом<br>
Постусловия:	Если прецедент был успешно завершен, то пользователь может выполнять другие действия<br>
Альтернативные потоки:	—<br><br>

#### Таблица 7 Описание прецедента " Просмотр штрафов клиента "
Имя прецедента:	Просмотр штрафов клиента<br>
Краткое описание:	Прецедент позволяет просмотреть все штрафы клиента<br>
Актёры:	Менеджер<br>
Предусловия:	Должен быть выполнен прецедент «Просмотр одного клиента»<br>
Основной поток:	Выводит все штрафы клиента (если они есть)<br>
Постусловия:	Если прецедент был успешно завершен, то пользователь может выполнять другие действия<br>
Альтернативные потоки:	—<br><br>

#### Таблица 8 Описание прецедента " Комментарии к клиенту"
Имя прецедента:	Комментарии к клиенту <br>
Краткое описание:	Прецедент позволяет просматривать комментарии к клиенту<br>
Актёры:	Менеджер<br>
Предусловия:	Должен быть выполнен прецедент «Просмотр одного клиента»<br>
Основной поток:	Выводит комментарии к клиенту.<br>
Постусловия:	Если прецедент был успешно завершен, то пользователь может выполнять другие действия<br>
Альтернативные потоки:	—<br><br>

#### Таблица 9 Описание прецедента " Сортировка списка клиента "
Имя прецедента:	Сортировка списка клиента<br>
Краткое описание:	Прецедент позволяет сортировать данные списков клиентов<br>
Актеры:	Менеджер<br>
Предусловия:	Должен быть выполнен прецедент “Просмотр списка клиентов”<br>
Основной поток:	Сортирует клиентов<br>
Постусловия:	Если прецедент был успешно завершен, то пользователь может выполнять другие действия<br>
Альтернативные потоки:	—<br><br>

#### Таблица 10 Описание прецедента " Удаление клиента"
Имя прецедента:	Удаление клиента<br>
Краткое описание:	Прецедент позволяет удалять клиента из БД<br>
Актёры:	Менеджер<br>
Предусловия:	Должен быть выполнен прецедент “Просмотр одного клиента”<br>
Основной поток:	При нажатии на кнопку “Удалить”, текущая запись удаляется<br>
Постусловия:	Если прецедент был успешно завершен, то клиент удаляется из базы данных<br>
Альтернативные потоки:	—<br><br>

#### Таблица 11 Описание прецедента “Просмотр списка договоров”
Имя прецедента	Просмотр списка договоров<br>
Краткое описание	Прецедент позволяет просматривать список всех договоров<br>
Актёры	Менеджер<br>
Предусловия	Должен быть хотя бы один договор<br>
Основной поток	Выводится информация обо всех договорах в виде таблицы. Таблица содержится как в карточке клиента (в ней содержатся все договоры конкретного клиента), так и отдельно (в ней содержится список всех договоров)<br>
Постусловия	Если прецедент был успешно завершен, то пользователь может выполнять другие действия<br>
Альтернативные потоки	—<br><br>

#### Таблица 12 Описание прецедента " Просмотр одного договора"
Имя прецедента	Просмотр одного договора<br>
Краткое описание	Прецедент позволяет просматривать один конкретный договор<br>
Актёры	Менеджер<br>
Предусловия	Должен быть хотя бы один договор<br>
Основной поток	Выводится информация о конкретном договоре<br>
Постусловия	Если прецедент был успешно завершен, то пользователь может выполнять другие действия.<br>
Альтернативные потоки	—<br><br>

#### Таблица 13 Описание прецедента "Составление договора"
Имя прецедента	Составление договора<br>
Краткое описание	Прецедент позволяет заключать новые договора<br>
Актёры	Менеджер<br>
Предусловия	Должен быть клиент и менеджер<br>
Основной поток	Открывается форма добавления договора, куда вносятся необходимые данные<br>
Постусловия	Если прецедент был успешно завершен, то в БД добавляется новая договор<br>
Альтернативные потоки	Если имеются пустые поля, либо введены некорректные данные, то пользователю выдается сообщение об ошибке и дается возможность исправить данные<br><br>

#### Таблица 14 Описание прецедента "Просмотр списка договоров"
Имя прецедента	Сортировка списка договоров<br>
Краткое описание	Прецедент позволяет сортировать договора<br>
Актёры	Менеджер<br>
Предусловия	Должен быть выполнен прецедент “Просмотр списка договоров”<br>
Основной поток	Позволяет сортировать договоры<br>
Постусловия	Если прецедент был успешно завершен, то пользователь может выполнять другие действия<br>
Альтернативные потоки	—<br><br>

#### Таблица 15 Описание прецедента " Изменение данных в договоре "
Имя прецедента	Изменение данных в договоре<br>
Краткое описание	Прецедент позволяет редактировать данные в договоре<br><br>
Актёры	Менеджер<br>
Предусловия	Должен быть выполнен прецедент “Просмотр списка договоров”<br>
Основной поток	Открывается форма редактирования договора, где изменяются необходимые данные.<br>
Постусловия	Если прецедент был успешно завершен, то форма редактирования закрывается, и измененные данные сохраняются<br>
Альтернативные потоки	Если имеются пустые поля, либо введены некорректные данные, то пользователю выдается сообщение об ошибке и дается возможность исправить данные<br><br>

#### Таблица 16 Описание прецедента " Просмотра списка платежей "
Имя прецедента	Просмотра списка платежей<br>
Краткое описание	Прецедент позволяет просмотреть списки платежей<br>
Актёры	Менеджер<br>
Предусловия	Должен быть выполнен прецедент “Просмотр одного договора”<br>
Основной поток	Открываются платежи по договорам<br>
Постусловия	Если прецедент был успешно завершен, то пользователь может выполнять другие действия<br>
Альтернативные потоки	—<br><br>

#### Таблица 17 Описание прецедента "Удаление договора"
Имя прецедента	Удаление договора<br>
Краткое описание	Прецедент позволяет удалять договора<br>
Актёры	Менеджер<br>
Предусловия	Должен быть выполнен прецедент “Просмотр списка книг”<br>
Основной поток	При нажатии на кнопку “Удалить”, текущая запись удаляется<br>
Постусловия	Если прецедент был успешно завершен, то договор удаляется из базы данных<br>
Альтернативные потоки	—<br><br>

#### Таблица 18 Описание прецедента "Просмотр списка договоров"
Имя прецедента	Фильтрация списка договоров<br>
Краткое описание	Прецедент позволяет фильтровать договора<br>
Актёры	Менеджер<br>
Предусловия	Должен быть выполнен прецедент “Просмотр списка договоров”<br>
Основной поток	Позволяет фильтровать договоры<br>
Постусловия	Если прецедент был успешно завершен, то пользователь может выполнять другие действия<br>
Альтернативные потоки	—<br><br>


#### Таблица 19 Описание прецедента “Просмотр списка отчетов”
Имя прецедента	Просмотр списка отчетов<br>
Краткое описание	Прецедент позволяет просматривать список всех отчетов<br>
Актёры	Директор, менеджер<br>
Предусловия	Должен быть хотя бы один отчет<br>
Основной поток	Выводятся списки отчетов <br>
Постусловия	Если прецедент был успешно завершен, то пользователь может выполнять другие действия<br>
Альтернативные потоки	—<br><br>

#### Таблица 20 Описание прецедента "Добавление отчета"
Имя прецедента	Добавление отчета<br>
Краткое описание	Прецедент позволяет добавлять новые отчеты<br>
Актёры	Директор, менеджер<br>
Предусловия	Должны быть выполнены прецеденты «Просмотр списка отчетов»<br>
Основной поток	Открывается форма куда вносят данные отчета<br>
Постусловия	Если прецедент был успешно завершен, то в БД добавляется новый отчет<br>
Альтернативные потоки	Если имеются пустые поля, либо введены некорректные данные, то пользователю выдается сообщение об ошибке и дается возможность исправить данные<br><br>

#### Таблица 21 Описание прецедента "Изменение данных в отчетах"
Имя прецедента	Изменение данных в отчетах<br>
Краткое описание	Прецедент позволяет редактировать данные в отчетах<br>
Актёры	Директор, менеджер<br>
Предусловия	Должен быть выполнен прецедент “Просмотр списка отчетов”<br>
Основной поток	Открывается форма редактирования отчета, где изменяются необходимые данные.<br>
Постусловия	Если прецедент был успешно завершен, то форма редактирования закрывается, и измененные данные сохраняются<br>
Альтернативные потоки	Если имеются пустые поля, либо введены некорректные данные, то пользователю выдается сообщение об ошибке и дается возможность исправить данные<br><br>

#### Таблица 23 Описание прецедента "Удаление отчета"
Имя прецедента	Удаление отчета<br>
Краткое описание	Прецедент позволяет удалять отчет<br>
Актёры	Директор, менеджер<br>
Предусловия	Должен быть выполнен прецедент “Просмотр списка отчетов”<br>
Основной поток	При нажатии на кнопку “Удалить”, текущая запись удаляется<br><br>
Постусловия	Если прецедент был успешно завершен, то отчет удаляется из базы данных<br>
Альтернативные потоки	—<br>

#### Таблица 24 Описание прецедента " Сортировка списка отчетов"
Имя прецедента	Сортировка списка отчетов<br>
Краткое описание	Прецедент позволяет сортировать отчеты по выбранным данным<br>
Актёры	Директор, менеджер<br>
Предусловия	Должен быть выполнен прецедент “Просмотр списка отчетов”<br>
Основной поток	Позволяет сортировать отчеты<br>
Постусловия	Если прецедент был успешно завершен, то пользователь может выполнять другие действия.<br>
Альтернативные потоки	—<br><br>

#### Таблица 25 Описание прецедента " Фильтрация списка отчетов"
Имя прецедента	Фильтрация списка отчетов<br>
Краткое описание	Прецедент позволяет фильтровать отчеты<br>
Актёры	Менеджер, Директор<br>
Предусловия	Должен быть выполнен прецедент “Просмотр списка отчетов”<br>
Основной поток	Позволяет фильтровать отчеты<br>
Постусловия	Если прецедент был успешно завершен, то пользователь может выполнять другие действия.<br>
Альтернативные потоки	—<br><br>

#### Таблица 26 Описание прецедента "«Просмотр статистики вырученных денег за аренду ТС», «Просмотр статистики по менеджерам», «Просмотр статики по клиенту», «Просмотр статистики арендованных ТС»"
Имена прецедентов	«Просмотр статистики вырученных денег за аренду ТС», «Просмотр статистики по менеджерам», «Просмотр статики по клиенту», «Просмотр статистики арендованных ТС»<br>
Краткое описание	Прецеденты позволяют просматривать отчеты<br>
Актёры	Менеджер, Директор<br>
Предусловия	Должен быть выполнен прецедент “Просмотр списка отчетов”<br>
Основной поток	Позволяет просматривать все отчеты<br>
Постусловия	Если прецедент был успешно завершен, то пользователь может выполнять другие действия.<br>
Альтернативные потоки	—<br><br>

#### Таблица 27 Описание прецедента "Просмотр списка сотрудников"
Имя прецедента	Просмотр списка клиентов<br>
Краткое описание	Прецедент позволяет просматривать список всех сотрудников<br>
Актёры	Директор<br>
Предусловия	Должен быть хотя бы один сотрудник. Если таковых нет, то пользователю предлагается создать нового сотрудника<br>
Основной поток	Выводится информация обо всех сотрудниках в виде таблицы<br>
Постусловия	Если прецедент был успешно завершен, то пользователь может выполнять другие действия<br>
Альтернативные потоки	—<br><br>

#### Таблица 27 Описание прецедента "Добавление сотрудника"
Имя прецедента	Добавление сотрудника<br>
Краткое описание	Прецедент позволяет добавлять новых сотрудников<br>
Актёры	Директор<br>
Предусловия	Должен быть выполнен прецедент “Просмотр списка сотрудников”<br>
Основной поток	Открывается форма добавления нового сотрудника, куда заносятся все необходимые данные<br>
Постусловия	Если прецедент был успешно завершен, то форма добавления сотрудника закрывается, и в БД добавляется новый клиент<br>
Альтернативные потоки	Если имеются пустые поля, либо введены некорректные данные, то пользователю выдается сообщение об ошибке и дается возможность исправить данные<br><br>

#### Таблица 28 Описание прецедента "Редактирование данных о сотруднике"
Имя прецедента	Редактирование данных о сотруднике<br>
Краткое описание	Прецедент позволяет редактировать данные о сотруднике<br>
Актёры	Директор<br>
Предусловия	Должен быть выполнен прецедент “Просмотр одного сотрудника”<br>
Основной поток	Открывается форма редактирования клиента, где изменяются необходимые данные<br>
Постусловия	Если прецедент был успешно завершен, то форма редактирования сотрудника закрывается, и измененные данные о сотруднике сохраняются<br>
Альтернативные потоки	Если имеются пустые поля, либо введены некорректные данные, то пользователю выдается сообщение об ошибке и дается возможность исправить данные<br><br>

#### Таблица 29 Описание прецедента " Просмотр одного сотрудника"
Имя прецедента	Просмотр одного сотрудника<br>
Краткое описание	Прецедент позволяет просмотреть данные выбранного сотрудника<br>
Актёры	Директор<br>
Предусловия	Должен быть выполнен прецедент “Просмотр списка сотрудников ”<br>
Основной поток	Выводится вся информация о конкретном сотруднике<br>
Постусловия	Если прецедент был успешно завершен, то пользователь может выполнять другие действия<br>
Альтернативные потоки	—
