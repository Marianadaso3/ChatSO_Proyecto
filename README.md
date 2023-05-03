# SistosChat

protoc --c_out=. chat.proto


gcc -o servidor servidor.c chat.pb-c.c -pthread -lprotobuf-c

./servidor 8080


gcc -o cliente cliente.c chat.pb-c.c -pthread -lprotobuf-c

./cliente usuario1 127.0.0.1 8080 

status

1 -> ACTIVO
2 -> OCUPADO
3 -> INACTIVO