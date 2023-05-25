# csgo-event-server
A ready-to-use event server for Counter-Strike: Global Offensive Game State Integration.

`csgo-event-server` automates the injection of a Game State Integration configuration file into your CS:GO installation and provides an event stream to hook into (e.g. using the `EventSource` class in JavaScript). 

> **Note:** The example UI currently ignores map, weapon, and team-related events—while the example configuration file does not request any spectator-only events.

## How to Use
Run `npm install` to install all project dependencies. 

Run `npm start` to inject the configuration file and start the server.

After the server is started, Ctrl-Click on the printed URL to view the included example interface.

Now, after opening CS:GO, you should see the header information populate with the game title and your Steam ID.

The rest of the UI will populate when you have joined a match.

## Development
The name of your configuration file is determined by the `name` specified in your `package.json`.
> **Note:** You may override this by specifying an `APP_NAME` property in an `.env` file.

To modify the configuration file associated with your event server, modify the `config.js` file at the base of the repository.

The port used by the server is dynamically selected based on the available ports on your computer. To override this selection, you can specify a `PORT` property in an `.env` file.
