# youtubedl-java [![Build Status](https://travis-ci.org/sapher/youtubedl-java.svg?branch=master)](https://travis-ci.org/sapher/youtubedl-java)

A simple java wrapper for [youtube-dl](https://github.com/rg3/youtube-dl) executable

There's a lot of thing left to do. Parsing output is one of them. Too bad, youtube-dl output unform

# Prerequisite

Youtube-dl should be installed and available.

# Usage

## Installation

You can use jitpack.io to add the library to your project.

[youtube-dl](https://jitpack.io/#sapher/youtubedl-java)

## Make request

```java
// Video url to download
String videoUrl = "https://www.youtube.com/watch?v=dQw4w9WgXcQ";

// Destination directory
String directory = System.getProperty("user.home");

// Build request
YoutubeDLRequest request = new YoutubeDLRequest(videoUrl, directory);
request.setOption("ignore-errors");		// --ignore-errors
request.setOption("output", "%(id)s");	// --output "%(id)s"
request.setOption("retries", 10);		// --retries 10

// Make request and return response
YoutubeDLResponse response = YoutubeDL.execute(request);

// Response
String stdOut = response.getOut(); // Executable output
```
# Links
* [Youtube-dl documentation](https://github.com/sapher/youtubedl-java)
