# exceedProject_G10
The topic is "IOT for new normal" so our group decides to do a water dispenser. this idea based on the "contactless" concept. 

### HARDWARE

### BACKEND
In the backend part, we use the Flask framework to manage the Raspberry pi based server. the server gets a response from hardware(esp32 microcontroller), it will be calculating water left, time interval, and the usage statistics in a time interval and update data to MongoDB database the frontend will fetching the data through "/popular path" to access to a database and hardware will using GET and POST method to communicate with the server through "/water" path.

-to run a server
```shell
python3 app.py 
```
-to run a time reset function
```shell
python3 timeDivider.py
```

### FRONTEND
