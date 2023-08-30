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

If Weather Integration crashing from time to time (becoming unavailable) you can add automation to reload it when it's happen:  
![1](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/d687d7da-d5b5-4af7-8ff5-0774371498e6)  ![2](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/44de7502-4c62-410d-82bb-c33581406b92)  ![3](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/11229961-bd87-4275-b982-70246c4f654d)  ![4](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/6af4c41d-cc80-44ed-a488-423930e4c514)  ![23](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/cb3b5951-3195-4ac3-9942-54e59a517105)  ![24](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/54af2975-921d-4367-9a9a-9950f4840553)  ![26](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/2a51d17e-524b-4fc2-b0bb-3ebf0961d050)  ![27](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/b7ca8947-9ef4-470a-826f-d52f679ed853)  ![28](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/1ef24a4f-e127-4f34-8638-0e3720bea2eb)  ![29](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/bbd9913e-f7ff-4b3e-8333-2a0cddad9313)  ![30](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/9c60853b-2839-43ba-951d-19fd83d6de63)  ![31](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/e1c2d6f3-d8e4-4c9d-9377-46e0ca74fa0f)  ![32](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/9dafa345-5ce6-411a-ac8d-24571ed24762)  
Check and if everything is right, press "Save":  
![33](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/385c6730-4f20-4bd9-a522-5b2983f32a8d)  ![34](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/42d27b9f-f3ae-4df2-a6b6-a791fe00e616)  
Or you can reload Integration manually:  
![17](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/e6fe2203-59df-491a-8b5a-d94f40d4044b)  ![18](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/a92afcc0-00d7-4123-ab90-2959139d30de)  ![35](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/0cf51384-e922-48d7-8110-ad87c3d3aff4)  ![36](https://github.com/Silergo/Home-Assistant-Lametric-Weather/assets/32046715/eb37d373-6e58-4c04-9a9c-142f5275e7c7)
