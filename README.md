var username = "cryaotic"

"https://api.twitch.tv/kraken/streams/" + username

/* e.g.



{  
   "stream":{  
      "_id":22031550448,
      "game":"Dungeons \u0026 Dragons",
      "viewers":7664,
      "created_at":"2016-06-26T03:05:28Z",
      "video_height":720,
      "average_fps":60,
      "delay":0,
      "is_playlist":false,
      "_links":{  
         "self":"https://api.twitch.tv/kraken/streams/cryaotic"
      },
      "preview":{  
         "small":"https://static-cdn.jtvnw.net/previews-ttv/live_user_cryaotic-80x45.jpg",
         "medium":"https://static-cdn.jtvnw.net/previews-ttv/live_user_cryaotic-320x180.jpg",
         "large":"https://static-cdn.jtvnw.net/previews-ttv/live_user_cryaotic-640x360.jpg",
         "template":"https://static-cdn.jtvnw.net/previews-ttv/live_user_cryaotic-{width}x{height}.jpg"
      },
      "channel":{  
         "mature":true,
         "status":"Late Night with Cry and Russ",
         "broadcaster_language":"en",
         "display_name":"Cryaotic",
         "game":"Dungeons \u0026 Dragons",
         "language":"en",
         "_id":7951350,
         "name":"cryaotic",
         "created_at":"2009-08-25T18:36:55Z",
         "updated_at":"2016-06-26T05:33:17Z",
         "delay":null,
         "logo":"https://static-cdn.jtvnw.net/jtv_user_pictures/cryaotic-profile_image-717edb17cfe5e649-300x300.png",
         "banner":null,
         "video_banner":"https://static-cdn.jtvnw.net/jtv_user_pictures/cryaotic-channel_offline_image-64efba6b3c511beb-1920x1080.png",
         "background":null,
         "profile_banner":"https://static-cdn.jtvnw.net/jtv_user_pictures/cryaotic-profile_banner-c7a1719c6cc189ce-480.png",
         "profile_banner_background_color":"#1c6469",
         "partner":true,
         "url":"https://www.twitch.tv/cryaotic",
         "views":27407168,
         "followers":582103,
         "_links":{  
            "self":"http://api.twitch.tv/kraken/channels/cryaotic",
            "follows":"http://api.twitch.tv/kraken/channels/cryaotic/follows",
            "commercial":"http://api.twitch.tv/kraken/channels/cryaotic/commercial",
            "stream_key":"http://api.twitch.tv/kraken/channels/cryaotic/stream_key",
            "chat":"http://api.twitch.tv/kraken/chat/cryaotic",
            "features":"http://api.twitch.tv/kraken/channels/cryaotic/features",
            "subscriptions":"http://api.twitch.tv/kraken/channels/cryaotic/subscriptions",
            "editors":"http://api.twitch.tv/kraken/channels/cryaotic/editors",
            "teams":"http://api.twitch.tv/kraken/channels/cryaotic/teams",
            "videos":"http://api.twitch.tv/kraken/channels/cryaotic/videos"
         }
      }
   },
   "_links":{  
      "self":"https://api.twitch.tv/kraken/streams/cryaotic",
      "channel":"https://api.twitch.tv/kraken/channels/cryaotic"
   }
}




OR


{  
   "stream":null,
   "_links":{  
      "self":"https://api.twitch.tv/kraken/streams/cryaotic",
      "channel":"https://api.twitch.tv/kraken/channels/cryaotic"
   }
}



*/




if stream != null

	// else wait 30 seconds repeat
	
"https://api.twitch.tv/kraken/channels/" + username + "/videos?broadcasts=true&limit=1&offset=0"


/*



{  
   "_total":51,
   "_links":{  
      "self":"https://api.twitch.tv/kraken/channels/cryaotic/videos?broadcast_type=archive&broadcasts=true&limit=1&offset=0&user=cryaotic",
      "next":"https://api.twitch.tv/kraken/channels/cryaotic/videos?broadcast_type=archive&broadcasts=true&limit=1&offset=1&user=cryaotic"
   },
   "videos":[  
      {  
         "title":"Late Night with Cry and Russ",
         "description":null,
         "broadcast_id":22031550448,
         "broadcast_type":"archive",
         "status":"recording",
         "tag_list":"",
         "views":299,
         "created_at":"2016-06-26T03:05:50Z",
         "url":"https://www.twitch.tv/cryaotic/v/74568661",
         "_id":"v74568661",
         "recorded_at":"2016-06-26T03:05:29Z",
         "game":"Drawful 2",
         "length":11122.689915688,
         "preview":"https://static-cdn.jtvnw.net/v1/AUTH_system/vods_b3ec/cryaotic_22031550448_475447422/thumb/thumb0-320x240.jpg",
         "thumbnails":[  
            {  
               "url":"https://static-cdn.jtvnw.net/v1/AUTH_system/vods_b3ec/cryaotic_22031550448_475447422/thumb/thumb0-320x240.jpg",
               "type":"generated"
            }
         ],
         "fps":{  
            "audio_only":0.0,
            "chunked":60.0,
            "high":26.25,
            "low":26.25,
            "medium":26.25,
            "mobile":26.25
         },
         "resolutions":{  
            "chunked":"1280x720",
            "high":"1280x720",
            "low":"640x360",
            "medium":"852x480",
            "mobile":"400x226"
         },
         "_links":{  
            "self":"https://api.twitch.tv/kraken/videos/v74568661",
            "channel":"https://api.twitch.tv/kraken/channels/cryaotic"
         },
         "channel":{  
            "name":"cryaotic",
            "display_name":"Cryaotic"
         }
      }
   ]
}



*/



parse file for "_id"

// v74568661

set "_id" = VOD_ID

replace "v" for ""

// VOD_ID = 74568661

"https://api.twitch.tv/api/vods/" + VOD_ID + "/access_token"

/* Returns



{"token":"{\"user_id\":97449834,\"vod_id\":74568661,\"expires\":1466995335,\"chansub\":{\"restricted_bitrates\":[]},\"privileged\":false,\"https_required\":false}","sig":"1e8cd628c0dded3d07ffb8d91d411e327ce438ca"}



*/


set "token" = token1

replace "\\" with ""

// token1 = {"user_id":97449834,"vod_id":74568661,"expires":1466995335,"chansub":{"restricted_bitrates":[]},"privileged":false,"https_required":false}

set "sig" = sig

// sig = 1e8cd628c0dded3d07ffb8d91d411e327ce438ca

"http://usher.twitch.tv/vod/" + VOD_ID + "?nauth=" + token1 + "&nauthsig=" + sig + "&allow_source=true"

/*
		
		http://usher.twitch.tv/vod/74568661?nauth={"user_id":97449834,"vod_id":74568661,"expires":1466995335,"chansub":{"restricted_bitrates":[]},"privileged":false,"https_required":false}&nauthsig=1e8cd628c0dded3d07ffb8d91d411e327ce438ca&allow_source=true
	
*/

//returns json file with VOD_ID as the title, contains links for .m3u8 files

/*




#EXTM3U
#EXT-X-TWITCH-INFO:ORIGIN="swift",CLUSTER="edgecast_vod",REGION="NA",MANIFEST-CLUSTER="edgecast_vod",USER-IP="100.37.242.69"
#EXT-X-MEDIA:TYPE=VIDEO,GROUP-ID="chunked",NAME="Source",AUTOSELECT=YES,DEFAULT=YES
#EXT-X-STREAM-INF:PROGRAM-ID=1,BANDWIDTH=3778894,CODECS="avc1.4D4020,mp4a.40.2",RESOLUTION="1280x720",VIDEO="chunked"
http://vod.edgecast.hls.ttvnw.net/v1/AUTH_system/vods_b3ec/cryaotic_22031550448_475447422/chunked/index-dvr.m3u8
#EXT-X-MEDIA:TYPE=VIDEO,GROUP-ID="high",NAME="High",AUTOSELECT=YES,DEFAULT=YES
#EXT-X-STREAM-INF:PROGRAM-ID=1,BANDWIDTH=1103278,CODECS="avc1.4D401F,mp4a.40.2",RESOLUTION="1280x720",VIDEO="high"
http://vod.edgecast.hls.ttvnw.net/v1/AUTH_system/vods_b3ec/cryaotic_22031550448_475447422/high/index-dvr.m3u8
#EXT-X-MEDIA:TYPE=VIDEO,GROUP-ID="medium",NAME="Medium",AUTOSELECT=YES,DEFAULT=YES
#EXT-X-STREAM-INF:PROGRAM-ID=1,BANDWIDTH=653864,CODECS="avc1.4D401E,mp4a.40.2",RESOLUTION="852x480",VIDEO="medium"
http://vod.edgecast.hls.ttvnw.net/v1/AUTH_system/vods_b3ec/cryaotic_22031550448_475447422/medium/index-dvr.m3u8
#EXT-X-MEDIA:TYPE=VIDEO,GROUP-ID="low",NAME="Low",AUTOSELECT=YES,DEFAULT=YES
#EXT-X-STREAM-INF:PROGRAM-ID=1,BANDWIDTH=499986,CODECS="avc1.42C01E,mp4a.40.2",RESOLUTION="640x360",VIDEO="low"
http://vod.edgecast.hls.ttvnw.net/v1/AUTH_system/vods_b3ec/cryaotic_22031550448_475447422/low/index-dvr.m3u8
#EXT-X-MEDIA:TYPE=VIDEO,GROUP-ID="mobile",NAME="Mobile",AUTOSELECT=YES,DEFAULT=YES
#EXT-X-STREAM-INF:PROGRAM-ID=1,BANDWIDTH=270438,CODECS="avc1.42C00D,mp4a.40.2",RESOLUTION="400x226",VIDEO="mobile"
http://vod.edgecast.hls.ttvnw.net/v1/AUTH_system/vods_b3ec/cryaotic_22031550448_475447422/mobile/index-dvr.m3u8




*/


parse file for links 

/*

Chunked = Source
High = High
Medium = Medium
Low = Low
Mobile = Mobile

*/


// going with source because the rest is for scrubs Kappa

parse chunked url
chunked = source

"http://vod.edgecast.hls.ttvnw.net/v1/AUTH_system/vods_b3ec/cryaotic_22031550448_475447422/chunked/index-dvr.m3u8"

returns .m3u8 playlist file 

remove "index-dvr.m3u8" from source url // somehow???

"http://vod.edgecast.hls.ttvnw.net/v1/AUTH_system/vods_b3ec/cryaotic_22031550448_475447422/chunked/"

/* e.g.


#EXTM3U
#EXT-X-VERSION:3
#EXT-X-TARGETDURATION:2
#ID3-EQUIV-TDTG:2016-06-26T03:06:34
#EXT-X-PLAYLIST-TYPE:EVENT

#EXT-X-TWITCH-ELAPSED-SECS:0.0
#EXT-X-TWITCH-TOTAL-SECS:13784.433
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=0&end_offset=944323
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=944324&end_offset=1888835
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=1888836&end_offset=2832783
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=2832784&end_offset=3778047
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=3778048&end_offset=4722183
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=4722184&end_offset=5667635
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=5667636&end_offset=6612523
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=6612524&end_offset=7557787
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=7557788&end_offset=8502863
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=8502864&end_offset=9448127
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=9448128&end_offset=10392639
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=10392640&end_offset=11336775
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=11336776&end_offset=12281475
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=12281476&end_offset=13225987
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=13225988&end_offset=14170123
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=14170124&end_offset=15115011
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=15115012&end_offset=16060275
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=16060276&end_offset=17004599
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=17004600&end_offset=17949863
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=17949864&end_offset=18894751
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=18894752&end_offset=19840767
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=19840768&end_offset=20785655
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=20785656&end_offset=21731107
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=21731108&end_offset=22675431
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=22675432&end_offset=23620319
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=23620320&end_offset=24563703
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=24563704&end_offset=25508967
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=25508968&end_offset=26453667
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=26453668&end_offset=27398367
#EXTINF:2.000,
index-0000000029-Qd9l.ts?start_offset=27398368&end_offset=28343255
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=0&end_offset=945075
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=945076&end_offset=1889211
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=1889212&end_offset=2834287
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=2834288&end_offset=3778611
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=3778612&end_offset=4723499
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=4723500&end_offset=5668575
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=5668576&end_offset=6613087
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=6613088&end_offset=7557975
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=7557976&end_offset=8502487
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=8502488&end_offset=9446999
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=9447000&end_offset=10391135
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=10391136&end_offset=11335835
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=11335836&end_offset=12280347
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=12280348&end_offset=13225235
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=13225236&end_offset=14170311
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=14170312&end_offset=15114071
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=15114072&end_offset=16058771
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=16058772&end_offset=17003471
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=17003472&end_offset=17948171
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=17948172&end_offset=18892119
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=18892120&end_offset=19836631
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=19836632&end_offset=20781895
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=20781896&end_offset=21726219
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=21726220&end_offset=22670731
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=22670732&end_offset=23615431
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=23615432&end_offset=24559755
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=24559756&end_offset=25504455
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=25504456&end_offset=26448779
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=26448780&end_offset=27395547
#EXTINF:2.000,
index-0000000059-g5QM.ts?start_offset=27395548&end_offset=28339307


*/

parse for first returned value "index-0000000029...start_offset=0&..."
parse for "last" first returned value "index-0000000029...start_offset=...end_offset=28343255"

go to source + returned values

// http://vod.edgecast.hls.ttvnw.net/v1/AUTH_system/vods_b3ec/cryaotic_22031550448_475447422/chunked/index-0000000029-Qd9l.ts?start_offset=0&end_offset=28343255

rinse and repeat 

