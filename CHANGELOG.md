<div align="center">

  <img src="https://user-images.githubusercontent.com/4072962/38543709-fb04c520-3cad-11e8-8e23-0bb1155f16ae.png" />

  <h1>Situation Based IoT Data Generator</h1>

</div>

# Running the code

Prerequisites

#### node_be : 14.x (last running version : 14.19.3)
#### ui : 8.x (last running version : 8.17.0)

## Installation
Clone the repository or download the code files.

```bash
git clone https://github.com/ShalmolyMondal/IoTDG.git
```

## Front-End 

Navigate to IoTDG/ui/public-src

### Install dependencies (with respective node versions)

```bash
npm install
```

## Back-End 

Navigate to IoTDG/node_be

### Install dependencies (with respective node versions)

```bash
npm install
```

The “npm start” command can be used to run the production build instead of “npm run dev”. 
The backend application is set up to run under port 9080, configured on the node_be/app.js file.


####FastAPI :

```bash
uvicorn main:app --reload
```

The frontend project is served on port 8090. The application can then be accessed using http://localhost:8090/situations/.


#node_be => Node version : 14.19.3 (windows) npm run dev
#UI => Node version : 8.17.0 (windows) (use lts of 8.x) => local port : 9100 npm run server
#python uvicorn main:app --reload
