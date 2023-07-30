#See https://aka.ms/customizecontainer to learn how to customize your debug container and how Visual Studio uses this Dockerfile to build your images for faster debugging.


# per windows
#FROM mcr.microsoft.com/dotnet/aspnet:7.0 AS base


# per linux
FROM mcr.microsoft.com/dotnet/aspnet:7.0-jammy AS base
 



WORKDIR /app
EXPOSE 80
EXPOSE 443





COPY ./TestBlazorArm64/bin/Release/net7.0/ /app/

#COPY ./bin/Release/net7.0/publish/ /app/

ENTRYPOINT ["dotnet", "TestBlazorArm64.dll"]


#FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build
#WORKDIR /src
#COPY ["TestBlazorArm64/TestBlazorArm64.csproj", "TestBlazorArm64/"]
#RUN dotnet restore "TestBlazorArm64/TestBlazorArm64.csproj"
#COPY . .
#WORKDIR "/src/TestBlazorArm64"
#RUN dotnet build "TestBlazorArm64.csproj" -c Release -o /app/build

#FROM build AS publish
#RUN dotnet publish "TestBlazorArm64.csproj" -c Release -o /app/publish /p:UseAppHost=false
#
#FROM base AS final
#WORKDIR /app
#COPY --from=publish /app/publish .
#ENTRYPOINT ["dotnet", "TestBlazorArm64.dll"]
