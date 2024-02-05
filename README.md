Certainly! Here's the README file with proper formatting:

# Deployment Instructions

## Prerequisites:

- Docker
- Kubernetes (locally, you can use Minikube)
- kubectl (Kubernetes command-line tool)

## Steps:

### 1. Build the Docker Image:

- Navigate to the directory containing your Dockerfile.
- Run the following command to build the image:
    ```bash
    docker build -t <image_name>:<tag> .
    ```
    Replace `<image_name>` and `<tag>` with your desired values.

### 2. Deploy the Pod:

- Apply the `course.yml` file to deploy the pod:
    ```bash
    kubectl apply -f course.yml
    ```
- Verify pod status:
    ```bash
    kubectl get pods
    ```

### 3. Create the Service:

- Apply the `service.yml` file to create the service:
    ```bash
    kubectl apply -f service.yml
    ```

### 4. Access the Application:

- Get the Minikube IP address:
    ```bash
    minikube ip
    ```
- Use the Minikube IP address and the port specified in your service to access the application in your browser:
    ```
    http://<minikube_ip>:<port>
    ```

Make sure to replace `<minikube_ip>` and `<port>` with the actual values obtained.

---
