A simple real-time location-tracking project built using Leaflet, Browser Geolocation API, and Socket.io.
Each connected user shares their live coordinates, and the map updates instantly with their marker.

Approach
1. Checking for Geolocation Support
The first step was verifying whether the user’s browser supports geolocation

2. Using High-Accuracy Location Settings
 { enableHighAccuracy: true, timeout: 5000, maximumAge: 0 }

3. Initializing the Map
I created the main map using Leaflet and centered it at (0, 0)
Then I added OpenStreetMap tiles

4. Managing All User Markers
To keep track of each connected user, I maintained a markers object

5. Clearing Markers on Disconnect
When a user disconnects, the backend notifies all clients with that user’s ID.
I simply removed their marker from the map



Installation & Setup (How You Can Run It)

Follow these steps to run the project locally:

1. Clone the repo
git clone <your-repo-link>
cd <your-project-folder>

2. Install dependencies
npm install

3. Start the backend server
node server.js

This starts the Socket.io backend on default port 3000.

4. Serve the frontend

If you're using a simple index.html, you can serve it using:

npm install -g serve
serve .

Or open the HTML file directly in the browser
(but some geolocation features need HTTPS or localhost).

5. Open the App

Visit:
http://localhost:3000

Open the app on multiple tabs or devices to see real-time location tracking.

