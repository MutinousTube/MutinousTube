<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mutinous Technology</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            text-align: center;
            background-color: #f0f2f5;
            margin: 0;
            padding: 5px 10px;
        }
        .header {
            margin-top: 10px;
            margin-bottom: 10px;
        }
        .profile-img {
            width: 113px;
            height: 113px;
            border-radius: 50%;
            border: 4px solid #fff;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            object-fit: cover;
            display: block;
            margin: 0 auto;
        }
        h3 {
            margin: 5px 0 0 0;
            color: #333;
        }
        .description {
            font-size: 16px;
            color: #333;
            max-width: 400px;
            margin: 2px auto 10px auto;
            font-weight: 500;
        }
        .btn {
            display: block;
            width: 94%; 
            max-width: 400px;
            margin: 12px auto;
            padding: 13px 0;
            text-decoration: none;
            color: white;
            border-radius: 12px;
            font-weight: bold;
            font-size: 16px;
            transition: transform 0.2s;
        }
        .btn:hover { transform: scale(1.02); opacity: 0.9; }
        
        /* Renkler */
        .yt { background-color: #FF0000; }
        .tt { background-color: #000000; }
        .rumble { background-color: #87C232; }
        .dm { background-color: #0066DC; }
        .tg { background-color: #0088cc; }
        .ig { background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%); }
        .tw { background-color: #1DA1F2; }
        .ms { background-color: #6364FF; }
        .wa { background-color: #25D366; }
        .pt { background-color: #FF424D; }
        .fb { background-color: #4267B2; }
        .com { background-color: #555; }
        .mail { background-color: #D44638; }

        /* Video Oynatıcı Alanı */
        .video-container {
            width: 94%;
            max-width: 400px;
            margin: 25px auto;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            position: relative;
            padding-bottom: 56.25%; /* 16:9 Oranı */
            height: 0;
        }
        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: 0;
        }
        
        /* Telegram Resmi Yerleşim Alanı */
        .telegram-container {
            width: 94%;
            max-width: 400px;
            margin: 25px auto;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            background: #fff;
            display: inline-block;
            text-align: left;
        }
    </style>
</head>
<body>

    <div class="header">
        <a href="https://www.youtube.com/@mutinoustube">
            <img src="https://yt3.googleusercontent.com/x0mGWLt60-GJv2ZvwAcvOmkTftz_zogGGIB01a3mqXIZGpvSxL_k_n1eb4kmZWBLIWa6I0atcA=s160-c-k-c0x00ffffff-no-rj" alt="Mutinous Technology Logo" class="profile-img">
        </a>
        
        <a href="https://youtube.com/MutinousTube" style="text-decoration: none; color: inherit;">
            <h3>Mutinous Technology</h3>
        </a>
        
        <p class="description">Bağımsız Yayıncılığıma Hoşgeldiniz Tüm Güncel İçeriklerime Buradan Ulaşabilirsiniz.</p>
    </div>

    <a href="https://youtube.com/MutinousTube" class="btn yt">YouTube</a>
    <a href="https://www.youtube.com/channel/UCNQpjQqIsdUkKjsulWjngJA/join" class="btn dm">Özel Katıl Üyeliği</a>
    <a href="https://www.youtube.com/playlist?list=UUMONQpjQqIsdUkKjsulWjngJA" class="btn ms">Katıl Üyeliği Videoları</a>
    <a href="https://www.tiktok.com/@mutinoustube" class="btn tt">TikTok</a>
    <a href="https://www.rumble.com/user/MutinousTube" class="btn rumble">Rumble</a>
    <a href="https://www.dailymotion.com/MutinousTube" class="btn dm">Dailymotion</a>
    <a href="https://t.me/MutinousTube" class="btn tg">Telegram</a>
    <a href="https://www.instagram.com/MutinousTube" class="btn ig">Instagram</a>
    <a href="https://www.x.com/MutinousTube" class="btn tw">Twitter (X)</a>
    <a href="https://mastodon.social/@MutinousTube" class="btn ms">Mastodon</a>
    <a href="https://whatsapp.com/channel/0029Vb4JKWmIyPtbv15mol0F" class="btn wa">WhatsApp</a>
    <a href="https://www.patreon.com/MutinousTube" class="btn pt">Patreon</a>
    <a href="https://odysee.com/@MutinousTube" class="btn dm">Odysee</a>
    <a href="https://www.facebook.com/MutinousTube" class="btn fb">Facebook</a>
    <a href="https://youtube.com/@MutinousTube/community" class="btn com">Topluluk</a>
    <a href="mailto:MutinousTube@gmail.com" class="btn mail">İletişim</a>

    <!-- YouTube API Oynatıcı Yuvası (Yalnızca bu otomatik oynar) -->
    <div class="video-container">
        <div id="player"></div>
    </div>

    <!-- Dailymotion Oynatma Listesi (Otomatik oynatma tamamen kapatıldı) -->
    <div class="video-container">
        <iframe 
            src="https://www.dailymotion.com/embed/playlist/xbx1yy?autoplay=0&mute=0&queue-autoplay-next=0" 
            allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
            allowfullscreen>
        </iframe>
    </div>

    <script>!function(r,u,m,b,l,e){r._Rumble=b,r[b]||(r[b]=function(){(r[b]._=r[b]._||[]).push(arguments);if(r[b]._.length==1){l=u.createElement(m),e=u.getElementsByTagName(m)[0],l.async=1,l.src="https://rumble.com/embedJS/u4p7gvi"+(arguments[1].video?'.'+arguments[1].video:'')+"/?url="+encodeURIComponent(location.href)+"&args="+encodeURIComponent(JSON.stringify([].slice.apply(arguments))),e.parentNode.insertBefore(l,e)}})}(window, document, "script", "Rumble");</script>

<div id="rumble_v76n2f8"></div>
<script>
Rumble("play", {"video":"v76n2f8","div":"rumble_v76n2f8"});</script>
        </iframe>
    </div>

    <!-- Telegram Resmi Güvenli Oynatma/Gösterim Ekranı -->
    <div class="telegram-container">
        <script async src="https://telegram.org/js/telegram-widget.js?22" data-telegram-post="MutinousTube/111" data-width="100%"></script>
    </div>

    <!-- YouTube Gelişmiş IFrame API Altyapısı -->
    <script>
        var tag = document.createElement('script');
        tag.src = "https://www.youtube.com/iframe_api";
        var firstScriptTag = document.getElementsByTagName('script')[0];
        firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);

        var player;
        function onYouTubeIframeAPIReady() {
            player = new YT.Player('player', {
                height: '100%',
                width: '100%',
                playerVars: {
                    'listType': 'playlist',
                    'list': 'PLs8e_3KWChB_qb5k_r-lYlg31Xyl5AKhu',
                    'autoplay': 1,
                    'mute': 1, 
                    'playsinline': 1,
                    'rel': 0
                },
                events: {
                    'onReady': onPlayerReady
                }
            });
        }

        function onPlayerReady(event) {
            event.target.playVideo();
            
            var unlockSound = function() {
                if (player && typeof player.unMute === 'function') {
                    player.unMute();
                    player.setVolume(100); 
                    player.playVideo();   
                }
                window.removeEventListener('click', unlockSound);
                window.removeEventListener('touchstart', unlockSound);
                window.removeEventListener('scroll', unlockSound);
            };

            window.addEventListener('click', unlockSound);
            window.addEventListener('touchstart', unlockSound);
            window.addEventListener('scroll', unlockSound);
        }
    </script>

</body>
</html>
