# Home-Assistant-Lametric-Weather
Home Assistant Lametric Weather Manual.
### Requirments:
  1. [Home Assistant server](https://www.home-assistant.io/installation/) (HA).
  2. Any DDNS (Dynamic DNS) for your Home Assistant server ([Dynu](https://www.dynu.com/), [Duckdns](https://www.duckdns.org/), [NoIp](https://www.noip.com/), etc).
### Installation:
  
  Basicly, you only need Home Assistant server with any Weather Integration that supported. By default Home Assistant have preinstalled Weather Integration from [Met.no](https://www.met.no/). Also supported OpenWeatherMap, AccuWeather, Gismeteo and Yandex. For Yandex and Gismeteo you need to install [HACS](https://hacs.xyz/) (biggest community store with custom integrations).   

  In Lametric app you need to enter two strings:  
  1. **Home Assistant URL**

Thats where you need DDNS. If you server behind reverse proxy, don't forget to add in `configuration.yaml`: 
<pre><code>http:
  use_x_forwarded_for: true
  trusted_proxies:
    - my_reverse_poxy_ip
</code></pre>
Replace "my_reverse_proxy_ip" to the ip of you reverse proxy server.  
*You can also just forward port of your Home Assistant server (default is 8123) instead of DDNS, but it's not very safety. In that case "Home Assistant URL" is an external IP of you router, including port.*  
**Important note: In Lametric app you should NOT put "/" at the end of URL. For example, if you have DDNS `http://example.duckdns.org`, you "Home Assistant URL" should looks like: `http://example.duckdns.org` AND NOT `http://example.duckdns.org/`**
  
  2. **Home Assistant token**

To get your token, go to the profile in Home Assistant server, scroll to the very bottom and click on "Create Token":

![5](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/92712442-4dd7-4e32-871e-11a6cd9371c1) ![6](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/1579961c-1f61-41dc-8304-d3306638d3ae)  
Copy and paste it to the appropriate line in the Lametric app.
#### And thats all!

### Tips:
If you want to change celcius to fahrenheit, or pressure and wind speed units, you can do it in weather integration settings. For exampe:  
![17](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/d0b97cd4-3a04-46b2-a426-39807d69d4c7)  ![18](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/e59c9943-5678-4e68-bc16-086bba5de79c)  ![19](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/15c07b4b-d33c-408d-ab43-07af38b88d34)  ![20](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/140bc011-2d1c-4659-9c66-f79efd68cbad)  ![21](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/e9131eb4-13f5-4f76-864f-4ed13dbb206f)  ![22](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/c9089a74-6463-4bf5-ab89-d2ca92cfeac9)





