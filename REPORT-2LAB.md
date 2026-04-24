# Отчет по практической работе №2
## Студент: [Elyakova Alesya Lvovna]
## Группа: [16]
## Дата выполнения: [20.04.2026] 
### 1. Информация о кластере 
#### 1.1 Статус Minikube
Проверка установки kubernetes

![Проверка установки kubernetes](screenshots-lab2/image.png)

Запуск minikube

![Запуск minikube](screenshots-lab2/image2.png)

Статус minikube

![Статус minikube](screenshots-lab2/image3.png)

Включение дополнений

![Включение дополнений](screenshots-lab2/image4.png)

Проверка создания секрета

![Проверка создания секрета](screenshots-lab2/image5.png)

#### 1.2 Узлы кластера 
Информация о кластере

![Информация о кластере](screenshots-lab2/image6.png)

Список узлов

![Список узлов](screenshots-lab2/image7.png)

Вывод kubectl describe nodes

![Вывод kubectl describe nodes](screenshots-lab2/image8.png)
![Вывод kubectl describe nodes](screenshots-lab2/image9.png)
![Вывод kubectl describe nodes](screenshots-lab2/image10.png)

Список доступных API-ресурсов

![Список доступных API-ресурсов](screenshots-lab2/image11.png)

Просмотр конфигурации

![Просмотр конфигурации](screenshots-lab2/image12.png)
![Просмотр конфигурации](screenshots-lab2/image13.png)

#### Практическое задание 
Сохранение вывода команды kubectl get nodes -o wide в файл nodes.txt

![Сохранение вывода](screenshots-lab2/image14.png)

![Сохранение вывода](screenshots-lab2/image15.png)

### 2. Созданные ресурсы 
#### 2.1 Pods 

Применение манифеста

![Применение манифеста](screenshots-lab2/image16.png)

Просмотр подов

![Просмотр подов](screenshots-lab2/image17.png)

Детальная информация
![Детальная информация](screenshots-lab2/image18.png)

Логи

![Логи](screenshots-lab2/image19.png)

Выполнение команд в поде

![Выполнение команд в поде](screenshots-lab2/image20.png)

Удаление пода

![Удаление пода](screenshots-lab2/image22.png)

#### Практическое задание

Манифест пода

![Манифест пода](screenshots-lab2/image23.png)

Cтатус пода после запуска

![Cтатус пода после запуска](screenshots-lab2/image24.png)

Сохранение логов в файл

![Сохранение логов в файл](screenshots-lab2/image25.png)
![Сохранение логов в файл](screenshots-lab2/image26.png)

#### Работа с ReplicaSet

Создание ReplicaSet

![Создание ReplicaSet](screenshots-lab2/image27.png)

Просмотр ReplicaSet

![Просмотр ReplicaSet](screenshots-lab2/image28.png)

Просмотр созданных подов

![Просмотр созданных подов](screenshots-lab2/image29.png)

Масштабирование вручную

![Масштабирование вручную](screenshots-lab2/image30.png)

Наблюдение вручную

![Наблюдение вручную](screenshots-lab2/image31.png)

Эксперимент с самовосстановлением

![Эксперимент с самовосстановлением](screenshots-lab2/image32.png)

#### 2.2 Deployments 

Применение манифеста

![Применение манифеста](screenshots-lab2/image33.png)

Просмотр Deployment

![Просмотр Deployment](screenshots-lab2/image34.png)
![Просмотр Deployment](screenshots-lab2/image35.png)

Просмотр созданного ReplicaSet

![Просмотр созданного ReplicaSet](screenshots-lab2/image36.png)

Просмотр подов

![Просмотр подов](screenshots-lab2/image37.png)

Просмотр истории обновлений

![Просмотр истории обновлений](screenshots-lab2/image38.png)

Масштабирование через Deployment

![Масштабирование через Deployment](screenshots-lab2/image39.png)

Обновление образа

![Обновление образа](screenshots-lab2/image40.png)

Откат изменений

![Откат изменений](screenshots-lab2/image41.png)

Практическое задание

Deployment для PostgreSQL

![Deployment для PostgreSQL](screenshots-lab2/image42.png)
![Deployment для PostgreSQL](screenshots-lab2/image43.png)

Применение манифеста

![Применение манифеста](screenshots-lab2/image44.png)

Статус Deployments

![Статус Deployments](screenshots-lab2/image45.png)

Статус подов и логи Go-App

![Статус подов и логи Go-App](screenshots-lab2/image46.png)

#### 2.3 Services 
Создание сервисов

![Создание сервисов](screenshots-lab2/image47.png)

Просмотр сервисов

![Просмотр сервисов](screenshots-lab2/image48.png)

Детальная информация

![Детальная информация](screenshots-lab2/image49.png)

Проверка DNS-резолвинга внутри кластера

![Проверка DNS-резолвинга внутри кластера](screenshots-lab2/image50.png)

#### Валидация YAML
Проверка синтаксиса YAML с помощью онлайн-сервиса yamllint

![Проверка синтаксиса YAML](screenshots-lab2/image51.png)

Сухая проверка (dry-run) в Kubernetes

![Сухая проверка (dry-run) в Kubernetes](screenshots-lab2/image52.png)

Получение объяснения по полям

![Получение объяснения по полям](screenshots-lab2/image53.png)
![Получение объяснения по полям](screenshots-lab2/image54.png)
![Получение объяснения по полям](screenshots-lab2/image55.png)

Валидация с помощью kubeconform (это усовершенствованная версия kubeval, который устарел)

![Валидация с помощью kubeconform](screenshots-lab2/image56.png)

#### Отладка приложений
Просмотр событий в кластере

![Просмотр событий в кластере](screenshots-lab2/image57.png)

Просмотр логов конкретного пода

![Просмотр логов конкретного пода](screenshots-lab2/image58.png)

Просмотр логов предыдущей инстанции пода

![Просмотр логов предыдущей инстанции пода](screenshots-lab2/image59.png)

Порт-форвардинг для доступа к приложению без Service

![Порт-форвардинг для доступа к приложению без Service](screenshots-lab2/image60.png)

Интерактивная отладка - запуск временного пода в той же сети

![Интерактивная отладка - запуск временного пода в той же сети](screenshots-lab2/image61.png)

#### Мониторинг через Dashboard
Запуск дашборда

![Запуск дашборда](screenshots-lab2/image62.png)

Открытый дашборд (1 упавший под - из практического задания в 2.1 Pods)

![Открытый дашборд](screenshots-lab2/image63.png)

#### Последовательный запуск всех компонентов
Применение всех манифестов

![Применение всех манифестов](screenshots-lab2/image64.png)

Проверка статуса

![Проверка статуса](screenshots-lab2/image65.png)

Ожидание готовности

![Ожидание готовности](screenshots-lab2/image66.png)

Получение URL для доступа к приложению

![Получение URL для доступа к приложению](screenshots-lab2/image67.png)

### 3. Скриншоты работы приложения 
#### 3.1 Главная страница 
![Главная страница](screenshots-lab2/main-page.png) 
#### 3.2 Дашборд Kubernetes 
![Kubernetes Dashboard](screenshots-lab2/dashboard.png) 
![Kubernetes Dashboard](screenshots-lab2/dashboard2.png) 
![Kubernetes Dashboard](screenshots-lab2/dashboard3.png) 
#### 3.3 Результат GET /api/users 
![API Response](screenshots-lab2/api-response.png) 
### 4. Эксперименты с масштабированием 
#### 4.1 Масштабирование до 5 реплик 
Масштабирование до 5 реплик

![Масштабирование до 5 реплик](screenshots-lab2/image68.png)

Статус подов Go-App после масштабирования

![Статус подов Go-App после масштабирования](screenshots-lab2/image69.png)

#### 4.2 Проверка распределения нагрузки 
Команда PowerShell для нагрузочного тестирования

![Команда PowerShell для нагрузочного тестирования](screenshots-lab2/image70.png)

Логи nginx с разных подов

![Логи nginx с разных подов](screenshots-lab2/image71.png)

### 5. GitHub Actions 
#### 5.1 Успешная валидация манифестов 
![GitHub Actions Validation](screenshots-lab2/github-actions.png) 
### 6. Ответы на контрольные вопросы
1. В чем разница между Pod и Deployment?

Pod — минимальная единица развертывания в Kubernetes,
Deployment — более высокоуровневый объект, который управляет подами, ReplicaSet обеспечивает стратегии обновления, отката и масштабирования.

2. Для чего нужен Service типа ClusterIP?

Для организации внутреннего взаимодействия между компонентами приложения, развёрнутого в одном кластере. Он создаёт внутренний IP-адрес внутри кластера, который позволяет другим подам внутри кластера взаимодействовать с сервисом, но недоступен из внешней сети.

3. Как ReplicaSet обеспечивает самовосстановление?

При удалении какого-то пода из ReplicaSet взамен него автоматически создаётся новый.

4. Что произойдет с приложением, если удалить под PostgreSQL?

Если удалить под PostgreSQL, то приложение продолжит работать, на странице в информации о поде в поле Status значение поменяется на unhealthy, пропадут записи о пользователях из БД. Затем через небольшой промежуток времени автоматически создадится новый под PostgreSQL, в поле Status снова будет записано healthy, и записи о пользователях снова появятся, они подтянутся из init-script.

### 7. Выводы 
Из нового я узнала, как работать с Kubernetes и  Minikube, валидировать YAML, проводить отладку приложений, проводить проверку DNS-резолвинга внутри кластера, мониторинг через Dashboard и как проводить нагрузочное тестирование. 
