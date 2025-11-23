# project-flask-modules

A minimal Flask application demonstrating a simple REST server integrated with a Neo4j database. This project serves as a basic testcase to illustrate Flask routing and Neo4j connectivity using a custom Neo4j driver wrapper.

## Features

- Basic Flask web server with a root endpoint.
- Endpoint to initialize a Neo4j driver and run a test query.
- JSON response with the number of nodes retrieved from Neo4j.

## Tech Stack

- Python 3
- Flask
- Neo4j Python Driver (custom wrapper `neo_native_app`)

## Getting Started

### Prerequisites

- Python 3.6 or higher
- Neo4j database running and accessible

### Installation

1. Clone the repository:

```bash
git clone https://github.com/justin-napolitano/project-flask-modules.git
cd project-flask-modules
```

2. (Recommended) Create and activate a virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

3. Install dependencies:

```bash
pip install flask neo4j
```

*Note:* The project imports a custom module `neo_native_app` which is not included in this repository. Ensure this module is available in your Python path.

### Running the Server

```bash
python rest_server.py
```

The server will start on `http://0.0.0.0:5000` by default.

### Endpoints

- `/` : Returns a simple greeting message.
- `/init_neo_driver` : Initializes the Neo4j driver and returns the number of nodes in the database as JSON.

## Project Structure

```
project-flask-modules/
└── rest_server.py  # Main Flask application
```

- `rest_server.py`: Contains the Flask app, routes, and logic to connect to Neo4j using a custom driver.

## Future Work / Roadmap

- Add error handling for database connection failures.
- Include configuration management for database credentials and connection parameters.
- Expand API to support more complex queries and data manipulation.
- Add unit and integration tests.
- Package the custom Neo4j driver or include it as a submodule/dependency.
- Dockerize the application for easier deployment.
