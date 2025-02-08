<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sol's Profile & Interests</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #d4e4c4;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
        }
        .profile-card, .container {
            background: #f5f0e1;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            width: 350px;
            text-align: center;
            display: none;
        }
        .profile-card.active, .container.active {
            display: block;
        }
        .profile-pic {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid #a67b5b;
        }
        .username {
            font-size: 22px;
            font-weight: bold;
            color: #5c3d2e;
        }
        .bio {
            font-size: 14px;
            color: #665c54;
            margin-top: 10px;
        }
        .buttons {
            display: flex;
            justify-content: space-around;
            margin-top: 15px;
        }
        .btn {
            background: #a67b5b;
            border: none;
            padding: 8px 15px;
            border-radius: 10px;
            color: white;
            font-size: 14px;
            cursor: pointer;
            transition: 0.3s;
            text-decoration: none;
        }
        .btn:hover {
            background: #8b6347;
        }
        .btn:active {
            animation: bounce 0.3s;
        }
        @keyframes bounce {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        .music-player {
            display: flex;
            align-items: center;
            margin-top: 15px;
            padding: 10px;
            background: #fff;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .play-btn {
            background: none;
            border: none;
            font-size: 20px;
            cursor: pointer;
            color: #a67b5b;
            text-decoration: none;
        }
        h1 {
            font-size: 24px;
            color: #5c3d2e;
        }
        .likes, .dislikes {
            margin-top: 10px;
            padding: 10px;
            border-radius: 10px;
        }
        .likes {
            background-color: #d9f2d0;
        }
        .dislikes {
            background-color: #f2d0d0;
        }
        .info {
            display: inline-block;
            padding: 5px 10px;
            margin: 5px;
            background: #cde3b5;
            border-radius: 5px;
            font-size: 14px;
            color: #4a4a4a;
        }
        .info.dislike {
            background: #e3b5b5;
        }
        .song-thumbnail {
            width: 50px;
            height: 50px;
            border-radius: 5px;
            margin-right: 10px;
            object-fit: cover;
        }
    </style>
</head>
<body>
    <div class="profile-card active" id="profile">
        <img src="https://i.pinimg.com/736x/a7/f8/52/a7f8529907f7ac7a18bb83503e90c869.jpg" alt="Profile Picture" class="profile-pic">
        <div class="username">Sol ★ @clairdeluz</div>
        <div class="bio"> Christian, 16, hispanic<br>Jesus loves you!!!</div>
        <div class="bio">• what is essential is invisible to the eye •</div>
        <div class="buttons">
            <button class="btn" onclick="showPage('profile')">HOME</button>
            <button class="btn" onclick="showPage('interests')">INTERESTS</button>
        </div>
        <div class="music-player">
            <img src="https://i.pinimg.com/736x/e9/43/1a/e9431acbc2d01fcfa8880519b3585ff6.jpg" alt="Bored - Laufey" class="song-thumbnail">
            <span>Bored - Laufey</span>
            <a href="https://open.spotify.com/track/2SPbioo65CuUB3H0aW1ID5?si=0d889b8655ce47e5" target="_blank" class="play-btn">▶</a>
        </div>
    </div>

    <div class="container" id="interests">
        <h1>Interests</h1>
        <div class="likes">
            <strong>( ˶ˆᗜˆ˵ )</strong>
            <div class="info">Bible</div>
            <div class="info">Laufey</div>
            <div class="info">Keeho</div>
            <div class="info">Pochacco</div>
            <div class="info">Simulation games</div>
        </div>
        <div class="dislikes">
            <strong>(·•᷄_•᷅ )</strong>
            <div class="info dislike">Hate</div>
            <div class="info dislike">avocados</div>
            <div class="info dislike">avocados</div>
            <div class="info dislike">🥑</div>
            <div class="info dislike">AVOCADOS!!!</div>
        </div>
        <div class="buttons">
            <button class="btn" onclick="showPage('profile')">HOME</button>
            <button class="btn" onclick="showPage('interests')">INTERESTS</button>
        </div>
    </div>

    <script>
        function showPage(pageId) {
            document.getElementById('profile').classList.remove('active');
            document.getElementById('interests').classList.remove('active');
            document.getElementById(pageId).classList.add('active');
        }
    </script>
</body>
</html>
