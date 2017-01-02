# homebridge-pilight-somfy-blinds

`homebridge-pilight-somfy-blinds` is a plugin for Homebridge.

Control your `pilight-somfy`-based blinds via Homebridge!

## Installation

If you are new to Homebridge, please first read the Homebridge [documentation](https://www.npmjs.com/package/homebridge).
If you are running on a Raspberry, you will find a tutorial in the [homebridge-punt Wiki](https://github.com/cflurin/homebridge-punt/wiki/Running-Homebridge-on-a-Raspberry-Pi).

Install homebridge:
```sh
sudo npm install -g homebridge
```
Install homebridge-pilight-somfy-blinds:
```sh
sudo npm install -g homebridge-pilight-somfy-blinds
```

## Configuration

Add the accessory in `config.json` in your home directory inside `.homebridge`.

```js
   {
     "accessory": "Pilight-Somfy-Blinds",
     "name": "Blinds",
     "up_url": "http://<your_ip>/api.htm?ch=<BlindUpChNumber>&cmd=7",
     "down_url": "http://<your_ip>/api.htm?ch=<BlindDownChNumber>&cmd=7",
     "stop_url": "http://<your_ip>/api.htm?ch=<BlindStopChNumber>&cmd=7",
     "http_method": "PUT",
     "motion_time": "<time which your blind needs to move from up to down (in milliseconds)>"
    }
```

You can omit `http_method`, it defaults to `POST`.

## Note
This plugin based on [homebridge-noolite-http-blinds](https://www.npmjs.com/package/homebridge-noolite-http-blinds) which is based on [homebridge-blinds](https://www.npmjs.com/package/homebridge-blinds).

Feel free to contribute to make this a better plugin!
