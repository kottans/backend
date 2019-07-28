[![MIT Licensed][icon-mit]][license]
[![Awesome][icon-awesome]][awesome]
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

# Weather APP  
__Create CLI-program to read  weather forecast in your terminal.__  
As a user, I can provide location (city name) and required forecast period (accepted values: week forecast or day forecast) and see weather forecast in my terminal. If the city I have provided is not found, the program prints corresponding message and exits.
All cities I have entered will be stored permanently to file. If I start the program without providing any location, last successful query will be repeated.

Use Openweather API for requests https://openweathermap.org/api.

City and forecast range should be provided as command-line arguments:  
`l` for "location": enter city name. Optional. Default value - last successful location name followed by successful query.  
`r` for "range": supported values: “week” and “day”. Optional. Default value “day"

When called without arguments, the app gets weather for successful location. If no location was chosen, textual message “Please enter the location” will be printed.

Example:

```bash
my-weather-app --l=London --r=week
```
This request will show weather forecast for next week in London

```bash
my-weather-app r=week
```
This request triggers prompt “please enter location”

```bash
my-weather-app --l=foobar --r=week
```
This request for non-existing location will trigger the program to print “nothing found. Please enter a different location” and exit.

The design of weather forecast display is up to you. As minimal requirement please print temperature. You can also use ASCII code and other means to make beautiful messages.

⤴️ Back to [Contents](../contents.md)

[icon-chat]: https://img.shields.io/badge/chat-on%20telegram-blue.svg
[icon-mit]: https://img.shields.io/badge/license-MIT-blue.svg
[icon-awesome]: https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg
[license]: https://github.com/Kottans/web/blob/master/LICENSE.md
[awesome]: https://github.com/sindresorhus/awesome
