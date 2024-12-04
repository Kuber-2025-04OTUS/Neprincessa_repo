curl -k -v -H "Authorization: Bearer $TOKEN" https://10.96.0.1:443/metrics

# HT
- В namespace homework создать service account monitoring и дать ему доступ к эндпоинту /metrics вашего кластера

- Изменить манифест deployment из прошлых ДЗ так, чтобы поды запускались под service account monitoring

- В namespace homework создать service account с именем cd и дать ему роль admin в рамках namespace homework

- Создать kubeconfig длā service account cd

- Сгенерировать для service account cd токен с временем действия 1 день и сохранить его в файл token
