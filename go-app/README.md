# Go Application

This project is a simple Go application that can be built and run using Docker. It includes a GitHub Actions workflow for automatically publishing the Docker image to GitHub Container Registry.

## Project Structure

```
go-app
├── .github
│   └── workflows
│       └── docker-publish.yml
├── src
│   ├── main.go
├── Dockerfile
├── go.mod
├── go.sum
└── README.md
```

## Getting Started

### Prerequisites

- Go installed on your machine
- Docker installed on your machine

### Building the Application

To build the application, navigate to the project directory and run:

```bash
go build -o go-app ./src
```

### Running the Application

You can run the application directly using:

```bash
./go-app
```

### Building the Docker Image

To build the Docker image, use the following command:

```bash
docker build -t your-docker-image-name .
```

### Running the Docker Container

To run the Docker container, use:

```bash
docker run -p 8080:8080 your-docker-image-name
```

### GitHub Actions Workflow

The project includes a GitHub Actions workflow located at `.github/workflows/docker-publish.yml`. This workflow will automatically build and push the Docker image to GitHub Container Registry whenever changes are pushed to the `main` branch. 

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.