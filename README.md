# LEMP-Stack-Demo
Summer xOps-Cloud Native 07/05/2022

อิงจาก
https://blog.pjjop.org/how-to-set-lemp-stack-with-docker-containers/

เพิ่ม phpmyadmin ลงไปใน docker-compose 
    
    phpmyadmin:
        image: phpmyadmin
        restart: always
        ports:
            - 8080:80
        environment:
            - MYSQL_USER=<user>
            - MYSQL_PASSWORD=<password>
            - PMA_HOST=<server>

อิงจาก https://hub.docker.com/r/phpmyadmin/phpmyadmin/

command
- docker build <สร้าง contrainer>
- docker run <run container>

- docker images <ดู image>
- docker rmi <image_id> <ลบ image>
- docker start , stop <contrainer_id> <เปิด ปิด contrainer>
- docker rm <contrainer_id> <ลบ contrainer>
- docker ps <ดู process>

- docker network create <name> 
- docker network ls
- docker network inspect <name> <ดูภายใน network>

- docker-compose up -d <start container จากไฟล์>
- docker-compose down <down container>
- docker-compose down --rmi all <down container และ ลบ all image>
