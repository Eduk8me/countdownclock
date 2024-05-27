# Eduk8me Countdown Clock

This was written with the help of ChatGPT to bring in a countdown clock into [OBS](https://obsproject.com/) as a browser source. We were using a local script that wrote to a text file, but that wasn't very portable. The Eduk8me Countdown clock is a one web app written in html with Javascript that can run anywhere (even locally) or from [Eduk8.me](https://eduk8.me/countdown.html).

When using it in OBS, a good starting size for the browser source is 1920x300. The size can be adjusted as necessary to fit.

# Usage

The page requires one parameter, and that is the end date and time. This is passed as a url argument to the web page in the format of YYYY-mm-ddTGHH:MM. For example, to countdown to Christmas, the address would look like:

    https://eduk8.me/countdown.html?datetime=2024-12-25T00:00

By default it will show the countdown in hours, minutes, and seconds. For example, this event will happen in 23 hours, ten minutes, and 23 seconds:

    23:10:23

Passing `format=long` would render the above as:

    23 hours, 10 minutes, 23 seconds

The URL would look like this:

    https://eduk8.me/countdown.html?datetime=2024-12-25T00:00&format=long

# Additional parameters

* `time=include` - Show the end date and time
* `color=red` - Show the clock in red. You can use color names, hex code (use `%23` in place of #) or rgb values
* `msg=This is a message` - Show a message with the clock. The message should be coded in the url, but I've found that it works well enough just typing it out. You're mileage may vary

