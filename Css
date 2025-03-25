async function getWeather() {
    var apiKey = "a048c289ca1fa07bdae5a130955cbaa9";
    var city = document.getElementById('search').value; // Change to your desired city
    const url = "https://api.openweathermap.org/data/2.5/weather?q="+city+"&appid="+apiKey+"&units=metric";
    document.querySelector(".error").innerHTML="";
    try {
        const response = await fetch(url);
        const data = await response.json();
    document.querySelector(".city-name").innerHTML = (data.name!="undefined")?data.name:"-";
    document.querySelector(".weather-temp").innerHTML = Math.floor(data.main.temp) + '°';
    document.querySelector(".wind").innerHTML = Math.floor(data.wind.speed) + " m/s";
    document.querySelector(".pressure").innerHTML = Math.floor(data.main.pressure) + " hPa";
    document.querySelector('.humidity').innerHTML = Math.floor(data.main.humidity)+ "%";
    document.querySelector(".sunrise").innerHTML =  new Date(data.sys.sunrise * 1000).toLocaleTimeString([], {hour:"2-digit", minute:"2-digit"});
    document.querySelector(".sunset").innerHTML =  new Date(data.sys.sunset * 1000).toLocaleTimeString([], {hour:"2-digit", minute:"2-digit"});

    } catch (Exception) {
        document.querySelector(".error").innerHTML="Unknown Location Please Check.....";
    }
}
getWeather();
