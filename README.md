These are example JSONs we expect to receive from FP servers:

##Meetups

```JSON
{
  "meetups" :
  [
    {
      "eventName" : "The example party",
      "startYear"   : "1970",
      "startMonth": "12",
      "startDay" : "31",
      "startHour" : "16",
      "startMinute" : "16",
      "endYear" : "1971",
      "endMonth" : "1",
      "endDay" : "1",
      "endHour" : "17",
      "endMinute" : "17",
      "lat_lng" : [48.210033,16.363449],
      "website" : "https://fairphone.com/meetups/The-example-party/12"
    },
    {}  
  ],
  "angels" :
  [
    {
      "cityName" : "Foo City",
      "lat_lng" : "[48.210033,16.363449]",
      "website" : "https://fairphone.com/angels/foo-city/36"
    },
    {}
  ]
}
