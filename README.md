# Docker_Assignment

Tikhamporn Tepsut
Software Engineering II

How to RUN
use `docker-compose up`

If you can't reach "http://localhost/?username=alice", do this following step
`docker exec -it dockerassignment-db-1 /bin/bash`
`mysql -u root -p` ทำตามข้อสามในเอกสารที่อาจารย์บอก

ถ้ายังไม่ได้ให้ลอง `GRANT ALL PRIVILEGES ON *.* TO 'users_service'@'%';` ตามด้วย `FLUSH PRIVILEGES;` 
ถ้าถูกต้อง เมื่อลองใช้ `mysql -u users_service -p` และใช้ `show databases;` จะต้องมี Database ชื่อ ABCompany
จากนั้น `docker stop users_service` ตามด้วย `docker start users_service`
แล้วลองเข้าไปที่ "http://localhost/?username=alice" อีกครั้งจะพบว่าใช้งานได้แล้ว

HOW to check
run `curl -L "http://localhost/?username=alice" | json_pp`