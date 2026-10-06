# Домашнее задание к занятию «Сетевое взаимодействие в Kubernetes»

## Задание 1: Настройка Service (ClusterIP и NodePort)

Создадим новый namespace и пишем новый деплой , применяем деплой

<img width="770" height="993" alt="image" src="https://github.com/user-attachments/assets/28f18c48-99fb-4823-b883-8e70b9f584d0" />

Проверяем запуск трех реплик 

<img width="952" height="105" alt="image" src="https://github.com/user-attachments/assets/d425ea91-1813-40dd-b22e-8f1041945835" />

Создаем ClusterIP Service

<img width="896" height="793" alt="image" src="https://github.com/user-attachments/assets/a37d1c94-36b7-494e-815b-e5b2f7ada59e" />

Проверяем порты 

<img width="1185" height="257" alt="image" src="https://github.com/user-attachments/assets/790c68cc-5c70-4fe2-9dab-0871123a2647" />

Проверяем доступ изнутри кластера к приложениям по портам 9001 и 9002

<img width="1182" height="679" alt="image" src="https://github.com/user-attachments/assets/f1f449a4-eedd-4645-9000-400c32c4078b" />

Создаем сервис NodePort, где на порт 30080 принимает снаружи и перенаправляет на порт 80 внутри

<img width="1003" height="946" alt="image" src="https://github.com/user-attachments/assets/5981d850-8574-4493-ba58-e656124b3d1d" />
<img width="713" height="77" alt="image" src="https://github.com/user-attachments/assets/a3bacfc8-d084-4c91-bb0b-0baf301bf833" />


