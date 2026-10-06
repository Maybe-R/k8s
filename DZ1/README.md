# Домашнее задание к занятию «Запуск приложений в K8S»

## Чеклист готовности к домашнему заданию

### Установленное k8s-решение (например, MicroK8S).
<img width="667" height="370" alt="image" src="https://github.com/user-attachments/assets/57321e4d-66d7-4711-8066-5e812c577392" />

### Установленный локальный kubectl.

<img width="373" height="77" alt="image" src="https://github.com/user-attachments/assets/d8237ac5-e2d4-4b1e-8192-8d95edc2f2e1" />

В качестве редактора YAML-файлов с подключённым git-репозиторием использую Visual Studio Code.

## Задание 1. Создать Deployment и обеспечить доступ к репликам приложения из другого Pod

1. Создаем в поде два контейнера, описанные в деплое. В деплое меняем порт одного контейнера, так как у двух сервисов числился одинаковый.

<img width="942" height="980" alt="image" src="https://github.com/user-attachments/assets/045eb983-5897-44aa-8f2d-a8bf511a8837" />

2. Увеличиваем количество реплик
   
<img width="989" height="279" alt="image" src="https://github.com/user-attachments/assets/26811a09-dc0f-473f-9952-fafc64d9feb1" />

3. Создаем сервис Service и отдельный Pod-клиент

<img width="859" height="975" alt="image" src="https://github.com/user-attachments/assets/9e779328-bede-4adb-8481-741a9c87d580" />

4. Проверяем доступность из пода в приложение

<img width="982" height="545" alt="image" src="https://github.com/user-attachments/assets/e3baf691-9eae-4add-b713-ab6740304e62" />

Манифесты - https://github.com/Maybe-R/k8s/tree/main/DZ1/task1

## Задание 2. Создать Deployment и обеспечить старт основного контейнера при выполнении условий

Создаем новый файл деплоя, прописываем init-контейнер на образе busybox, который выполняет требования ожидания запуска.

<img width="696" height="873" alt="image" src="https://github.com/user-attachments/assets/e597b4ab-4d31-436b-871b-0984a6cf4654" />

Убеждаемся, что nginx не стартует - в блоке Init Containers: wait-for-service

<img width="1105" height="974" alt="image" src="https://github.com/user-attachments/assets/c2f28494-af97-46b5-af7d-6662c9986378" />

Создаем сервис, запускаем его и проверяем, что nginx стартует

<img width="778" height="981" alt="image" src="https://github.com/user-attachments/assets/247ecc73-9201-4c53-8ade-12a66f810e96" />

Манифесты - https://github.com/Maybe-R/k8s/tree/main/DZ1/task2
