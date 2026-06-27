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

        /* Video Oynatıcı ve Resim Alanları */
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
        .video-container iframe, .video-container div {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: 0;
        }
        
        /* Liste Kapak Resimleri Stili */
        .playlist-banner {
            width: 94%;
            max-width: 400px;
            margin: 25px auto -15px auto;
            border-radius: 12px;
            display: block;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        
        /* Telegram Resmi Yerleşim Alanı */
        .telegram-container {
            width: 94%;
            max-width: 400px;
            margin: 25px auto;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0,
