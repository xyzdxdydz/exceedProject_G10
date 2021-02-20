# exceedProject_G10

## BACKEND
In the backend part, we use the Flask framework to manage the Raspberry pi based server. the server gets a response from hardware(esp32 microcontroller), it will be calculating water left, time interval, and the usage statistic in a time interval and update data to MongoDB database the frontend will fetching the data through "/popular path" to access to a database and hardware will using GET and POST method to communicate with the server through "/water" path.
