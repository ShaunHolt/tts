# Text-to-Speech (TTS) Demo App
A simple web app demonstrating how text sounds in different TTS voices.

This web app will convert your text to speech using voices provided by a variety of TTS services including [Amazon Polly](https://aws.amazon.com/polly/), [CereProc](https://cereproc.com/), [IBM Watson](https://www.ibm.com/cloud/watson-text-to-speech), [Acapela](https://www.acapela-group.com/demos/), [Oddcast](https://www.oddcast.com/ttsdemo/index.php), [ReadSpeaker](https://www.readspeaker.com/), [Google Translate](https://translate.google.com/), [iSpeech](https://ispeech.org/).

NOTE: [Streamlabs'](https://streamlabs.com/) (unofficial) API is used to process TTS with Amazon Polly voices (called via the proxy.php file to work around CORS restrictions and provide some additional features). This can be used to emulate how messages will sound when donating to [Twitch.tv](https://twitch.tv) streamers who have the feature enabled. ![FeelsGoodMan](https://cdn.frankerfacez.com/emoticon/109777/1)

Inspired by [Peter Cunha's](https://github.com/petercunha/tts) very similar tool, I wanted to build this using only vanilla JS, as well as improve it with small UI/UX enhancements and by providing a massive selection of voices, including **all** those offered by Polly and other services.

## Features
- Over 500 different high-quality voices
- Lightning fast
- Copy link to TTS URL to clipboard for sharing with others
- Simple HTML5 and JavaScript, with no dependencies, frameworks, libraries etc. required

## Limitations
Many of the services used aren't intended for professional/commercial use or are utilising a live demo, and as such they have limitations. As a reminder: You should only be using this to test how your text sounds in various voices. If you need to use TTS for commercial purposes please check out the services' respective websites linked above for more information.

#### Polly via Streamlabs
- 550 byte limit for TTS processing with Amazon Polly voices
- TTS is outputted in ogg vorbis which is unsupported in web browsers on iOS, though can be played in third-party apps
- TTS URLs are valid for only 5 minutes.
#### CereProc
- 2000 byte limit
#### IBM Watson
- None?
#### Acapela
- 2000 character limit
- Light background music plays throughout
#### Oddcast
- 600 character limit
#### ReadSpeaker
- 250 character limit
- Says "this is a demo" before or after your text
- Light background music plays throughout
#### Google Translate
- 200 character limit
- TTS URLs are _not_ served over https; the secure URLs require a valid token, which while technically possible to generate, is not something I want to spend time on just for a simple demo app
#### iSpeech
- 150 byte limit (sometimes, and seemingly randomly, it's even less for languages such as Japanese and Chinese)
- Voice will always say "Powered by iSpeech" at the end


## Demo
Can be found at [**LazyPy.ro/tts**](https://lazypy.ro/tts)