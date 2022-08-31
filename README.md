# lolkil-scraper

npm package scraper to complete your app!

# instalation

Use the stable version:
```shell
npm install lolkil-scraper
```
Or via yarn
```shell
yarn add lolkil-scraper
```

Use the unstable version (no guarantee of stability, but latest fixes + features)
```sh
yarn add github:LoliKillers/lolkil-scraper
```

# List Scrape

* [Anime](#anime)
* [Download](#downloader)
* [Convert](#convert)
* [Information](#information)
* [Searching](#search)
* [Stalk](#stalk)
* [Image](#pinterest)
* [Hentai](#hentai)

### Anime 
| name | type | formats | require |
| :------------: | :-----: | :---------------: | :-----: |
| [Anoboy Search](https://62.182.83.93) | anime | anoboy_search | search |
| [Otakudesu Search](https://otakudesu.watch) | anime | otakudesu_search | search |
| [MAL Top Airing](https://myanimelist.net) | anime | mal_top_airing | - |
| [MAL Top Anime](https://myanimelist.net) | anime | mal_top_anime | - |
| [MAL Search Anime](https://myanimelist.net) | anime | mal_search_anime | search |
| [MAL Search Manga](https://myanimelist.net) | anime | mal_search_manga | search |
| [MAL Search Character](https://myanimelist.net) | anime | mal_search_character | search |

Example Code

```javascript
var lolkilScraper = require('lolkil-scraper');
```

```Anoboy Search```
```javascript
var search = 'One Piece'

lolkilScraper.anime.anoboy_search(search)
.then(res => {
    console.log(res)
})
.catch(err => {
  console.log(err)
})
```

```Otakudesu Search```
```javascript
var search = "Jujutsu"

lolkilScraper.anime.otakudesu_search(search)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

```My Anime List Top Airing```
```javascript
lolkilScraper.anime.mal_top_airing()
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

```My Anime List Top Anime```
```javascript
lolkilScraper.anime.mal_top_anime()
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

```My Anime List Search Anime```
```javascript
var search = 'One Piece'

lolkilScraper.anime.mal_search_anime(search)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

```My Anime List Search Manga```
```javascript
var search = 'Luffy'

lolkilScraper.anime.mal_search_character(search)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

### Downloader
| name | type | formats | require |
| :-----: | :-----: | :-----: | :-----: |
| [TikTok](https://vt.tiktok.com) | download | tiktok | url |
| [YouTube DL Mp3](https://www.youtube.com) | download | youtube_dl_mp3 | search |
| [YouTube DL Mp4](https://www.youtube.com) | download | youtube_dl_mp4 | search |
| [YouTube Play Mp3](https://www.youtube.com) | download | youtube_play_mp3 | search |
| [YouTube Play Mp4](https://www.youtube.com) | download | youtube_play_mp4 | search |

Example Code

```javascript
var lolkilScraper = require('lolkil-scraper')
```

```Tik Tok```
```javascript
var url = 'https://vt.tiktok.com/ZSR2vqUFY/?k=1'

lolkilScraper.download.tiktok(url)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```
```YouTube Download Mp3```
```javascript
var url = 'https://youtu.be/hrX2xbeKIJA'

lolkilScraper.download.youtube_dl_mp3(url)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```
```YouTube Download Mp4```
```javascript
var url = 'https://youtu.be/hrX2xbeKIJA'

lolkilScraper.download.youtube_dl_mp4(url)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```
```YouTube Play Mp3```
```javascript
var search = 'One Piece'

lolkilScraper.download.youtube_play_mp3(search)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```
```YouTube Play Mp4```
```javascript
var search = 'One Piece'

lolkilScraper.download.youtube_play_mp4(search)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

### Convert
| name | type | formats | require |
| :-----: | :-----: | :-----: | :-----: |
| [Emoji To Png](https://emojipedia.org) | convert | emoji_to_png | emoji |
| [Google Text To Speech](https://translate.google.com) | convert | gtts | text & language code |

Example Code

```javascript
var lolkilScraper = require('lolkil-scraper')
```

```Emoji To Png```
```javascript
var emoji = '🤑'

lolkilScraper.convert.emoji_to_png(emoji)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

```Google Text To Speech```
```javascript
var text = 'Hallo World'
var language = 'en' // Please check the list of language codes at https://cloud.google.com/speech-to-text/docs/languages

lolkilScraper.convert.gtts(text, language)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

### Information
| name | type | formats | require |
| :------------: | :------------: | :------------: | :------------: |
| [Earthquake Info](https://www.bmkg.go.id) | info | gempa_terkini | - |

Example Code
```javascript
var lolkilScraper = require('lolkil-scraper')
```

```Earthquake Info```
```javascript
lolkilScraper.info.gempa_terkini()
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

### Search
| name | type | formats | require |
| :------------: | :------------: | :------------: | :------------: |
| [Github Repo](https://github.com) | search | github_repo | repo |
| [Film](http://167.99.31.48/) | search | film | film |

Example Code
```javascript
var lolkilScraper = require('lolkil-scraper')
```

```Github Repository```
```javascript
var repo = 'lolkil-scraper'

lolkilScraper.search.github_repo(repo)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

```Film```
```javascript
var lolkilScraper = 'marvel'

lolkilScraper.search.film(repo)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

### Stalk
| name | type | formats | require |
| :------------: | :------------: | :------------: | :------------: |
| [Github Stalk](https://github.com) | stalk | github | username |

Example Code
```javascript
var lolkilScraper = require('lolkil-scraper')
```

```Github Stalk```
```javascript
var username = 'LoliKillers'

lolkilScraper.stalk.github(username)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

### Image
| name | type | formats | require |
| :------------: | :------------: | :------------: | :------------: |
| [Pinterest](https://id.pinterest.com) | image | pinterest | search |
| [Wallpaper Flare](https://www.wallpaperflare.com) | image | wallpaperflare | search |

Example Code
```javascript
var lolkilScraper = require('lolkil-scraper')
```

```Pinterest```
```javascript
var search = 'Loli'

lolkilScraper.image.pinterest(search)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

```Wallpaper Flare```
```javascript
var search = 'Loli'

lolkilScraper.image.wallpaperflare(search)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

### Hentai
| name | type | formats | require |
| :------------: | :------------: | :------------: | :------------: |
| [Search](https://hentai.tv) | hentai | search | search |
| [Random](https://hentai.tv) | hentai | random | - |

Example Code
```javascript
var lolkilScraper = require('lolkil-scraper')
```

```Search Hentai```
```javascript
var search = 'Loli'

lolkilScraper.hentai.search(search)
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

```Random Hentai```
```javascript
lolkilScraper.hentai.random()
.then(res => {
  console.log(res)
})
.catch(err => {
  console.log(err)
})
```

# NOTE

I will continue to update this package, so wait for my next update
For feature requests/report bugs/want to ask questions, please contact me at
* [WhatsApp](https://wa.me/6285785445412)
* [Telegram](https://t.me/Loli_Killers)
* [Instagram](https://instagram.com/ariasu.xyz)
