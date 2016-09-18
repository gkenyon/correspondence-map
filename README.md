# Correspondence Map
A geographic visualization of correspondence between abolitionists in the 19th century

## Why this project exists

# Project Set Up
This project consists of two parts:
1. A parser for downloading data from the DPLA API
2. A map that visualizes the data using LeafletJS

## Parser
1. In order to use the parser you will need to install NodeJS.
2. After installing Node, you will need to install the project dependencies
   1. Open a command line and navigate to the parser folder where the project is located
   2. run `npm install`. This will create a folder called `node_modules` and will install the libraries you need into it.
3. Create a file call `config.json` in the `parser` folder with the text below. Replace `[API Key]` with your DPLA API key.

   ```
   {
     "api_key": "79b1c904be68acc69e3cab2a5242433b"
   }
   ```
4. From the command window run `node get-data.js`. This will download the data into a file called letters.csv

## Setting up the map
### Remote web server
If you have a website with FTP access, the easiest thing to do is copy all the files into this repository to your web server in a folder called something like `map`. The map then should be available on your website at that folder i.e. `http://www.yourdomain.com/map`

### Local web server
There are a number of ways to run a local web server, one of the easiest with Node is to use the `node-server` module.
1. Open a command line and nagivate to the folder where the project is located.
2. Run `npm install -g jitsu`
3. Run `jitsu install http-server`
4. Run `node bin/http-server`

There will now be a server running by default on port 8080. To visit the map open a browser and go to `http://localhost:8080`

To stop the server you will hit `Ctrl-C`. To start the server again, you don't need to download it again, just run `node bin/http-server`
