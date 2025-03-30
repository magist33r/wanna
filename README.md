alien Ввел команду sudo yum install wget

image

Ввел команду su root, что бы зайти в командную строку от имени администратора после этого ввел команду vi /etc/sudoers

Далее вылезли команды image Дал права администратора пользователю

Что бы сохранить использовал команду :wq! что бы выйти без сохранения :q!

Скачал пакеты с помощью команды sudo yum install wget Пакет: wget-1.21.1-8.el9_4.x86_64 image

Использовал команду sudo yum install curl image Для работы с веб-ресурсами через сетевые протоколы. Для установки утилиты curl в дистрибутивах Linux Ввел команду sudo wget -P /etc/yum.repos.d/ https://download.docker.com/linux/centos/docker-ce.repo image Используется для скачивания конфигурационного файла репозитория Docker в CentOS. Это необходимо для установки Docker, чтобы получить наиболее актуальную версию программы.

Устанавливаем docker с помощью команды sudo yum install docker-ce docker-ce-cli containerd.io image После этого подверждаем установку image После этого еще раз подверждаем установку image Вводим команду sudo systemctl enable docker --now image Команда запускает службу Docker и настраивает её на автоматический запуск при загрузке системы.

sudo curl -L "https://github.com/docker/compose/releases/download/$COMVER/docker-compose-$(uname -s)-$(uname -m)" -o /usr/bin/docker-compose image Эта команда позволяет загрузить последнюю версию Docker Compose и заменить существующую, если она есть

sudo chmod +x /usr/bin/docker-compose image Эта команда необходима, если при использовании утилиты возникают проблемы с правами на выполнение.

docker-compose –version image Позволяет посмотреть версию команды docker-compose.

git clone https://github.com/skl256/grafana_stack_for_docker.git image Клонирует репозиторий по ссылке на компьютер. При клонировании на локальную машину копируются файлы и папки проекта, а также вся его история

Sudo yum install git image image Устанавливает Git и его зависимости в системе

git clone https://github.com/skl256/grafana_stack_for_docker.git image Создаём локальную копию репозитория по указанному URL. cd grafana_stack_for_docker image позволяет перейти в каталог с содержимым репозитория grafana_stack_for_docker

sudo mkdir -p /mnt/common_volume/swarm/grafana/config image Создаём папку с именем «config» в пути /mnt/common_volume/swarm/grafana. sudo chown -R 
(
i
d
−
u
)
:
(id -g) {/mnt/common_volume/swarm/grafana/config,/mnt/common_volume/grafana} image меняем владельца и группу для указанных папок и их содержимого touch /mnt/common_volume/grafana/grafana-config/grafana.ini image создаём файл grafana.ini в папке grafana-config в каталоге /mnt/common_volume.

cp config/* /mnt/common_volume/swarm/grafana/config/ image после выполнения этой команды все файлы из каталога config будут скопированы в каталог /mnt/common_volume/swarm/grafana/config/.

mv grafana.yaml docker-compose.yaml image после выполнения этой команды файл grafana.yaml будет переименован в docker-compose.yaml.

sudo docker compose up -d image Docker Compose начинает создавать и запускать все сервисы, указанные в docker-compose.yml файле. флаг -d: Ctrl + C: Прерывает (остановливает) выполнение текущей команды или процесса в терминале. Если запустили контейнеры без флага -d, использование Ctrl + C остановит их. Ctrl + Z: Приостанавливает выполнение текущего процесса и переводит его в фоновый режим. Это позволяе вернуться к терминалу и продолжить работу, но при этом процесс останется приостановленным. Чтобы вернуть процесс в активное состояние, можно использовать команду fg. image

image

sudo docker-compose image

sudo docker-compose stop image используется для остановки запущенных контейнеров sudo docker-compose down image остановил и удалили все контейнеры sudo docker-compose up -d image снова запустил контейнеры sudo docker-compose ps image вывел список запущенных контейнеров с их статусами и портами переход в папку cd grafana_stack_for_docker и выполнение комнады git clone https://github.com/Kokokii/alien.git image

cp docker-compose.yaml docker-compose.yaml1 image

cd /mnt/common_volume/swarm/grafana/config и cp prometheus.yaml prometheus.yaml1 image

image

image

image

echo -e "# TYPE light_metric1 gauge\nlight_metric1 39" | curl --data-binary @- http://localhost:8428/api/v1/import/prometheus image

Ввел connect null value (always) image
