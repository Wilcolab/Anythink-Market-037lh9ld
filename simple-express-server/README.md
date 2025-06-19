# Simple Express Server

This project is a simple Express server that listens on port 8001. It is designed to demonstrate the basic setup of an Express application with automatic restarts using Nodemon and Docker support.

## Getting Started

### Prerequisites

- Node.js (version 12 or higher)
- Yarn (version 1.22 or higher)
- Docker (optional, for containerization)

### Installation

1. Clone the repository:
   ```
   git clone <repository-url>
   cd simple-express-server
   ```

2. Install dependencies:
   ```
   yarn install
   ```

### Running the Server

To start the server with automatic restarts on code changes, use the following command:

```
yarn start
```

The server will be running at `http://localhost:8001`.

### Building the Docker Image

To build the Docker image for the application, run:

```
docker build -t simple-express-server .
```

### Running the Docker Container

After building the image, you can run the container with:

```
docker run -p 8001:8001 simple-express-server
```

The server will be accessible at `http://localhost:8001`.

### License

This project is licensed under the MIT License.