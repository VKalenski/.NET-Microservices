# **Platform Service**

>[1. Platform Service](#platform-service)
>
>[2. Initial Commands](#initial-commands)
>
>[3. Docker Commands](#docker-commands)
>
>[4. Kubernetes Commands](#kubernetes-commands)
>
>[5. .NET Commands](#net-commands)

---

### **Platform Service**

- Function as an "Asset Register";
- Track all the platforms / systems in the company;
- Built by the infrastructure team;
- User by:
    - Infrastructure team;
    - Technical Support Team;
    - Engineering;
    - Accounting;
    - Procurement.

---

### **Initial Commands**

> **Create new web api with name PlatformService:**
```
dotnet new webapi -n PlatformService --framework net6.0
```

> **Open in VS Code:**
```
code -r PlatformService
```

> **Add some packages:**
```dotnet add package AutoMapper.Extensions.Microsoft.DependencyInjection```
```dotnet add package Microsoft.EntityFrameworkCore```
```dotnet add package Microsoft.EntityFrameworkCore.Design: https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.Design/```
```dotnet add package Microsoft.EntityFrameworkCore.InMemory```
```dotnet add package Microsoft.EntityFrameworkCore.SqlServer```

> **Check .NET version:**
```
dotnet --version
```

> **Build project:**
```
dotnet build
```

> **Run project:**
```
dotnet run
```

---

### **Docker Commands**

> **Check Docker version:**
```
docker --version
```
--
> **Build docker image:**
```
docker build -t vilislavkalenski/platformservice .
```

> **Run docker image with current port (8080:80):**
```
docker run -p 8080:80 -d vilislavkalenski/platformservice
```

> **Show docker containers:**
```
docker ps
```
> **Push docker image:**
```
docker push vilislavkalenski/platformservice
```

> **Stop docker image:**
```
docker stop IdDocker
```

> **Start docker image:**
```
docker start IdDocker
```

---

### **Kubernetes Commands**

> *To deploy into DockerHub -> Kubernetes function is must be "**ON**" in Docker Desktop*

> **Check K8s version:**
```
kubectl version
```

> **Get all pods in current namespace (default):**
```
kubectl get pods
```

> **Apply current deployment file in K8s:**
```
kubectl apply -f platforms-depl.yml
```

> **Get all deployments in current namespace (default):**
```
kubectl get deployments
```

> **Delete current deployment file in namespace (default):**
```
kubectl delete deployment platforms-depl
```

> **Apply current service file in K8s:**
```
kubectl apply -f platforms-np-srv.yml
```

> **Get all services in current namespace (default):**
```
kubectl get services
```

---

### .NET Commands

> **Create .NET migration:**
```
dotnet-ef migrations add InitialCreate
```