These are example JSONs we expect to receive

##Fairphone

```JSON
{
  "meetups" :
  [
    {
      "eventName" : "The example party",
      "startDate" : "2016-10-13T14:00+02:00",
      "endDate" : "2016-10-13T18:00+02:00",
      "lat_lng" : [48.210033,16.363449],
      "website" : "https://fairphone.com/meetups/The-example-party/12"
    },
    {}  
  ],
  "angels" :
  [
    {
      "cityName" : "Foo City",
      "lat_lng" : [48.210033,16.363449],
      "website" : "https://fairphone.com/angels/foo-city/36"
    },
    {}
  ]
}
```
##T-Mobile
```JSON
{
  "shops" :
  [
    {
      "shopName" : "Example Shop",
      "lat_lng" : [48.210033,16.363449],
      "openingHours" :
      {
        "monday" : "9:15/18:30",
        "tuesday" : "9:15/18:30",
        "wednesday" : "9:15/18:30",
        "thursday" : "9:15/18:30",
        "friday" : "9:15/18:30",
        "saturday" : "9:15/18:30",
        "sunday" : ""
      },
      "website" : "www.t-mobile.at/shops/example_shop",
      "telNr" : "0676 2000"
    },
    {}
  ]
}
