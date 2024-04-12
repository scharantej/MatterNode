### I want to build an app for controlling Smart Home devices, specifically SmokeCo matter devices. How should I structure my Flask app?

**HTML Files:**

- **index.html**: This will be the main page of your application. It will display a list of connected devices and allow users to interact with them (e.g., turn on/off lights, adjust thermostat settings, monitor sensors).
- **device_detail.html**: When a user selects a device from the list, this page will show detailed information about the device, such as its status, configuration options, and historical data.

### Routes:

- **Home Route (root)** `/`: Renders the `index.html` page.
- **Device List Route** `/devices`: Retrieves a list of connected Smart Home devices and returns it as JSON. This route will be called when the `index.html` page loads to populate the list of devices.
- **Device Detail Route** `/device/<device_id>`: Retrieves detailed information about a specific device and returns it as JSON. This route will be called when a user clicks on a device from the list in `index.html` to open the `device_detail.html` page.
- **Control Device Route** `/device/<device_id>/<action>`: Allows the user to perform actions on devices, such as turning on/off lights, adjusting thermostat settings, or locking/unlocking doors. The specific action will be specified in the `action` parameter, and the route will update the device's state accordingly.
- **Configuration Route** `/device/<device_id>/configure`: Allows the user to configure settings for the device, such as setting schedules, customizing notifications, or changing device preferences.
- **History Route** `/device/<device_id>/history`: Retrieves historical data for a device, such as temperature readings, motion events, or energy consumption.