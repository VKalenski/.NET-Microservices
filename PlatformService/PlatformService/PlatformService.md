### Platform Service

- Function as an "Asset Register"
- Track all the platforms / systems in the company
- Built by the infrastructure team
- User by: 
    - Infrastructure team
    - Technical Support Team
    - Engineering
    - Accounting
    - Procurement

---

- ```dotnet new webapi -n PlatformService --framework net6.0```
- code -r PlatformService
- dotnet add package AutoMapper.Extensions.Microsoft.DependencyInjection
- dotnet add package Microsoft.EntityFrameworkCore
- dotnet add package Microsoft.EntityFrameworkCore.Design: https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.Design/
- dotnet add package Microsoft.EntityFrameworkCore.InMemory
- dotnet add package Microsoft.EntityFrameworkCore.SqlServer
- dotnet build
- dotnet run
- prop + TAB -> for create property
- Ctrl + B -> hide the panel

- docker --version

- docker build -t vilislavkalenski/platformservice .
- docker run -p 8080:80 -d vilislavkalenski/platformservice
- docker ps
- docker stop IdDocker
- docker start IdDocker
- docker push vilislavkalenski/platformservice


To deploy into DockerHub -> Kubernetes function is must be on in Docker Desktop
- kubectl version
- kubectl get pods
- kubectl apply -f platforms-depl.yml
- kubectl get deployments
- kubectl delete deployment platforms-depl.yml

- kubectl apply -f platforms-np-srv.yml
- kubectl get services