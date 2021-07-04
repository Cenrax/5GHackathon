




### Clothing Mode

Command to enable: ```Start clothing mode```

In this mode, the app detects different types of clothes, colors, and patterns in order to help users making better clothing choices. Users just need to point to clothes and tap anywhere on the screen and the app will then speak out loud the detection.

### Navigation/Walking Mode

Command to enable: ```Start walking mode```

Walking Mode can help users navigate safely by monitoring moving cars.

### Shopping Mode

Command to enable: ```Start shopping mode```

Shopping Mode helps users finding and buying things. Users just need to say **where's (object name)** and the app will monitor in real-time until the object is found.

### Objects Mode

Command to enable: ```Start objects mode```

Objects Mode helps users finding objects. Users just need to say **where's (object name)** and the app will monitor in real-time until the object is found.

### Labels Mode

Command to enable: ```Start labels mode```

Labels Mode helps users choose the right product for them. Users just need to point the camera to the product, tap anywhere on the screen, and then the app says the most relevant info from the product (names, nouns, brands, adjectives)


### Menu Mode

Command to enable: ```Start menu mode```

Menu Mode helps users reading menus to help them decide what to eat. Users just need to point the camera to the menu, tap anywhere on the screen, and then the app says the menu items with their prices. Users can tap again at any moment to interrupt the speaking.

### Numbers Mode

Command to enable: ```Start numbers mode```

Numbers Mode helps users reading numbers (especially phone numbers)

### Explore Mode

Command to enable: ```Start explore mode```

Explore Mode helps users exploring and understanding the world around them. They can imagine what’s around from the description and better enjoy going out.

When the user needs to stop current mode s/he just needs to say: ```stop``` or ```exit```.





### Socket.IO Audio

The audio from the app is streamed to the Socket.IO server (```Node.JS```) for continuous real-time speech-to-text recognition.

The server uses Voice Activity Detection (VAD) to detect when the user started saying something and when s/he has stopped speaking. The chunks of audio are then streamed continuously to DeepSpeech model (```TensorFlow```), which is a model based on Baidu's Deep Speech research paper. When the user has finished speaking, the detection is then finished and the result is processed to detect which actions should be performed. The detected actions are then returned to the app.

### Socket.IO Video

The video from the app is streamed to the Socket.IO server (```Node.JS```) for continuous real-time image recognition.

This server acts as an API gateway by receiving an incoming image with the current mode and then routing the image for processing in the mode-specific APIs, which are described next.


### Mobile App

The app is a Progressive Web App, which allows the app to be developed in HTML5 and Javascript, but can be added to the users' home Screen (Available from Safari iOS). The audio is synthesized using Text-to-Speech API available in iOS Webkit Javascript API. Video and audio are also capture using APIs available on iOS Webkit Javascript API.

### Audio Flow

### Video/Image Flow

