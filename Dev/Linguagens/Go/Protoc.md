#Fazer 
comando para gerar 
 protoc --go_out=./app/grpc/pb --go_opt=paths=source_relative --go-grpc_out=./app/grpc/pb --go-grpc_opt=paths=source_relative --proto_path=./app/grpc/proto ./app/grpc/proto/*.proto