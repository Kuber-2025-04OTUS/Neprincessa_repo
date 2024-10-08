# Volumes, StorageClass, PV, PVC

## Основное задание
- Создать манифест pvc.yaml, описывающий PersistentVolumeClaim, запрашивающий хранилище 
storageClass по-умолчанию
- Создать манифест cm.yaml для объекта типа configMap, описывающий произвольный набор пар ключ-значение
- В манифесте deployment.yaml изменить спецификацию volume типа emptyDir, который монтируется в init и основной контейнер, на pvc, созданный в предыдущем пункте
- В манифесте deployment.yaml добавить монтирование ранее созданного configMap как volume к основному контейнеру пода в директориĀ /homework/conf, так, чтобы его содержимое можно было получить, обратившись по url /conf/file


## Задание со *
- Создать манифест storageClass.yaml, описывающий объект типа storageClass с provisioner https://k8s.io/minikube-hostpath и reclaimPolicy Retain
- Изменить манифест pvc.yaml так, чтобы в нем запрашивалось хранилище созданного вами storageClassа
