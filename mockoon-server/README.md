# Mockoon Server

This project is a mock server created using Mockoon, designed to facilitate the development and testing of applications by simulating API responses.

## Project Structure

```
mockoon-server
├── data.json                  # mock response and other configurations for the Mockoon 
├── package.json               # npm configuration file
├── .gitignore                 # Files and directories to ignore by Git
└── README.md                  # Documentation for the project
```

## Setup Instructions

1. Clone the repository:
   ```
   git clone <repository-url>
   cd mockoon-server
   ```

2. Install the dependencies:
   ```
   npm install
   ```

3. Start the mock server:
   ```
   npm start
   ```

## Usage

Once the server is running, you can send requests to the defined routes in the `data.json` file. The server will be available at `http://localhost:3000` by default (or the port specified in your data.json).

### Example Endpoints

- GET /users - Returns a list of users
- GET /users/:id - Returns a specific user by ID

You can modify the `data.json` file to add more routes, responses, or customize existing ones.

## Customizing the Mock Server

To customize the mock API:
1. Edit the `data.json` file directly, or
2. Use the Mockoon desktop application to create/modify your API and export the configuration to `data.json`

## Contributing

Feel free to submit issues or pull requests if you have suggestions or improvements for the mock server.

## License

This project is licensed under the MIT License.