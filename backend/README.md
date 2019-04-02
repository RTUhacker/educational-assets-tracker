# Display Server

This server simulates the changing location of a set of vehicles given a
[GTFS](https://en.wikipedia.org/wiki/General_Transit_Feed_Specification)
schedule.

## Usage

The server has two dependencies, Google Maps APIs to query predicted travel
times using the [Directions API](https://developers.google.com/maps/documentation/directions/),
and [Firebase Realtime Database](https://firebase.google.com/docs/database/).

To authorize access to the Google Directions API, add a Google Maps API key in the following places:

- At the top of `generate_paths.js`
- At the top of `simulation.js`

Using the process outlined in
[Directions API: Get a Key](https://developers.google.com/maps/documentation/directions/get-api-key).

To authenticate to Firebase, populate the `serviceAccountKey_example.json` file using the
process outlined in
[Firebase Admin SDK setup](https://firebase.google.com/docs/admin/setup).

To configure which Firebase Realtime Database URL to use to communicate with
`display-client`, configure the `databaseURL` at the top of `tracker_configuration_example.js`.

Also in `tracker_configuration_example.js`, configure `mapsApiKey` where you put Maps API key, and `simulation` which determines whether to use the vehicle simulator or real location data from the vehicle locator. While developing and testing, set this value to true.

To install library dependencies, use Node Package Manager.

```bash
npm install
```

To run the server, again use npm.

```bash
npm run main
```
