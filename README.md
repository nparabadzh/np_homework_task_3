# Network programming homework - task 3
Homework for the "Network programming" course in FMI - 2019.  


### Условие на задача 3
`Да се преработи кодът от Java simple echo. Вместо сървърът да отваря нова нишка (thread) за всеки клиент, да създава thread pool, от който да се заемат временно нишки със синхронизация.`

1. Стартиране на приложенията\
В два отделни проекта в IntelliJ, Eclipse или друго IDE за JAVA се стартира първо TCPmultiServer_threads класа (в конзолата изкарва "Listening"), а след това се стартира TCP_echo_client класа. След пускането на TCP_echo_client, в конзолата изкарва: "Enter IP address of the server: ", където въвеждаме 127.0.0.1. Ако връзката е реализирана, на конзолата на TCP_echo_client се изкарва "Connected to echo server (127.0.0.1)", a в конзолата на TCPmultiServer_threads се изкарва "Got connection from /127.0.0.1". Всичко написано в конзолата на TCP_echo_client (например "something") след това би трябвало да се отрази в конзолата на TCPmultiServer_threads "Test: something". Така тестваме, че работи.

2. Допълнителни библиотеки\
Допълнителни класове, които съм използвала за създаването на Thread pool, са ExecutorService и Executors. Тъй като те са част от Java.util те не трябва да се свалят допълнително.

#### Note
Относно синхронизацията: нишките не използват споделени ресурси затова използването на методи за синхронизация не е необходимо.
