# Wormplay frontend

## Description

An online two-player word game that uses webcam for facial recognition. Upon entering the lobby, players can pull faces to represent four different emotions at their webcam, and the emotion recognition API detects which emotion is being expressed, and takes a photo at the correct moment. These photos of the player's own face are transferred onto the 'word worm' - a 2D physics object that crawls around the screen, onto which the player drops Scrabble tiles to spell out words and get points against their opponent.

The game provides:

- A login and lobby system to find other users online to play against
  - React
- An in-game chatroom
  - Socket.IO
- A webcam feature with facial and emotion recognition
  - Facial recognition API
- A 2D physics game
  - Phaser
- Realtime connections to allow both players to see each other's in-game action instantly
  - Backend server using Express and Socket.IO
- Checking of valid words during gameplay
  - Oxford English Dictionary API

This was the final project at the [Northcoders](https://northcoders.com/) coding bootcamp, and was thought of, designed, developed, and tested all within two weeks. The project started just at the beginning of the Covid-19 lockdown in the UK, and so the team of four collaborated entirely remotely, using Trello as a kanban board, daily standups, and Agile method throughout.

## The Team

[James Johnson](https://github.com/Brork)
<br/>
[Patrick Mackridge](https://github.com/PatrickMackridge)
<br/>
[Chris Matus](https://github.com/chicorycolumn)
<br/>
[Nadia Rashad](https://github.com/nadiarashad)

The team's presentation can be found [here](https://www.youtube.com/watch?v=NdILlpRjQAg).

## Instructions

This frontend is live on [Netlify](https://wormplay.netlify.app/).
<br/>
The backend counterpart repository can be found [here](https://github.com/nadiarashad/wormplay-BE).
<br/>
You can also download this repository and run the project locally by following these steps:

1. Fork this repository by clicking the button labelled 'Fork' on the [project page](https://github.com/chicorycolumn/wormplay-FE).
   <br/>
   Copy the url of your forked copy of the repository, and run `git clone the_url_of_your_forked_copy` in a Terminal window on your computer, replacing the long underscored word with your url.
   <br/>
   If you are unsure, instructions on forking can be found [here](https://guides.github.com/activities/forking/) or [here](https://www.toolsqa.com/git/git-fork/), and cloning [here](https://www.wikihow.com/Clone-a-Repository-on-Github) or [here](https://www.howtogeek.com/451360/how-to-clone-a-github-repository/).

2. Open the project in a code editor, and run `npm install` to install necessary packages. You may also need to install [Node.js](https://nodejs.org/en/) by running `npm install node.js`.

3. Run `npm start` to open the project in development mode.
   <br/>
   Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Deploy

General instructions for taking a **React project** and hosting it on **Netlify** for **automatic deployment** are as follows:

0. Ensure the project is initialised in a Git repository. If you are unsure what this means, instructions can be found [here](https://medium.com/@JinnaBalu/initialize-local-git-repository-push-to-the-remote-repository-787f83ff999) and [here](https://www.theserverside.com/video/How-to-create-a-local-repository-with-the-git-init-command).

1. Login to Netlify and click _New Site from Git_, then select _Github_ and then the project in question. Set the command as `npm run build`.

Now when you commit and push to Github, Netlify will deploy the latest version of the project automatically.
