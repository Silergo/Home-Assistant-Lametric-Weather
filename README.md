# Home-Assistant-Lametric-Weather
Home Assistant Lametric Weather Manual.
### Requirments:
  1. [Home Assistant server](https://www.home-assistant.io/installation/) (HA).
  2. Any DDNS (Dynamic DNS) for your Home Assistant server ([Dynu](https://www.dynu.com/), [Duckdns](https://www.duckdns.org/), [NoIp](https://www.noip.com/), etc).
### Installation:
  
  Basicly, you only need Home Assistant server with any Weather Integration that supported. By default Home Assistant have preinstalled Weather Integration from [Met.no](https://www.met.no/). Also supported OpenWeatherMap, AccuWeather, Gismeteo and Yandex. For Yandex and Gismeteo you need to install [HACS](https://hacs.xyz/) (biggest community store with custom integrations).   

  In Lametric app you need to enter two strings:  
  1. **Home Assistant URL**

Thats where you need DDNS. If you server behind reverse proxy don't forget to add in `configuration.yaml`: 
<pre><code>http:
  use_x_forwarded_for: true
  trusted_proxies:
    - my_reverse_poxy_ip
</code></pre>
**Important note: In Lametric app you should NOT put "/" at the end of URL. For example, if you have DDNS `http://example.duckdns.org` from duckdns, you "Home Assistant URL" should looks like: `http://example.duckdns.org` AND NOT `http://example.duckdns.org/`**
  
  2. **Home Assistant token**

To get your token, go to profile in Home Assistant server, scroll to the bottom and click on "Create Token":

![5](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/92712442-4dd7-4e32-871e-11a6cd9371c1) ![6](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/1579961c-1f61-41dc-8304-d3306638d3ae)  
Copy and paste it to the appropriate line in Lametric app.
#### And thats all!

