# Home-Assistant-Lametric-Weather
Home Assistant Lametric Weather Manual.
### Requirments:
  1. [Home Assistant server](https://www.home-assistant.io/installation/) reachable from the internet.
  2. *Optional: any DDNS (Dynamic DNS) for your Home Assistant server ([Dynu](https://www.dynu.com/), [Duckdns](https://www.duckdns.org/), [NoIp](https://www.noip.com/), etc).*
### Installation:
  
  Basicly, you only need Home Assistant server with any Weather Integration that supported. By default Home Assistant have preinstalled [Weather Integration](https://www.home-assistant.io/integrations/met) from [Met.no](https://www.met.no/). Also supported [OpenWeatherMap](https://www.home-assistant.io/integrations/openweathermap), [AccuWeather](https://www.home-assistant.io/integrations/accuweather), [Tomorrow.io](https://www.home-assistant.io/integrations/tomorrowio), [SMHI](https://www.home-assistant.io/integrations/smhi), [Gismeteo](https://github.com/Limych/ha-gismeteo), [Yandex](https://github.com/IATkachenko/HA-YandexWeather), [Pirate Weather](https://github.com/alexander0042/pirate-weather-ha) and [Weatherbit](https://github.com/briis/weatherbit). For Yandex, Gismeteo, Pirate Weather and Weatherbit you need to install [HACS](https://hacs.xyz/) (biggest community store with custom integrations).  
  
  #### *Make sure that the entity ID's of Weather Integrations match the appropriate ID's from the list below:*    
  &nbsp;&nbsp;&nbsp;> - **Meteorologisk institutt (Met.no):** weather.forecast_home_assistant
  &nbsp;&nbsp;&nbsp;> - **OpenWeatherMap:** weather.openweathermap
  &nbsp;> - **AccuWeather:** weather.home_assistant
  &nbsp;> - **Tomorrow.io:** weather.tomorrow_io_home_assistant_daily
  &nbsp;> - **SMHI:** weather.smhi_weather
  &nbsp;> - **Yandex:** weather.yandex_weather
  &nbsp;> - **Gismeteo:** weather.gismeteo
  &nbsp;> - **Pirate Weather:** weather.pirateweather
  &nbsp;> - **Weatherbit:** weather.weatherbit 
  
  **To find and edit that ID's look into the Weather Integration settings. For example:**  
  ![17](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/f4b1ee45-5a6e-489d-92ba-88e69f5e2a52) ![18](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/5e24b3d2-573a-4a55-ad6a-01b9d01a0823) ![40](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/7e72cbae-785a-4679-842d-912cab10d26a) ![41](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/dbf45f71-4fdc-4db6-b5f6-704900f9321b) ![42](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/b12eda8d-83cc-4fa1-a13a-ed357c8dffcb) ![43](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/3db6dcc2-72f0-4985-a503-d50d1fb3d896)  
  
  *"Precipitation Warning" option shows alert about approaching rain or snow. Lametric takes closest forecast from chosen Weather Integration and if its any kind of rain or snow, it will show the message in selected language (English, French, German, Japanese, Ukrainian, Spanish or Russian). In AccuWeather you must enable forecast in options, but this will sacrifice 40 minutes of data refreshment rate:*  
  ![17](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/f0d0008e-42fd-4d63-ad41-8deea56ab614) ![18](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/596f0ad8-ab5b-4108-a280-c00869d1b55c) ![37](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/018d0f93-8b92-4d11-b56f-58a40aef11d1) ![38](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/799fdecf-3ef9-4d00-b572-a471e4231c26) ![39](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/4a7e0b5d-6e85-4d90-8ab4-8a574aaef6b4)


  In Lametric app you need to enter two strings:  
  1. **Home Assistant URL**

Thats where you need DDNS. ***But instead of that, you can just forward port of your Home Assistant server (default port is 8123) in router settings. In that case "Home Assistant URL" will be an external IP of you router, including port. Although, this way is not very safety.*** If you server behind reverse proxy, don't forget to add in `configuration.yaml`: 
<pre><code>http:
  use_x_forwarded_for: true
  trusted_proxies:
    - my_reverse_proxy_ip
</code></pre>
Replace "my_reverse_proxy_ip" with ip of you reverse proxy server.    
**Important note: In the Lametric app you should NOT put "/" at the end of URL. For example, if you have DDNS `http://example.duckdns.org`, you "Home Assistant URL" should looks like: `http://example.duckdns.org` AND NOT `http://example.duckdns.org/`**
  
  2. **Home Assistant token**

To get your token, go to the profile in Home Assistant server, scroll to the very bottom and click on "Create Token":

![5](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/f9f70943-6a18-49a6-93eb-d380981756a6)  ![6](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/8d63daf5-25ca-4761-9dd6-d25fa157efa4)  
Copy and paste it to the appropriate line in the Lametric app.
#### And thats all!

### Tips:
If you want to change celcius to fahrenheit, or pressure and wind speed units, you can do it in weather integration settings. For example:  
![17](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/71de1c27-ca16-4dd6-9e01-865239ef05d8)  ![18](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/00ed7182-3808-4799-9f32-8cad3903e4e4)  ![19](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/7af35af8-f30a-4784-9101-b4ea5956b6a0)  ![20](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/be6f74e4-60ec-49c8-9eab-5bf85d2ae761)  ![21](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/ca7ec3a5-136c-41c1-b8f5-468deba491b7)  ![22](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/c4a6992c-0cec-47bc-b373-c9eaac92b05a)  
If Weather Integration crashing from time to time (becoming unavailable) you can add automation to reload it when it's happen:  
![1](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/0529f5ce-bda9-4ab4-9181-15f1831b7a62)  ![2](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/e84e6d1c-d0c8-4346-a95c-a7e2912047d6)  ![3](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/cf89f024-7bf8-4137-829e-d5ab268a1bc5)  ![4](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/e0aa2816-d8fa-406c-b5df-2d26261d3d1f)  ![23](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/9629fe41-5021-4d4e-894a-9b9295acca4f)  ![24](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/0dfa909a-8c1d-4040-841a-6974a056b68d)  ![26](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/ad55d1a6-49f1-474f-95f8-1aa9db544aad)  ![27](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/5e9fd185-95d5-48f3-8f5a-35b5561f57a7)  ![28](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/9fae819a-c8b9-4ef5-b870-88a91496c050)  ![29](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/e61af8c9-e42e-4071-bff2-42c30761e762)  ![30](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/f53b39e5-6a52-4489-9a78-6054ff67fb16)  ![31](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/de5180f0-cd19-4a96-8dd0-7a3383934f69)  ![32](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/873ac0fd-de6b-412d-86fa-74976acfb9fd)  
Check and if everything is right, press "Save":  
![33](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/f6f74f9a-3d00-46d8-85e0-84301361e323)  ![34](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/86e4086b-cb1d-4de9-b319-0e094cf737e2)  
Or you can reload Integration manually:  
![17](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/8dd5be2a-2fa1-4d2f-af01-fcf01c4c45ae)  ![18](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/502fcdc5-edd6-4458-b06c-385c948adc86)  ![35](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/0663eb83-7344-4ec6-9dfd-68b4dbe6ff89)  ![36](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/894b933a-8ee1-4e33-b9b3-4f39b7f3f689)
