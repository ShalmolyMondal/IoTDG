<div align="center">

  <h1>Situation Based IoT Data Generator</h1>

</div>

# Local Development

Prerequisites

#### node_be : 14.x (last tested version : 14.19.3)
#### ui : 8.x (last tested version : 8.17.0)

## Installation

Clone the repository or download the code files.

  ```bash
  git clone https://github.com/ShalmolyMondal/IoTDG.git
  ```

## Front-End Development

Navigate to `IoTDG/ui/public-src'

### Install the dependencies (with respective node versions) by running the following command

```bash
npm install
```
### Start the server by running the following command

```bash
npm run server
```

- This will start the server and listen on port 8090.
- The application can then be accessed using http://localhost:8090/situations/.

## Back-End Development

Navigate to `IoTDG/node_be'

### Install dependencies (with respective node versions) by running the following command

```bash
npm install
```
### Start the development server by running the following command
```bash
npm run dev
```

- The “npm run” command can be used to run the production build instead of “npm run dev”.
- The backend application is set up to run under port 9080, configured on the node_be/app.js file.
  

## FastAPI Development

### Run the following command to start the FastAPI server
```bash
uvicorn main:app --reload
```

## License

Unless you explicitly state otherwise, any contribution intentionally submitted for inclusion by you shall be licensed at the discretion of the repository maintainers without any additional terms or conditions.
