# GraphQL AI

This project is a simple GraphQL server using Apollo Server and TypeScript.

## Project Structure
```
graphql-ai/
├── src/
│ ├── index.ts
├── Dockerfile
├── docker-compose.yml
├── package.json
├── tsconfig.json
└── README.md
```

## Setup Instructions

### Prerequisites

- Node.js >= 18.0.0

### Installation

1. Clone the repository:
    ```sh
    git clone git@gitlab.com:software-hideout/graphql-ai.git
    cd graphql-ai
    ```

2. Initialize npm and set type to module:
    ```sh
    npm init --yes && npm pkg set type="module"
    ```

3. Install dependencies:
    ```sh
    npm install @apollo/server graphql
    npm install --save-dev typescript @types/node
    npm install
    ```

### Running the Project

1. Compile the TypeScript code:
    ```sh
    npm run compile
    ```

2. Start the server:
    ```sh
    npm run start
    ```

3. Open your browser and navigate to `http://localhost:4000/graphql`.

### Docker
To build and run the Docker container, run the following commands:
```sh
cd graphql-ai
docker build -t graphql-ai .
docker run -p 4000:4000 graphql-ai
#Or use docker-compose:
docker-compose up
```

## License

This project is licensed under the ISC License.
