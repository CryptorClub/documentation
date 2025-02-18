# Object types used across the API


### ImageObject

```javascript
{
	"url": String,
	"width": Number, // Integer
	"height": Number // Integer
}
```


### ThumbnailObject

```javascript
{
	"quality": String,
	"url": String,
	"width": Number, // Integer
	"height": Number // Integer
}
```


### VideoObject

```javascript
{
	"type": "video", // Constant

	"title": String,
	"videoId": String,

	"author": String,
	"authorId": String,
	"authorUrl": String,
	"authorVerified": Boolean,

	"videoThumbnails": [
		// One or more ThumbnailObject
	],

	"description": String,
	"descriptionHtml": String,

	"viewCount": Number, // Integer
	"viewCountText": String,
	"lengthSeconds": Number, // Integer

	"published": Number, // Unix timestamp
	"publishedText": String,

	// Only available on premiered videos
	"premiereTimestamp": Number, // Unix timestamp

	"liveNow": Boolean,
	"premium": Boolean,
	"isUpcoming": Boolean
}
```


### ChannelObject

```javascript
{
	"type": "channel", // Constant

	"author": String,
	"authorId": String,
	"authorUrl": String,
	"authorVerified": Boolean,
	"authorThumbnails": [
		// One or more ThumbnailObject
	],

	"autoGenerated": Boolean,
	"subCount": Number, // Integer
	"videoCount": Number, // Integer

	"description": String,
	"descriptionHtml": String,
}
```


### PlaylistObject

```javascript
{
	"type": "playlist", // Constant

	"title": String,
	"playlistId": String,
	"playlistThumbnail": String,

	"author": String,
	"authorId": String,
	"authorUrl": String,
	"authorVerified": Boolean,

	"videoCount": Number, // Integer
	"videos": [
		{
			"title": String,
			"videoId": String,
			"lengthSeconds": Number, // Integer
			"videoThumbnails": [
				// One or more ThumbnailObject
			]
		}
	]
}
```
