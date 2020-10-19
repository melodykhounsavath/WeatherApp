# WeatherApp
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>WeatherSearch</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css"
        integrity="sha384-JcKb8q3iqJ61gNV9KGb8thSsNjpSL0n8PARn9HuZOnIxN0hoP+VmmDGMN5t9UJ0Z" crossorigin="anonymous" />
    <script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>
    <style>
        h1 {
            font-size: 24px;
            font-weight: 100;
            margin: 0;
            line-height: 28px;
        }

        ul {
            margin: 0 0 10px;
            padding: 0;
        }

        li {
            font-size: 16px;
            font-weight: 100;
            list-style: none;
            line-height: 1;
            height: 20px;
        }

        .weather-search {
            border: 1px solid;
            padding: 20px;
            margin: 25px auto;
            border-radius: 15px;
            max-width: 600px;
        }

        .cloud {
            height: 54px;
            margin-right: 10px;
        }

        .temp {
            font-size: 64px;
            font-weight: 400;
            line-height: 1;
        }

        .units {
            position: relative;
        }

        .search-form {
            margin-bottom: 20px;
        }
    </style>

</head>

<body>
    <div class="container">
        <div class="weather-search">
            <form class="search-form" id="search-form">
                <div class="row">
                    <div class="col-6">
                        <div>
                            <input type="search" class="form-control" placeholder="Type a city..." id="search-input" />
                        </div>
                    </div>
                    <div class="col-3">
                        <input type="submit" value="Search" class="form-control btn btn-primary shadow-sm" />
                    </div>
                    <div class="col-3">
                        <button type="button" class="btn btn-success w-100"
                            id="current-location-button">Current</button>
                    </div>
                </div>
            </form>
            <h1 id="city"></h1>
            <ul>
                <li id="display"></li>
                <li id="forcast"></li>
            </ul>
            <div class="row">
                <div class="col-6">
                    <div class="cloud">
                        <div class="float-left">
                            <span class="temperature"></span>
                            <span class="units">°C|°F </span>
                        </div>
                    </div>
                </div>
                <div class="col-6">
                    <ul>
                        <li>Humidity: <span id="humidity"></span>%</li>
                        <li>Wind: <span id="wind"></span>km/h</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
    </div>

    <script src="src/index.js"></script>
</body>

</html>
