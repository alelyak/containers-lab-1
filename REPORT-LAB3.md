# Отчет по практической работе №3
## Студент: [EAL]
## Группа: [16]
## Дата выполнения: [02.04.2026] 
### 1. Подготовка узлов 
#### 1.1 Версия ОС и настройки
Обновление системы и установка базовых пакетов

![Обновление системы и установка базовых пакетов](screenshots-lab3/image.png)
![Обновление системы и установка базовых пакетов](screenshots-lab3/image2.png)

Версия ОС

![Версия ОС](screenshots-lab3/image3.png)

Редактирование /etc/hosts

![Редактирование /etc/hosts](screenshots-lab3/image4.png)

##### Проверка связи между узлами

На k8s-master

![Проверка связи между узлами](screenshots-lab3/image5.png)

На k8s-worker1

![Проверка связи между узлами](screenshots-lab3/image6.png)

На k8s-worker2

![Проверка связи между узлами](screenshots-lab3/image7.png)
#### 1.2 Отключение swap 
На k8s-master

![Отключение swap](screenshots-lab3/image8.png)

На k8s-worker1

![Отключение swap](screenshots-lab3/image9.png)

На k8s-worker2

![Отключение swap](screenshots-lab3/image10.png)
#### 1.3 Модули ядра 
Настройка модулей ядра

На k8s-master

![Настройка модулей ядра](screenshots-lab3/image11.png)

На k8s-worker1

![Настройка модулей ядра](screenshots-lab3/image12.png)

На k8s-worker2

![Настройка модулей ядра](screenshots-lab3/image13.png)

##### Настройка параметров sysctl для Kubernetes

На k8s-master

![Настройка параметров sysctl для Kubernetes](screenshots-lab3/image14.png)

На k8s-worker1

![Настройка параметров sysctl для Kubernetes](screenshots-lab3/image15.png)

На k8s-worker2

![Настройка параметров sysctl для Kubernetes](screenshots-lab3/image16.png)
### 2. Установка containerd 

На k8s-master

![Установка containerd](screenshots-lab3/image17.png)

На k8s-worker1

![Установка containerd](screenshots-lab3/image18.png)

На k8s-worker2

![Установка containerd](screenshots-lab3/image19.png)

#### 2.1 Версия containerd 
![Версия containerd](screenshots-lab3/image20.png)
#### 2.2 Конфигурация containerd 
Настройка containerd

На k8s-master

![Настройка containerd](screenshots-lab3/image21.png)
![Настройка containerd](screenshots-lab3/image22.png)

На k8s-worker1

![Настройка containerd](screenshots-lab3/image23.png)
![Настройка containerd](screenshots-lab3/image24.png)

На k8s-worker2

![Настройка containerd](screenshots-lab3/image25.png)
![Настройка containerd](screenshots-lab3/image26.png)

Содержимое /etc/containerd/config.toml после настройки

![Содержимое /etc/containerd/config.toml после настройки](screenshots-lab3/image27.png)
### 3. Установка kubeadm 
Добавление репозитория Kubernetes

На k8s-master

![Добавление репозитория Kubernetes](screenshots-lab3/image28.png)

На k8s-worker1

![Добавление репозитория Kubernetes](screenshots-lab3/image29.png)

На k8s-worker2

![Добавление репозитория Kubernetes](screenshots-lab3/image30.png)

Установка компонентов

На k8s-master

![Установка компонентов](screenshots-lab3/image31.png)

На k8s-worker1

![Установка компонентов](screenshots-lab3/image32.png)

На k8s-worker2

![Установка компонентов](screenshots-lab3/image33.png)
#### 3.1 Версии компонентов 
Фиксация версий и проверка установленных версий

На k8s-master

![Фиксация версий и проверка установленных версий](screenshots-lab3/image34.png)

На k8s-worker1

![Фиксация версий и проверка установленных версий](screenshots-lab3/image35.png)

На k8s-worker2

![Фиксация версий и проверка установленных версий](screenshots-lab3/image36.png)
### 4. Инициализация кластера 
Настройка kubelet

На k8s-master

![Настройка kubelet](screenshots-lab3/image37.png)

На k8s-worker1

![Настройка kubelet](screenshots-lab3/image38.png)

На k8s-worker2

![Настройка kubelet](screenshots-lab3/image39.png)

Проверка, что все необходимые порты свободны

![Проверка, что все необходимые порты свободны](screenshots-lab3/image40.png)

Инициализация control plane

![Инициализация control plane](screenshots-lab3/image41.png)
![Инициализация control plane](screenshots-lab3/image42.png)

Настройка kubectl для обычного пользователя

![Настройка kubectl для обычного пользователя](screenshots-lab3/image43.png)

Присоединение k8s-worker1 к кластеру

![Присоединение k8s-worker1 к кластеру](screenshots-lab3/image44.png)

Присоединение k8s-worker2 к кластеру

![Присоединение k8s-worker2 к кластеру](screenshots-lab3/image45.png)
#### 4.1 Узлы кластера 
Присвоение ролей узлам и вывод списка узлов кластера

![Присвоение ролей узлам и вывод списка узлов кластера](screenshots-lab3/image46.png)
#### 4.2 Поды в namespace kube-system 
![Поды в namespace kube-system](screenshots-lab3/image47.png)
### 5. Сетевые компоненты 
#### 5.1 Calico 
Установка Tigera Calico operator

![Установка Tigera Calico operator](screenshots-lab3/image48.png)

Редактирование custom-resources.yaml и вывод kubectl get pods -n calico-system

![Редактирование custom-resources.yaml и вывод kubectl get pods -n calico-system](screenshots-lab3/image49.png)
#### 5.2 MetalLB 
Установка MetalLB

![Установка MetalLB](screenshots-lab3/image50.png)

Применение конфигурации и вывод списка подов и пула адресов

![Применение конфигурации и вывод списка подов и пула адресов](screenshots-lab3/image51.png)
[вставьте вывод kubectl get ipaddresspools -n metallb-system] 
#### 5.3 Ingress Controller 
Установка NGINX Ingress Controller

![Установка NGINX Ingress Controller](screenshots-lab3/image52.png)

Вывод списка подов и сервисов

![Вывод списка подов и сервисов](screenshots-lab3/image53.png)

Применение конфигурации

![Применение конфигурации](screenshots-lab3/image54.png)
### 6. Развернутое приложение 
Подготовка namespace

![Подготовка namespace](screenshots-lab3/image55.png)

Создание директории для манифестов

![Создание директории для манифестов](screenshots-lab3/image56.png)

Применение всех манифестов

![Применение всех манифестов](screenshots-lab3/image57.png)


#### 6.1 Все ресурсы в namespace lab3-app 
![Все ресурсы в namespace lab3-app](screenshots-lab3/image58.png)
#### 6.2 PersistentVolumeClaim 
![PersistentVolumeClaim](screenshots-lab3/image59.png)
### 7. Скриншоты 
Настройка локального доступа
![Настройка локального доступа](screenshots-lab3/image60.png)
#### 7.1 Главная страница приложения 
![Главная страница](screenshots-lab3/main-page.png) 
#### 7.2 Дашборд с информацией о поде 
![Pod info](screenshots-lab3/pod-info.png) 
#### 7.3 Список пользователей из БД 
![Users list](screenshots-lab3/users-list.png) 
### 8. Тестирование отказоустойчивости 
Проверка самовосстановления

![Проверка самовосстановления](screenshots-lab3/image61.png)
#### 8.1 Симуляция отказа узла 
Временная остановка kubelet на k8s-worker1 и последующий запуск

![Временная остановка kubelet на k8s-worker1 и последующий запуск](screenshots-lab3/image62.png)

Наблюдение за статусом узла

![Наблюдение за статусом узла](screenshots-lab3/image63.png)

Перезапущенные поды на другом узле

![Перезапущенные поды на другом узле](screenshots-lab3/image64.png)
#### 8.2 Проверка сохранности данных 
Удаление пода с PostgreSQL и проверка сохранности данных после перезапуска

![Удаление пода с PostgreSQL и проверка сохранности данных после перезапуска](screenshots-lab3/image65.png)
### 9. Ответы на контрольные вопросы
1. Какие компоненты входят в control plane и какова их роль?

Kube-apiserver - предоставляет RESTful API, через который пользователи, инструменты командной строки (например, kubectl) и другие компоненты Kubernetes взаимодействуют с кластером.

Kube-scheduler - компонент, который отвечает за назначение новых подов на доступные Worker Nodes.

Kube Controller Manager - центральный компонент Control Plane, который запускает процессы контроллеров, каждый из которых следит за изменениями на сервере API Kubernetes и стремится, чтобы текущее состояние соответствовало желаемому, определённому в спецификациях ресурсов.

Etcd - распределённое хранилище типа «ключ-значение», которое служит базой данных для всего кластера Kubernetes. Хранит все конфигурационные данные, состояние кластера, метаданные объектов и информацию о желаемом состоянии кластера.

2. Чем отличается развертывание с kubeadm от использования Minikube?

Minikube предназначен для запуска локального одноузлового кластера на одном компьютере, подходит для тестирования приложений перед развёртыванием.

Kubeadm предназначен для развёртывания кластера из нескольких узлов на разных компьютерах, Он автоматизирует процесс: настраивает узел управления (запускающий etcd, API-сервер, контроллер-менеджер, планировщик) и присоединяет рабочие узлы к нему. Подходит для Production-ready развёртывания.

3. Для чего нужен CNI-плагин и какую роль выполняет Calico?

CNI нужен для настройки сети в подах и обеспечения их связности. Calico выполняет роль сетевого плагина, который обеспечивает подключение подов к сети, управляет маршрутизацией и поддерживает сетевые политики.

4. В чем разница между Service типа NodePort, LoadBalancer и Ingress?

NodePort - открывает определённый порт на каждом узле кластера. Это обеспечивает прямой сетевой доступ без анализа URL и HTTP-заголовков. Запросы поступают на IP-адрес ноды и указанный порт, затем передаются к сервису.

LoadBalancer - создаёт внешний балансировщик нагрузки через облачного провайдера (или Metallb). Это перенаправляет входящий трафик на NodePort или ClusterIP.

Ingress - обеспечивает маршрутизацию на основе доменного имени и URL. Позволяет использовать общий внешний IP-адрес для нескольких сервисов.

5. Как обеспечивается отказоустойчивость control plane?

Обеспечивается за счёт распределения компонентов между несколькими узлами.

### 10. Выводы 
Из нового я узнал, как устанавливать сетевой плагин Calico, балансировщик нагрузки Metallb и NGINX Ingress Controller для управления внешним доступом. Узнал один из новых способов предоставления внешнего доступа к подам в кластере.
При развёртывании кластера понадобилось дополнительно создать StorageClass local-path, а также сервис nginx, о чём не было сказано в практической работе, а также сначала некорректно работал фронтенд, его пришлось исправлять. В остальном проблем не было.
