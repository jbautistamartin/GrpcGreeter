docker build -t grpcgreeter -f Dockerfile .

--> Para contenedores Windows.

docker create --name grpcgreeter -p 5001:5001 -e ASPNETCORE_Kestrel__Certificates__Default__Password=GrpcGreeter -e ASPNETCORE_Kestrel__Certificates__Default__Path=C:\App\GrpcGreeter.pfx --user ContainerAdministrator grpcgreeter

--> Para contenedores Linux.

docker create --name grpcgreeter -p 5001:5001 -e ASPNETCORE_Kestrel__Certificates__Default__Password=GrpcGreeter -e ASPNETCORE_Kestrel__Certificates__Default__Path=/App/GrpcGreeter.pfx grpcgreeter


docker run --rm -it -p 8000:80 -p 8001:443 -e ASPNETCORE_URLS="https://+;http://+" -e ASPNETCORE_HTTPS_PORT=8001 -e ASPNETCORE_Kestrel__Certificates__Default__Password="<CREDENTIAL_PLACEHOLDER>" -e ASPNETCORE_Kestrel__Certificates__Default__Path=/https/aspnetapp.pfx -v %USERPROFILE%\.aspnet\https:/https/ mcr.microsoft.com/dotnet/samples:aspnetapp
