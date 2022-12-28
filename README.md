<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Weather App</title>
    <style>
        h1,
        h2,
        h3 {
            text-align: center;
        font-family: Arial, Helvetica, sans-serif;
        }
      h1 {
        color: #1a64d6;
        font-size: 34px;
        font-weight: 900;
        padding-bottom: 0px;
        margin-bottom: 5px;
        line-height: 48px;
        
      }
      h2 {
        font-size: 34px;
        margin: 0;
        line-height: 48px;
        font-weight: 400;
      }
      ul {
        padding: 0;
      }
      li {
        list-style: none;
        text-align: center;
        padding: 10px 0;
        border-radius: 10px;
        transition: all 200ms ease-in-out;
        max-width: 400px;
        margin: 0;
      }
      li:hover {
        background: #fffbef;
      }
      p {
        font-size: 18px;
        opacity: 0.7;
        text-align: center;
        font-family: monospace;
      }
      .degrees {
        font-weight: normal;
      }
      button {
        color: #fff;
        background-color: white;
        display: block;
        margin: 20px auto;
        background: #1a64d6;
        padding: 15px 20px;
        line-height: 22px;
        font-size: 16px;
        padding: 16px 24px;
        transition: all 200ms ease;
        box-shadow: rgba(red, green, blue, alpha) 0px 8px 8px 0;
        cursor: pointer;
        border-radius: 30px;
        border: 1px solid #1a64d6;
      }
      button:hover {
        background: white;
        color: #1a64d6;
        border: 1px solid #1a64d6;
        cursor: pointer;
      }
      p {
        font-size: 18px;
        font-family: "Courier New", Courier, monospace;
      }
    </style>
    <meta />
  </head>
  <body>
    <center>
      <h1>
        🌥️
        <br />
        <strong> Currently 21° in Tokyo </strong>
      </h1>
      <h2>
        <span class="degrees"> 13° / </span>
        <strong>23°</strong>
      </h2>
      <ul>
        <li>
          <h3>🌧️Tomorrow</h3>
          <p>
            10° /
            <strong>22°</strong>
          </p>
        </li>
        <li>
          <h3>🌥️Saturday</h3>
          <p>
            15° /
            <strong>17°</strong>
          </p>
        </li>
        <li>
          <h3>☀️ Sunday</h3>
          <p>
            25° /
            <strong>28°</strong>
          </p>
        </li>
      </ul>
      <button>Change city</button>
      <p>Coded by Denise Stephens</p>
    </center>

     <script>
       function changeCity() {
        let city = prompt("What city do you live in?");
        let temperature = prompt("What temperature is it?");
        let heading = document.querySelector("h1");
        if (temperature < 0) {
          heading.innerHTML =
            "☹️<br />Currently " + temperature + "°C in " + city;
        } else {
          heading.innerHTML =
            "😄<br />Currently " + temperature + "°C in " + city;
        }
      }

      let changeButton = document.querySelector("button");
      changeButton.addEventListener("click", changeCity);
    </script>
  </body>
</html>
