# team-globe
Demo for visualizing a remote team (or any collection of items) on a 3D globe

A secondary is to use the console of the browser as the interface and not have to worry about UI components.

## Run
`npm start`

## Add Team Members
Edit index.html, but I'd like to add them in via the console or pass them in via paremeters when loading the globe

Can add a user via the console

## Usage
Use keyboard commands to cycle between members of the team and fly to their location

`help()` from Browser console will display the following information as well

Before using this viewer, please create a collection of items to visualize of form:

`[{ "name": "alice", "lat": 30, "long" : -30, "image": ".placeholder.png" }] `

The addPeople command will add the above data structure to the map like so:
`addPeople([{ "name": "alice", "lat": 30, "long" : -30, "image": ".placeholder.png" }])`

The format for an individual person is:
{
    "name": "Name of Person - not used",
    "lat": "latitude in degrees",
    "long": "longitued in degress",
    "image": "an image from the local filesystem to display, no remote origins allowed"
}

Functional Commands:
addPeople(arrayOfPeople) - adds an array of people
next() - flies camera to the next item in the collection
prev() - flies camera to previous item in the collection
home() - flies camera back out to the world view
reset() - returns the visualizaiton to the default state

Keyboard Commands: (with web UI in focus)
Left Arrow Key - next()
Right Arrow Key - prev()
Up - home()



## notes
Sort team before adding to UI using the browser console
`team.sort((a,b) => b.lat - a.lat) //sorts team from north to south (in northern hemisphere)`
Or
`team.sort((a,b) => b.long - a.long) //sorts team from east to west`

