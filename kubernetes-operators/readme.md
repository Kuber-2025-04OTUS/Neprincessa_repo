# Задание 1

create resources:

```
kubectl apply -f sa.yaml -f clusterrole.yaml -f crb.yaml -f crd.yaml 
kubectl apply -f deployment.yaml 
kubectl apply -f mysqlcrd.yaml
```

## Проверка работоспособности

- для оператора 

![alt text](image-1.png)

- для crd
![alt text](image-2.png)

## Удаление ресурсов

Видно, что были ресурсы, включая pv,pvc и при удалении mysql crd удаляется всё

![alt text](image-3.png)

## проверка валидности паттерна
если указать некорректное значение в размере, то выдаёт ошибку 

![alt text](image-4.png)


# For Test
kubectl delete -f mysqlcrd.yaml
kubectl delete -f deployment.yaml 
kubectl delete -f sa.yaml -f clusterrole.yaml -f crb.yaml -f crd.yaml 