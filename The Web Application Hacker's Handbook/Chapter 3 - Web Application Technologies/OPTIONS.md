The **HTTP `OPTIONS` method** requests permitted communication options for a given URL or server. A client can specify a URL with this method, or an asterisk (`*`) to refer to the entire server.

it can be considered a shortcut to find another hole.

Getting valid methods:

curl -i -X OPTIONS <URL>
	
$ curl -i -X OPTIONS https://auth0.com
		HTTP/2 204
		server: Cowboy
		content-security-policy: frame-ancestors 'self'
		feature-policy: usb 'none'; gyroscope 'none'; accelerometer 'none'; ambient-ligh
		t-sensor 'none'
		x-frame-options: SAMEORIGIN
		referrer-policy: no-referrer-when-downgrade
		vary: Origin, Access-Control-Request-Headers
		**access-control-allow-methods: GET,HEAD,PUT,PATCH,POST,DELETE**
		date: Tue, 01 Jun 2021 13:16:29 GMT
		via: 1.1 vegur, 1.1 2948d9a27a84204b2bc36934485844b4.cloudfront.net (CloudFront)
		strict-transport-security: max-age=31536000
		x-xss-protection: 1
		x-content-type-options: nosniff
		x-cache: Miss from cloudfront
		x-amz-cf-pop: EZE51-C1
		x-amz-cf-id: xkB3DRVmlCqIFv5p9MeMKNxNKHlbTMrTbMlKnzmbXtBJh9x7UCKutA==
