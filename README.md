# StealthBotStreamAnnouncer
## 0.1.0

* StealthBot script for use on Battle.net. Tracks streamers and announces updates in chat.

## Notes

* You will need a Twitch API key to make Twitch API calls. Use the client_id parameter.
* This script was last used in 2017 and is not actively maintained. Repository exists for demonstration purposes only. Use at your own risk.
* Last functional with: **StealthBot Beta v.2.7 - Build 482**, **Battle.net during StarCraft 1.16.1**.
* List of tracked streamers is hardcoded into the script. Look for 'streamers' array.
```
streamers = Array( _
	array( _
		"https://api.twitch.tv/kraken/streams/exampleuser?client_id=12345", _
		"exampleuser @ twitch.tv/exampleuser2", _ ' // message displayed to chat
		0 _
	), _
	array( _
		"https://api.twitch.tv/kraken/streams/exampleuser2?client_id=12345", _
		"exampleuser2 @ twitch.tv/exampleuser2", _
		0 _
	), _
	_
	array( _
		"https://api.twitch.tv/kraken/streams/exampleuser3?client_id=12345", _
		"exampleuser3 @ twitch.tv/exampleuser3", _ 
		0 _
	) _
)
```

## Issues

* No delay implemented between web API calls. It's possible that requests are made too fast and server throttling is triggered.
* No exception management.