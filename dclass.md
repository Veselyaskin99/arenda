# Диаграмма классов
![](https://user-images.githubusercontent.com/74318083/102002830-55655080-3d3b-11eb-9b89-438c23301b20.png)



Person
Класс Person является предком классов Worker, Parent и Student. Этот класс содержит атрибуты: ID, FIO, Phone, editDate, delDate.
Client
Данный класс наследует все операции класса Person. Этот класс содержит атрибуты Person и атрибут: Comments(комментарии).
+Client() – конструктор класса Student без параметров;
+Client(ID: Int) – конструктор класса Student принимающий в качестве параметра Id сотрудника;
+add() – функция добавления человека в БД;
+del() – функция удаления человека из БД;
+edit() – функция изменений данных о человеке;
+ getContracts(): List<Contract> – функция для удобного обращения к функции из класса allContracts, которая возвращает список договоров, заключенных c выбранным клиентом;
allClients
Класс, связанный агрегацией «один-ко-многим» с классом Client. 
+ findAll( editDate: DateTime, delDate: DateTime, clNumber: Int, ID: Int, FIO: String, Phone: String, Contract: Contract, sorting : String, ASKorDESK : String,  count : Int, page : Int): List<Student> — функция с входными параметрами ID, FIO, Phone, Contract, sorting – поле, по которому будет осуществляться сортировка, ASKofDESK - по возрастанию или по убыванию,  count – количество.  Функция возвращает список всех найденных клиентов, удовлетворяющих условиям. Если введены параметры для сортировки, то данные будут отсортированы.
Worker
Данный класс наследует все операции класса Person. Этот класс содержит атрибуты Person и атрибуты: Position (должность), Password, Rate - ставка.
+Worker() – конструктор класса Worker без параметров;
+Worker(ID: Int) – конструктор класса Worker принимающий в качестве параметра Id сотрудника;
+add() – функция добавления человека в БД;
+del() – функция удаления человека из БД;
+edit() – функция изменений данных о человеке;
+ getContracts(): List<Contract> – функция для удобного обращения к функции из класса allContracts, которая возвращает список договоров, заключенных выбранным менеджером;
allWorkers
Класс, связанный агрегацией «один-ко-многим» с классом Worker. 
+ findAll( editDate: DateTime, delDate: DateTime, worNumber: Int, ID: Int, FIO: String, Position: String, sorting : String, ASKorDESK : String,  count : Int, page : Int): List<Worker> — функция с входными параметрами Status, ID, FIO, Position - должность, sorting – поле, по которому будет осуществляться сортировка, ASKofDESK - по возрастанию или по убыванию,  count – количество.  Функция возвращает список всех найденных работников, удовлетворяющих условиям. Если введены параметры для сортировки, то данные будут отсортированы.
Contract
Данный класс содержит атрибуты: ID, DateEnd, DateEndFact, DateStart – дата заключения договора, Client, Worker, Status, TS, Price.
+Contract() – конструктор класса Contract без параметров;
+Contract(ID: Int) – конструктор класса Contract принимающий в качестве параметра Id договора;
+add() – функция добавления договора в БД;
+del() – функция удаления договора из БД;
+edit() – функция изменений данных о договоре;
+ addPay(Payment: Double): String– добавление оплаты по договору;
+ Cancellation(): String – функция для расторжения договора.
allContracts
Класс, связанный агрегацией «один-ко-многим» с классом Contract. 
+ findAll(conNumber: Int,  ID: Int, Date: DateTime, Client: Client, Worker: Worker, Cost: Double,  dateStart, dateEnd, dateEndFact, sorting : String, ASKorDESK : String,  count : Int, page : Int): List<Contract>  — функция с входными параметрами ID, Date – дата заключения договора, Client, Worker – менеджер, который заключил договор, Cost – цена за ТС, dateStart – дата заключения договора, dateEnd – дата, когда нужно сдать ТС, dateEndFact – дата когда был сдано ТС, sorting – поле, по которому будет осуществляться сортировка, ASKofDESK - по возрастанию или по убыванию,  count – количество.  Функция возвращает список всех найденных договоров, удовлетворяющих условиям. Если введены параметры для сортировки, то данные будут отсортированы.
TS
Класс отображающий все ТС. 
Атрибуты:  Price(цена), Status (арендована или нет) , Category (категория), State number (гос номер), Brand car model (модель машины), History (История повреждений).
+add() – функция добавления книги в БД;
+del() – функция удаления книги из БД;
+save() – функция сохранения изменений;
+ getContracts():List<Contract> - получает всю историю аренды ТС.
allTS
+ findAll(Price: Double,  State number: String, Brand car model: string, sorting : String, ASKorDESK : String,  count : Int, page : Int): List<TS>  — функция с входными параметрами ID, State number – гос номер ТС, brand car model – модель машины, Price – цена за ТС, , sorting – поле, по которому будет осуществляться сортировка, ASKofDESK - по возрастанию или по убыванию,  count – количество.  Функция возвращает список всех найденных ТС, удовлетворяющих условиям. Если введены параметры для сортировки, то данные будут отсортированы.
Pay
Данный класс содержит атрибуты: Contract (для заключения договора между клиентом и центром), Worker (для выплаты зарплаты), Indicator (Показывает – заключение договора или выплата зарплаты), Date, Payment, editDate, delDate. 
+Pay() – конструктор класса Pay без параметров;
+add() – функция добавления оплаты в БД;
+del() – функция удаления оплаты из БД;
+edit() – функция изменений данных об оплате.
allPay
Класс, связанный агрегацией «один-ко-многим» с классом Pay. 
+ findAll( editDate, delDate, payNumber: Int, Contract: Contract, Worker: Worker, Indicator: Boolean, Date: DateTime, Payment: Double, sorting : String, ASKorDESK : String,  count : Int, page : Int): List<Pay> — функция с входными параметрами payNumber – количество выводимых оплат, Contract – договор, по которому требуется получить оплаты, Date, Payment – оплата, sorting – поле, по которому будет осуществляться сортировка, ASKofDESK - по возрастанию или по убыванию,  count – количество.  Функция возвращает список всех найденных оплат, удовлетворяющих условиям. Если введены параметры для сортировки, то данные будут отсортированы.
