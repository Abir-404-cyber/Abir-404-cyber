<!DOCTYPE html>
<html>
  <head>
    <title>Digital Clock</title>
    <style>
      /* style the clock display */
      #clock {
        font-size: 3em;
        font-weight: bold;
        text-align: center;
      }
    </style>
  </head>
  <body>
    <div id="clock"></div>

    <script>
      // function to update the clock display
      function updateClock() {
        var now = new Date();
        var hours = now.getHours();
        var minutes = now.getMinutes();
        var seconds = now.getSeconds();
        var timeString = hours.toString().padStart(2, '0') + ':' + 
                         minutes.toString().padStart(2, '0') + ':' + 
                         seconds.toString().padStart(2, '0');
        document.getElementById('clock').innerHTML = timeString;
      }

      // call the updateClock function every second
      setInterval(updateClock, 1000);
    </script>
  </body>
</html>
