# DevOps Cheat Sheet

## 1. **Docker Commands**

| Command                      | Description                                   |
|------------------------------|-----------------------------------------------|
| `docker --version`           | Check Docker version.                         |
| `docker pull <image>`        | Download a Docker image from a registry.     |
| `docker images`              | List downloaded Docker images.               |
| `docker rmi <image>`         | Remove a Docker image.                        |
| `docker run <image>`         | Run a container from a Docker image.         |
| `docker ps`                  | List running containers.                      |
| `docker stop <container>`     | Stop a running container.                     |
| `docker exec -it <container> /bin/bash` | Access the terminal of a running container. |
| `docker-compose up`          | Start services defined in a `docker-compose.yml` file. |
| `docker-compose down`        | Stop and remove containers defined in a `docker-compose.yml` file. |

---

## 2. **Kubernetes Commands**

| Command                      | Description                                   |
|------------------------------|-----------------------------------------------|
| `kubectl version`            | Check Kubernetes version.                     |
| `kubectl get nodes`          | List all nodes in the cluster.               |
| `kubectl get pods`           | List all pods in the current namespace.      |
| `kubectl create -f <file>`   | Create resources defined in a YAML file.     |
| `kubectl apply -f <file>`    | Apply changes defined in a YAML file.        |
| `kubectl delete pod <name>`   | Delete a specific pod.                        |
| `kubectl exec -it <pod> -- /bin/bash` | Access the terminal of a running pod.       |
| `kubectl logs <pod>`         | View logs of a specific pod.                  |

---

## 3. **CI/CD Principles and Tools**

| Principle/Tool             | Description                                   |
|----------------------------|-----------------------------------------------|
| **Continuous Integration**  | Automatically test and integrate code changes. |
| **Continuous Delivery**     | Automatically deploy every change to a testing/staging environment. |
| **Continuous Deployment**   | Automatically deploy every change to production. |
| **GitHub Actions**          | CI/CD tool integrated with GitHub repositories. |
| **Travis CI**              | CI service for GitHub projects.              |
| **CircleCI**               | Cloud-based CI/CD service for automated testing and deployment. |
| **Jenkins**                | Open-source automation server for CI/CD.     |

---

## 4. **Infrastructure as Code Basics (Terraform)**

| Command                      | Description                                   |
|------------------------------|-----------------------------------------------|
| `terraform --version`        | Check Terraform version.                      |
| `terraform init`             | Initialize a Terraform configuration.        |
| `terraform plan`             | Preview changes before applying.             |
| `terraform apply`            | Apply changes to reach the desired state.    |
| `terraform destroy`          | Remove all resources defined in the configuration. |
| `terraform fmt`              | Format Terraform files to a canonical format. |
| `terraform validate`         | Validate the configuration files.            |
| `terraform output`           | Display outputs defined in the configuration. |

---

## 5. **Best Practices**

| Practice                   | Description                                   |
|----------------------------|-----------------------------------------------|
| **Version Control**        | Keep all configuration files in version control. |
| **Automate Everything**    | Automate manual processes to minimize errors. |
| **Use Environment Variables** | Manage sensitive data securely.            |
| **Monitor and Log**        | Implement monitoring and logging for observability. |
| **Documentation**          | Keep documentation up to date for processes and infrastructure. |

---

This **DevOps Cheat Sheet** provides a comprehensive overview of Docker, Kubernetes, CI/CD principles and tools, and Infrastructure as Code with Terraform.

Key Command
Ctrl/Cmd + B Toggle bold
Ctrl/Cmd + I Toggle italic
Alt+S (on Windows) Toggle strikethrough1
Ctrl + Shift + ] Toggle heading (uplevel)
Ctrl + Shift + [ Toggle heading (downlevel)
Ctrl/Cmd + M Toggle math environment
Alt + C Check/Uncheck task list item
Ctrl/Cmd + Shift + V Toggle preview
Ctrl/Cmd + K V Toggle preview to side
