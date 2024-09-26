# Telemetry Architecture

## Keywords

[#telemetry](https://en.wikipedia.org/wiki/Telemetry) 
[#metadata](https://en.wikipedia.org/wiki/Metadata) 
[#privacy](https://en.wikipedia.org/wiki/Privacy) 
[#folksonomy](https://en.wikipedia.org/wiki/Folksonomy) 
[#semiotics](https://en.wikipedia.org/wiki/Semiotics) 
[#memetics](https://en.wikipedia.org/wiki/Memetics) 
[#mapping](https://en.wikipedia.org/wiki/Mapping)
[#scraping](https://en.wikipedia.org/wiki/Web_scraping)
[#tagging](https://en.wikipedia.org/wiki/Tag_(metadata)) 
[#slowmedia](https://en.wikipedia.org/wiki/Slow_media) 
[#obfuscation](https://en.wikipedia.org/wiki/Obfuscation) 
[#python](https://en.wikipedia.org/wiki/Python_(programming_language)) 
[#houdini](https://en.wikipedia.org/wiki/Houdini_(software)) 

### Instructor
- **Instructor:** Joris Putteneers - putteneersjoris@gmail.com - [website](http://putteneersjoris.xyz) - [github](https://github.com/archiGrad/Bartlett_ws_october_2024)


## workshop description

In this workshop, students will combine scraped data, image metadata and google telemetry data to create analytical drawings of their site thatwill help them formulate a design strategy and proposal.

### 1.1 What is telemetry data?

Telemetry data refers to automatically and remotely transmitted information. Companies like Google and Facebook collect a large volume and scope of user data, which may include:

- Network connectivity (to check who is near you)
- GPS coordinates (to check where you are)
- Vehicle type, speed, direction, etc. (where you are going)
- Temperature, humidity, air quality, light levels (environmental conditions)
- Audio and video calls (what you are talking about)
- Spending patterns (what are your spending habits)
- Click patterns (what you like to do on the internet)
- Ambient audio recording
- Eye tracking patterns (what you like to look at) 
- Heart rate, blood pressure, body temperature, emotional state, sleep patterns (some smartwatches only)

This data creates a full digital fingerprint of a person, which can be used for both good and bad purposes. Governing bodies like the General Data Protection Regulation (GDPR) and Personal Data Protection Act (PDPA) exist to protect users. Many others exist around the world.

Many software applications, including Adobe, Rhino, and operating systems like Windows or macOS, use telemetry systems for feedback, trend analysis, and license management.

Internet of Things (IoT) is an extension of this concept, where devices are constantly connected to the internet. This includes devices such as your smartwatch, Google Home, and even your cell phone.

When used correctly and ethically, with a common consensus, where the code is open-sourced, and with a clear agenda, telemetry data can be an extremely useful tool for data analysis, visualization, and predictions in many professions, including architecture and urban planning.

In this workshop, the service we will utilize to capture this telemetry data is 'Google Takeout'.

### 1.2 What is metadata?

Globally, in 2023, about 400 million terabytes are uploaded, including 5.3 billion images being uploaded every day. That is as many images in a day as the whole year of 2011. Lets assume 1 image is 1mb and that metadata counts for 1%, , that would mean  53,000 GB = 53 TB (terabytes) / day.


- Camera information (make, model)
- Capture settings (date, time, exposure, GPS coordinates)
- Copyright information
- Editing history

Example of image metadata:
```
Image: example_photo.jpg (JPEG, 3024x4032, sRGB)
EXIF: Apple iPhone 12 Pro, iOS 15.1
2023:09:18 14:30:15, 1/120 sec, f/1.6, ISO 100
Focal Length: 4.2mm, Flash: Off
GPS: 40°41'21.91"N, 74°2'40.20"W
Altitude: 10.5m, Speed: 0, Direction: 45.0°
IPTC: © John Doe Photography
Title: Sunset in Central Park
Caption: Beautiful sunset view from Central Park, New York City
Keywords: sunset, park, nature, city, landscape
XMP: Created: 2023-09-18T16:45:30-04:00 (Adobe Photoshop 2023)
Modified: 2023-09-19T09:15:22-04:00, Rating: 4
Color Profile: sRGB IEC61966-2.1 (Display Device Profile)
Photoshop: Document Ancestors: xmp.did:9A8B7C6D5E4F3A2B1C0D9E8F7A6B5C4D
Thumbnail: JPEG, 9012 bytes, 160x120 pixels
```

In this workshop, the most interesting data is the GPS data and timestamp. This GPS data, combined with data from a telemetry service like Google Takeout, can provide interesting insights into not just where or when a photo was taken, but more importantly the circumstances surrounding its capture.

## Workshop Preparation

1. Choose a site in or around London:
   - Site has to be a "project in need" .
2. Ensure your Google Maps Timeline is active:
   - View your timeline in Google Maps. If you can see a route, that means it is successful.
   - If it's not working, watch the provided tutorial.
   - If issues persist, extract a Google Takeout, deselect everything, and only select timeline. Download and verify the timeline semantic history data has .json files like "2024_AUGUST.json" with data inside of it. https://takeout.google.com/
   - Report any additional problems in the chat.
3. Verify that your phone can store images with metadata:
   - Check if you can see the map when scrolling up on your photos.

## Site Visit Instructions

- Turn on your phone's location services and cellular data BEFORE leaving for your site. Your location and cellular data must stay on during your whole trip.
- Take a minimum of:
  - 25 photos of your site (front views, side views, interior, exterior, etc.)
  - 15 photos of the site surroundings (neighboring architecture, waterways, railroads, people, etc.)
  - 10 photos during transportation (multiple modes encouraged and will give more interesting results: bike, boat, foot, on foot, car, etc.)

## Quantity over Quality

With all students participating, a significant amount of data will be produced. More data means:
- Increased Granularity: With more data points, we can increase the resolution and detail of our map.
- Enhanced Resolution: A larger dataset allows us to create a more precise and accurate representation of the information we're mapping.
- Reduced Impact of Anomalies: As the volume of data increases, individual anomalies or outliers will have less influence on the overall results.
- Extraction of Meaningful Information: A larger dataset provides more opportunities to identify patterns and extract meaningful information that might not be apparent with less data.

While the final map will be provided in the following week, students are highly encouraged to show interest and attempt to work with the data themselves.

## Procedures

### Agenda
| Date | Day | Event | London (BST/UTC+1) | Bangkok (ICT/UTC+7) | Hours |
|------|-----|-------|---------------------|---------------------|-------|
| September 30 | Monday | Introduction and presentation, discuss site visit | 10:00 - 13:00 | 16:00 - 19:00 | 3 |
| October 1 | Tuesday | site visit | - | - | 0 |
| October 2 | Wednesday | python basics, loading image data, make groups | 12:00 - 15:00 | 18:00 - 21:00 | 3 |
| October 3 | Thursday | loading telemetry data and google scrape | 09:00 - 12:00, 12:30 - 15:00 | 15:00 - 18:00, 18:30 - 21:00 | 5.5 |
| October 4 | Friday | Free day | - | - | 0 |
| October 5 | Saturday | houdini basics, producing maps and extracing insights | 09:00 - 12:00, 12:30 - 15:00 | 15:00 - 18:00, 18:30 - 21:00 | 5.5 |
| October 6 | Sunday | Free day | - | - | 0 |
| October 7 | Monday | design proposal and working session | 09:00 - 12:00, 12:30 - 15:00 | 15:00 - 18:00, 18:30 - 21:00 | 5.5 |
| October 8 | Tuesday | working session  | 13:00 - 15:00 | 19:00 - 21:00 | 2 |
| October 9 | Wednesday | working session | 12:00 - 15:00 | 18:00 - 21:00 | 3 |
| October 10 | Thursday | working session | 09:00 - 12:00, 12:30 - 15:00 | 15:00 - 18:00, 18:30 - 21:00 | 5.5 |
| October 11 | Friday | Final presentations | 11:00 - 15:00 | 17:00 - 21:00 | 4 |


Note: 30-minute lunch breaks are included for full-day sessions, except on October 2nd, 8th, 9th, and 11th.

### Workshop preparation
- A Google account with location history turned on
- Houdini apprentice 20.5
- Houdini labs tools
- a cellphone with cellular data (android or IOS)

## Additional Notes

- Refer to the [Discord channel](https://discord.com/channels/1288761113718030378/1288761533903671319).
