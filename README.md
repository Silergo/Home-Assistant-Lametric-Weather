# Home-Assistant-Lametric-Weather
Home Assistant Lametric Weather Manual.
# Requirments
  [Home Assistant server](https://www.home-assistant.io/installation/) **(version 2024.8.0 or higher)** REACHABLE from the internet.
  
# Installation
  
  Basicly, you only need Home Assistant server with any Weather Integration that supported. By default Home Assistant have preinstalled [Weather Integration](https://www.home-assistant.io/integrations/met) from [Met.no](https://www.met.no/). Also supported [OpenWeatherMap](https://www.home-assistant.io/integrations/openweathermap), [AccuWeather](https://www.home-assistant.io/integrations/accuweather), [SMHI](https://www.home-assistant.io/integrations/smhi) (only for Sweden), [Gismeteo](https://github.com/Limych/ha-gismeteo), [Yandex](https://github.com/IATkachenko/HA-YandexWeather), [Pirate Weather](https://github.com/alexander0042/pirate-weather-ha) and [WeatherAPI](https://github.com/iprak/weatherapi). For Yandex, Gismeteo, Pirate Weather and WeatherAPI you need to install [HACS](https://hacs.xyz/) (biggest community store with custom integrations).  
  
***Make sure that the entity ID's of Weather Integrations match the appropriate ID's name from the list below:***   
  > - **Meteorologisk institutt (Met.no):** weather.forecast_home_assistant
  > - **OpenWeatherMap:** weather.openweathermap
  > - **AccuWeather:** weather.home_assistant  
  > - **SMHI:** weather.smhi_weather
  > - **Yandex:** weather.yandex_weather
  > - **Gismeteo:** weather.gismeteo
  > - **Pirate Weather:** weather.pirateweather
  > - **WeatherAPI:** weather.weatherapi_weatherapi
 
  **To find and edit that ID's name, look into the Weather Integration settings. For example:**  
  ![17](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/f4b1ee45-5a6e-489d-92ba-88e69f5e2a52) ![18](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/5e24b3d2-573a-4a55-ad6a-01b9d01a0823) ![40](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/7e72cbae-785a-4679-842d-912cab10d26a) ![41](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/dbf45f71-4fdc-4db6-b5f6-704900f9321b) ![42](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/b12eda8d-83cc-4fa1-a13a-ed357c8dffcb) ![43](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/78888698-7588-402f-90c0-1571fd941409)

<br/>
In the Lametric app you need to enter two strings:
<br/>
<br/>
  
  1. **HA URL**

Enter **IP address with port or domain name of your Home Assistant server**, it should look like this: http://xxx.xxx.xxx.xxx:8123, where xxx.xxx.xxx.xxx - IP address of you Home Assistant server and 8123 - Home Assistant server port. If your Home Assistant server is behind router, then **HA URL** is **external** IP of you router with port, it should look like above: http://xxx.xxx.xxx.xxx:8123, but xxx.xxx.xxx.xxx - **external** IP of you router and 8123 - Home Assistant server port. Don't forget to forward 8123 port to your Home Assistant server in router settings.   
**Important note: In the Lametric app you should NOT put "/" at the end of URL. You "HA URL" should looks like: `http://xxx.xxx.xxx.xxx:8123` AND NOT `http://xxx.xxx.xxx.xxx:8123/`**
  
  2. **HA token**

To get your token, go to the profile in Home Assistant server, choose "Security" tab, scroll to the very bottom and click on "Create Token":

![65](https://github.com/user-attachments/assets/8c1da887-892b-48cc-8bf0-8d042ba52592)  
Copy and paste it to the appropriate line in the Lametric app.
#### And thats all!

# Options in the app
  1. **Weather Integration**: choose weather integration installed on your server.
  2. **Other options**:
  > - "Pressure" - show pressure from chosen integration.
  > - "Humidity" - show humidity from chosen integration.
  > - "Windspeed" - show windspeed from chosen integration.
  > - "Forecast temperature" - show closest temperature from integration forecast.
  3.  **Precipitation Warning**: this option shows alert about approaching rain or snow. Lametric takes closest forecast from chosen Weather Integration and if its any kind of rain or snow, it will show the message in selected language (English, French, German, Japanese, Ukrainian, Spanish or Russian).

*Also, app save **last** value of temperature, state icon and forecast, so if weather integration will become unavailable, you'll still be able to see **your last** weather information, until integration becomes available again.* 

### Tip
If you want to change celcius to fahrenheit, or pressure and wind speed units, you can do it in weather integration settings. For example:  
![17](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/71de1c27-ca16-4dd6-9e01-865239ef05d8)  ![18](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/00ed7182-3808-4799-9f32-8cad3903e4e4)  ![19](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/7af35af8-f30a-4784-9101-b4ea5956b6a0)  ![20](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/be6f74e4-60ec-49c8-9eab-5bf85d2ae761)  ![21](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/ca7ec3a5-136c-41c1-b8f5-468deba491b7)  ![22](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/c4a6992c-0cec-47bc-b373-c9eaac92b05a)
