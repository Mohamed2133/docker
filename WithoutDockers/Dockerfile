FROM microsoft/aspnetcore:1.1

WORKDIR /app

COPY *.csproj ./
COPY . ./

#COPY ${source:-obj/Docker/publish} .
FROM microsoft/aspnetcore:1.1
WORKDIR /app
COPY --from=build-env /app/out .
ENTRYPOINT ["dotnet", "WithoutDockers.dll"]



