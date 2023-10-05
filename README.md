#Docker

для установки репозитория введите команду
git clone https://github.com/S-Maksim0/docker_node.git

затем для создания образа node перейдие в папку node

cd node

и запустите команду 

docker build -t image_name .

вместо image_name напишите своё название образа
и чтобы создать и запустить контейнер введите команду 
docker run -d -p 3000:3000 --name имя_контейнера


потом выйдите с папки с помощью команды cd .. и перейдите в папку postgres с помощью команды

cd postgres

затем создайте образ бд postgres

docker build -t image_name .

вместо image_name напишите своё название образа

docker run -d -p 3000:3000 --name имя_контейнера

чтобы совершать операции в бд использу  те команду
docker exec -it mydatabase-container psql -U myuser -d mydb

где mydatabase-container замените на название вашей бд

базовые операции sql

CREATE TABLE users (
    user_id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL,
    password VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
создание бд

INSERT INTO users (username, email, password) VALUES ('JohnDoe', 'johndoe@example.com', 'mypassword');
добавление пользователя


SELECT * FROM users; выводим всех пользователей


