# Anythink Market Servers

This project contains two servers: a FastAPI server implemented in Python and a Node.js server implemented with Express. Both provide routes for managing a task list.

## Project Structure

- `python-server/src/main.py`: FastAPI server implementation (Python). Handles adding and retrieving tasks.
- `python-server/src/__init__.py`: Marks the `src` directory as a Python package.
- `python-server/requirements.txt`: Python dependencies for the FastAPI server.
- `python-server/Dockerfile`: Docker image for the FastAPI server.
- `simple-express-server/src/server.js`: Express server implementation (Node.js). Handles the same task routes as the Python server.
- `simple-express-server/package.json` and `yarn.lock`: Node.js dependencies.
- `simple-express-server/Dockerfile`: Docker image for the Express server.
- `docker-compose.yml`: Defines and runs both servers as Docker services.

## Getting Started

To run both servers using Docker Compose:

```shell
docker compose up
```

- The FastAPI server will be available at port `8000`.
- The Node.js Express server will be available at port `8001`.

## API Routes (Both Servers)

- `GET /` (Node.js only): Returns "Hello World".
- `POST /tasks`: Adds a task to the task list. The request body should contain `{ "text": "your task" }`.
- `GET /tasks`: Retrieves the task list.

## Migration Details

The endpoints from the Python FastAPI server have been fully migrated to the Node.js Express server. Both servers now provide the same API for managing tasks. You can use either server interchangeably for development or testing.
