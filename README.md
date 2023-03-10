# Домашнее задание к занятию 11.2. «Кеширование Redis/memcached» Баранов Сергей


---


### Задание 1. Кеширование 

###### Приведите примеры проблем, которые может решить кеширование. 

*Приведите ответ в свободной форме.*

Кэширование позволяет увеличивать производительность веб-приложений за счёт использования сохраненных ранее данных, вроде ответов на сетевые запросы или 
результатов вычислений. Благодаря кэшу, при очередном обращении клиента за одними и теми же данными, сервер может обслуживать запросы быстрее. Запросы к 
базам данных могут быть медленными и требовать серьезных системных ресурсов, так как серверу баз данных, для формирования ответа, нужно выполнять некие 
вычисления. Если запросы повторяются, кэширование их средствами базы данных поможет уменьшить время ее отклика. Кроме того, кэширование полезно в ситуациях, 
когда несколько компьютеров работают с базой данных, выполняя одинаковые запросы. В системах долговременного хранения информации кэш диска (его ещё называют 
буфером диска или кэширующим буфером) - это встроенная в жесткий диск память, которая играет роль буфера между процессором и физическим жестким диском. 
Дисковые кэши работают, исходя из предположения, что когда на диск что-то пишут, или с него что-то читают, есть вероятность того, что в ближайшем будущем к 
этим данным будут обращаться снова. В каждом браузере имеется реализация HTTP-кэша (его ещё называют веб-кэшем), который предназначен для временного хранения 
материалов, полученных из интернета, таких, как HTML-страницы, JavaScript-файлы и изображения. Перед нами весьма полезная технология, которая даёт следующие 
преимущества всем участникам обмена данными: 
* Улучшаются впечатления пользователя от работы с сайтом, так как ресурсы из локального кэша загружаются очень быстро. 
* Уменьшается нагрузка на серверное приложение и на другие серверные компоненты, ответственные за обработку запросов. 
* Высвобождается некоторая часть сетевых ресурсов, которыми теперь могут воспользоваться другие пользователи интернета, экономятся средства на оплату трафика.
В компьютерных сетях прокси-серверы могут быть представлены специальным аппаратным обеспечением или соответствующими приложениями. Они играют роль посредников 
между клиентами и серверами, хранящими данные, которые этим клиентам требуются. Кэширование - это одна из задач, которую они решают.
Отлично подходит для тяжелых операций чтения БД.


---


### Задание 2. Memcached

Установите и запустите memcached.

*Приведите скриншот systemctl status memcached, где будет видно, что memcached запущен.*

![monitoring](https://github.com/12sergey12/11.2_Redis_memcached/blob/main/images/11.2-2_memcached.png)


---


### Задание 3. Удаление по TTL в Memcached

###### Запишите в memcached несколько ключей с любыми именами и значениями, для которых выставлен TTL 5. 

*Приведите скриншот, на котором видно, что спустя 5 секунд ключи удалились из базы.*

![monitoring](https://github.com/12sergey12/11.2_Redis_memcached/blob/main/images/11.2-3_del.png)


---


### Задание 4. Запись данных в Redis

Запишите в Redis несколько ключей с любыми именами и значениями. 

*Через redis-cli достаньте все записанные ключи и значения из базы, приведите скриншот этой операции.*

![monitoring](https://github.com/12sergey12/11.2_Redis_memcached/blob/main/images/11.2-4_redis.png)
