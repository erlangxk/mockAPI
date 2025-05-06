# Mockoon Server

This project is a mock server created using Mockoon, designed to facilitate the development and testing of applications by simulating API responses.

## Project Structure

```
mockAPI/
├── data.json                 # Mock response and other configurations for Mockoon 
├── package.json              # npm configuration file
├── Dockerfile                # Docker container configuration
├── docker-compose.yml        # Docker Compose configuration
├── .gitignore                # Files and directories to ignore by Git
└── README.md                 # Documentation for the project
```

## Setup Instructions

### Standard Setup

1. Clone the repository:
   ```
   git clone <repository-url>
   cd mockAPI
   ```

2. Install the dependencies:
   ```
   npm install
   ```

3. Start the mock server:
   ```
   npm start
   ```

### Docker Setup

1. Clone the repository:
   ```
   git clone <repository-url>
   cd mockAPI
   ```

2. Build and start the container using Docker Compose:
   ```
   docker-compose up -d
   ```

3. To stop the container:
   ```
   docker-compose down
   ```

## Usage

Once the server is running, you can send requests to the defined routes in the `data.json` file. The server will be available at `http://localhost:3000` by default (or the port specified in your data.json).

### Example Endpoints

- GET /users - Returns a list of users (with a 3-second delay)
- GET /users/:id - Returns a specific user by ID

You can modify the `data.json` file to add more routes, responses, or customize existing ones.

### Response Templates

The API uses Mockoon's templating system:
- URL parameters: `{{urlParam 'paramName'}}`
- Example: `/users/123` will return a user with id "123"

## Customizing the Mock Server

To customize the mock API:
1. Edit the `data.json` file directly, or
2. Use the Mockoon desktop application to create/modify your API and export the configuration to `data.json`

When using Docker, the `data.json` file is mounted as a volume, so you can modify it without rebuilding the container.

### Adding Latency

You can simulate network delays by setting the `latency` property (in milliseconds) in your response configurations:

```json
"responses": [
  {
    "latency": 3000,  // 3-second delay
    ...
  }
]
```

## Docker Configuration

The project includes Docker configuration for easy deployment:

- `Dockerfile`: Configures a Node.js 22 Alpine container to run the Mockoon server
- `docker-compose.yml`: Sets up the container with appropriate port mapping and volume mounting

### Customizing Docker Configuration

- To change the port mapping, edit the `ports` section in `docker-compose.yml`
- To add environment variables, add an `environment` section to the service in `docker-compose.yml`

## Contributing

Feel free to submit issues or pull requests if you have suggestions or improvements for the mock server.

## License

This project is licensed under the MIT License.