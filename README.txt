docker build -t grpcgreeter -f Dockerfile .
docker create --name grpcgreeter -p 5001:5001 grpcgreeter