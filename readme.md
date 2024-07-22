# Earthquake Alert App

## Project Description

This project was developed for the NASA Space Apps Challenge. Our team created an innovative application that alerts, notifies, and provides checklists for users in the event of a nearby disaster. The app features a pop-up map showing the safest route to the nearest open location during an earthquake.

## Features

- Real-time disaster alerts and notifications
- Safety checklists and guidelines
- Pop-up map with the safest route to the nearest open location
- User-friendly interface and intuitive design

## Technologies Used

- **Languages:** PHP, HTML, CSS, JavaScript
- **APIs:** USGS API, Google Maps API
- **Platforms:** Android (Android Studio)

## Installation

### Prerequisites

- Android device with developer options enabled
- [Android Studio](https://developer.android.com/studio) installed
- Web server with PHP support

### Steps

1. Clone the repository:
    ```bash
    git clone https://github.com/kalyan1998/nasa_spaceapps.git
    cd nasa_spaceapps
    ```

2. Set up your web server to serve the PHP files in the repository:
    - Ensure your server is running and configured correctly.
    - Place the PHP files in the server's root directory or an accessible subdirectory.

3. Open the Android project in Android Studio:
    ```bash
    cd android
    open -a "Android Studio" .
    ```

4. Build and run the Android app on your device.

## Using PHP Backend with Mobile App

The PHP backend acts as a server-side component that processes requests from the mobile app. Here’s how it works:

1. **Data Retrieval**: The PHP scripts interact with various APIs (e.g., USGS for earthquake data) to fetch real-time information.
2. **Data Processing**: The backend processes the data and performs necessary calculations or transformations.
3. **API Endpoints**: The mobile app communicates with the PHP backend through API endpoints. These endpoints provide data such as alerts, safety checklists, and routing information.
4. **Response Handling**: The app sends HTTP requests to the backend, which responds with JSON data. The app then parses this data to update the UI accordingly.

### Example API Call

Here's a basic example of how the app might request data from the PHP backend:

```javascript
fetch('https://your-server-url/endpoint.php')
  .then(response => response.json())
  .then(data => {
    // Process the received data and update the app's UI
  })
  .catch(error => {
    console.error('Error fetching data:', error);
  });
