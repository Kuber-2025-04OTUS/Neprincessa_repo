# ДЗ №6

## Задание 1 
Создать 
Создатþ helm-chart позволāĀûий деплоитþ приложение, 
которое у вас полуùилосþ при вýполнении ДЗ 1-5. При 
ÿтом необходимо уùестþ:
● Основнýе параметрý в манифестах, такие как имена 
обüектов, имена контейнеров, исполþзуемýе образý, 
хостý, портý, колиùество запускаемýх реплик 
должнý бýтþ заданý как переменнýе в úаблонах и 
конфигурироватþсā ùерез values.yaml либо ùерез 
параметрý при установке релиза
● Репозиторий и тег образа не должнý бýтþ одним 
параметром
● Пробý должнý бýтþ вклĀùаемý/отклĀùаемý ùерез 
конфиг
● В notes должно бýтþ описано сообûение после 
установки релиза, отображаĀûее адрес, по которому 
можно обратитсā к сервису
● При именовании обüектов в úаблонах старайтесþ 
придерживатþсā best practice из лекøии
●  Добавþте в свой ùарт сервис-зависимостþ из 
доступнýх community-ùартов. Например mysql или 
redis.

helm create hw-app

# Переделать в нс номеворк
![alt text](image.png)

![alt text](image-1.png)

![alt text](image-2.png)

![alt text](image-3.png)

![alt text](image-4.png)
elm repo add bitnami https://charts.bitnami.com/bitnami
 1985  helm repo add stable https://charts.helm.sh/stable
 1986  helm dependency build .
 1987  helm repo add bitnami https://charts.bitnami.com/bitnami
 1988  helm dependency build .
 1989  helm dependency --help
 1990  helm dependency build .
![alt text](image-5.png)


helm pull oci://registry-1.docker.io/bitnamicharts/kafka
helm install my-release oci://registry-1.docker.io/bitnamicharts/kafka -f kubernetes-templating/kafka/values-dev.yaml 