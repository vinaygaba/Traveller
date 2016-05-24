# Traveller :airplane: :helicopter: :rocket: :bike: :car: :truck: :bus:

![Feature Image](images/FeatureImage.gif)

Add a map on your site with every place that you have visited! [Demo](http://www.vinaygaba.com/traveller/demo.html)

---

Introduction
-----

My motivation behind creating Traveller was to create a map for my website that showcases the places that I have visited. I soon realized that there might be more people(developers) who would want to have a similar page on their site so I decided to put this up on Github.

As of now, it is a simple html page but going forward, I will be working on converting this into a React component so that it can be easily added to any web app.

I will try to be as elaborate as possible in giving instructions about how one might customize it to suit their needs.


Usage
------

The page parses a JSON file in order to know which points need to be populated on the map. The format of the JSON string needs to be as follows:

```JSON
[
  {
    "name":"Name of place",
    "lat":"Latitude",
    "lon":"Longitude",
    "purpose":"lived/travelled"
  },
  {
    "name":"Name of place",
    "lat":"Latitude",
    "lon":"Longitude",
    "purpose":"lived/travelled"
  },
  .
  .
  .
]
```
Right now I use two different markers to represent whether you lived in a city or were just travelling. If you do not like this, it would be pretty simple to remove this by making changes in the styles.css file. More about this in the Customizations section.

Example JSON files can be found in [data](data/) folder.
You can either save the JSON file in the same server or host the json file on a service like [myjson](http://myjson.com)

To specify which JSON file to use, find the ```$.getJSON(pathToJSONFile,function(..))``` method call in the html page and replace the jsonPath with the path to your JSON file.

And this is it! This is the only step that is required in order to see the populated world map that you see in the above screenshot.

<b>Note</b>: I understand that manually adding the locations can be a pain in the butt, especially for people who have travelled a lot. This will change soon as I am exploring alternate ways to do this(Facebook/Foursquare Checkins). I am also open to suggestions from you guys so feel free to use the Issues tracker to give me feedback.
