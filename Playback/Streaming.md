### command for extracted m3u8 URL: 
`yt-dlp -f bestaudio -g <yt-url>`

// this downloads the m3u8 file from which we need to further download the audio chunks.

## steps:
- 2 tg-bot: in a same private channel
	- client:
		-  asking song or browse playlist or song radio
		- receives json response:
			- stream from `m3u8 json` 
			- display results
	- server: 
		- receives requests from tg channel
		- parse req: `song`, `browse`
			- song: helps downloading songs
				- `google-search` songs by artist (official audio)
				- fetch `m3u8` file from `yt-dlp -f bestaudio <yt-url>`
				- parse into json: 
					`master url: <url>, loop:{ timestamp: <remaining url>}}`
				- maybe: download the song and upload to tg-channel
			- browse:
				- playlist / song radio: 
					- fetch playlists from spotify
					- parse into json
					- send response
			- 