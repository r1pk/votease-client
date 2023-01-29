# VotEase-client

VotEase-client is a responsive application written in React which uses tools such as [Redux](https://redux.js.org/), [Material UI](https://mui.com/getting-started/usage/) and [Colyseus.js](https://www.colyseus.io/). VotEase is a voting app that can be used to quickly determine the best option from a list of available options.

## Screenshots

Create room page
![Create Room Page](https://i.imgur.com/8KeSChW.png)

Join room page
![Join Room Page](https://i.imgur.com/Natc3Aj.png)

Room page
![Room Page](https://i.imgur.com/2An3bgR.png)

## Pre-requisites

- [node.js v18+ or higher](https://nodejs.org/en/)
- [npm v8.0 or higher](https://nodejs.org/en/download/)

## Installation

Clone VotEase-client repository

```bash
git clone https://github.com/r1pk/votease-client.git master
```

Install all dependencies

```bash
cd ./master
npm install
```

Before running the application, configure the environment variables to provide the application with [server](https://github.com/r1pk/votease-server.git) address

```env
VITE_BASE_APP_TITLE=VotEase              # Application title used as a prefix for the document title
VITE_COLYSEUS_URL=                       # Colyseus server address

VITE_USERNAME_LOCALSTORAGE_KEY=username  # Local storage key used to store username
```

Run the app in development mode

```bash
npm run dev
```

After running the application, open `localhost:5173` in your browser.

Build the app for production to the `build` folder

```bash
npm run build
```

## Project structure

```bash
public                            # static files
src
   |-- api                        # api related folders and files
   |   |-- group                  # group of files related to a single api
   |   |   |-- index.js           # exports main api instance from the folder
   |-- components                 # grouped components used in the application
   |   |-- group                  # group of components
   |-- features                   # feature based modules
   |   |-- feature                # feature module
   |   |   |-- components         # components used in the feature
   |   |   |-- schemas            # schemas used in the feature forms
   |   |   |-- constants          # constants used across the feature
   |   |   |-- utils              # utility functions used in the feature components
   |   |   |-- index.js           # exports components from the feature
   |-- hooks                      # custom hooks used mostly in the page components
   |-- layouts                    # app layouts
   |   |-- layout                 # single layout
   |   |   |-- index.js           # exports main layout component from the folder
   |-- pages                      # page components
   |-- redux                      # redux related files
   |   |-- slices                 # redux toolkit store slices
   |   |-- store.js               # initializes redux store
   |   |-- index.js               # exports redux related files from the folder
   |-- routes                     # routes used in the application
   |   |-- AppRoutes.jsx          # available routes in the application
   |-- theme                      # theme related files used in the application
   |   |-- darkTheme.js           # dark theme object used in the application
   |-- App.jsx                    # main application component
   |-- main.jsx                   # entry point of the application
.env                              # file containing environment variables
```

## Live Demo

Application is automatically deployed using Vercel.

[Live demo](https://votease.vercel.app)

## Author

- Patryk [r1pk](https://github.com/r1pk) Krawczyk

## License

- [MIT](https://choosealicense.com/licenses/mit/)
