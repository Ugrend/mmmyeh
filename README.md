# osu Web Replays

osu! Web Replays is a tool to allow to watch [osu!](http://osu.ppy.sh/) replays in your browser.

## Getting Started

The website can be accessed [here](https://ugrend.github.io/osuwebreplay).

By default it has no access to any assets/beatmaps/etc.
Replays/Beatmaps/Skins can be loaded by dragging the .osr/.osz/.osk archives into the browser.  
If you load a replay that you do not have the beatmap available locally it will attempt to download a copy of the map, however no assets will be provided (eg no song)

You can also drag in asset files separately (eg: if you drag in a .mp3 for a map the song will now load for that map automatically)

__Disclaimer:__ Any map(excluding assets)/replay you drag in gets automatically uploaded to an API, so if you have something top secret I would suggest not draging it in ;)  

#### Skins:
I would highly suggest using a custom skin package as the default is not great and unfinished.  
You can do this by dragging in a osk file and once finished refresh the page, you only have to do this once.

### Browser Support
This was developed using Chrome 54 but also tested to work on Firefox 50  
Does **NOT** work on IE  
Kinda works on Edge however is very sluggish, Safari is even worse.  
Officially only supporting Chrome/Firefox

(It also works on Chrome on Android but you will encounter no sound atm, as well as scaling issues)


#### Linking replays
When you load a replay, the url will change allowing you to link that replay to someone else eg: https://ugrend.github.io/osuwebreplay/?r=gVQ1V  
You can link at a specific point by adding ```t=1m10s``` eg:  https://ugrend.github.io/osuwebreplay/?r=gVQ1V&t=1m10s

To auto play the replay you can add ```ap=1``` or ```ap=t``` eg: https://ugrend.github.io/osuwebreplay/?r=gVQ1V&t=1m10s&ap=1
### Development

You will need gruntjs and node.js

```
cd src
npm install
```
Once packages have been installed  you can build it With
```
grunt build
```
Alternatively you can run ```grunt watch``` to have it monitor for changes

## Built With

* [PixiJS](https://github.com/pixijs/pixi.js) - Used for 2D rendering
* [zip.js](https://github.com/gildas-lormeau/zip.js) - Used for unziping osz/osk files
* [LZMA-JS](https://github.com/nmrugg/LZMA-JS) - Used for decompressing replay data
* [jQuery](https://github.com/jquery/jquery) - Used for generic purposes
* [jQuery UI](https://github.com/jquery/jquery-ui) - Used for generic purposes
* [js-md5](https://github.com/emn178/js-md5) - Used for calculating md5sums of files
* [Bezier.js](https://github.com/Pomax/bezierjs) - Used to generate certain types of sliders.
* [mustache.js](https://github.com/janl/mustache.js/) - Used to generate parts of the main screen
* [typeahead.js](https://github.com/twitter/typeahead.js/) - Used for beatmap/replay search
* [PNotify](https://github.com/sciactive/pnotify) - Used for notifications
* [howler.js](https://github.com/goldfire/howler.js) - Used for music playback
* [Bootstrap](http://getbootstrap.com/) - Used for styling.

## Author

* [Ugrend](https://github.com/Ugrend)


## License

This project is licensed under GNU GPL version 3. - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* [opsu!](https://github.com/itdelatrisu/opsu) - Some code was referenced when making this project, primarily slider and difficulty calculations.

* Soleily - Renatus which is used for demoing licensed under [CC BY-NC 2.1](https://creativecommons.org/licenses/by-nc/2.1/jp/)


