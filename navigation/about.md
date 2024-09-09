---
layout: page
title: About
permalink: /about/
---


<h4>My Junior Year Schedule:</h4>

<img src="https://github.com/user-attachments/assets/b12f4e59-bdef-4583-adfa-85f3dd976fa1" alt="My Junior Year Schedule" style="height:400px;">

### About Me

I have a passion for computing and robotics, and I've been exploring these fields both in and out of school. Recently, I had the amazing opportunity to shadow an interventional radiologist, which deepened my interest in the intersection of technology and medicine. When I’m not diving into robotics or school projects, I love indulging in some of my favorite hobbies!

---

<div class="hobby-container">
    <img src="https://github.com/user-attachments/assets/0a6598b7-f8d4-409a-9cea-dd3d995dc405" alt="Sushi" class="main-image2">
    <p class="sushi-text">
        🍣 I absolutely love sushi! Whether it's a classic spicy tuna roll or something the california roll, I'm always on the hunt for the freshest sashimi and the most creative rolls. There's something about the perfect blend of flavors and textures that makes sushi irresistible to me.
    </p>
</div>

---

<div class="hobby-container">
    <img src="https://github.com/user-attachments/assets/79fb646e-5271-40ab-bb83-eb4a05acaa57" alt="Fav Movies" class="main-image">
    <p class="movie-text">
        🎬 I'm a huge fan of movies! My favorite movie by far is Perks of Being a Wallflower, and some other ones I love are all the Spiderman movies. 
    </p>
</div>

---

<div class="hobby-container">
    <img src="https://github.com/user-attachments/assets/ad9670f1-75e5-4195-a603-a755ca349fed" alt="Favorite Songs" class="main-image">
    <p class="song-text">
         🎵 Music is a big part of my life, helping me to relax, focus, and stay motivated. I enjoy a variety of genres, from Rap/Hip-Hop to Indie Pop. Some of my favorite artists right now include Lil Uzi Vert, Juice WRLD, and The Marías. Check out my curated playlist to see what I’m vibing to lately!
    </p>
    <audio controls class="audio-class">
        <source src="audio/myFavoriteSong.mp3" type="audio/mp3">
        
    </audio>
</div>

---

<h3 style="text-align:center;">Connect with Me!</h3>
<div style="text-align:center;">
    <a href="https://spotify.com/yourplaylist" target="_blank">🎵 Follow my Spotify Playlist</a>
</div>

<style>
    .hobby-container {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
        margin-bottom: 30px;
        padding: 20px;
        border: 1px solid #ddd;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }

    .main-image, .main-image2 {
        max-width: 300px;
        margin: 10px;
        border-radius: 10px;
        transition: transform 0.2s;
    }

    .main-image:hover, .main-image2:hover {
        transform: scale(1.05);
    }

    .sushi-text, .movie-text, .song-text {
        text-align: center;
        max-width: 300px;
        margin: 10px;
    }

    .audio-class {
        display: block;
        margin: 20px auto;
    }

    h3 {
        margin: 30px 0;
        color: #ff4500; 
        animation: bounce 2s infinite;
    }

    @keyframes bounce {
        0%, 20%, 50%, 80%, 100% {
            transform: translateY(0);
            color: #0D98BA; 
        }
        40% {
            transform: translateY(-5px); 
            color: #32cd32; 
        }
        60% {
            transform: translateY(-5px); 
            color: #32cd32; 
        }
    }
</style>

<script>
    document.getElementById('fetchMovies').addEventListener('click', () => {
        var genre = document.getElementById('genre').value;
        const endpoint = `https://example.com/api/MoviesByGenre/` + genre;
        if (genre) {
            fetch(endpoint, {
                method: 'GET'
            })
            .then(response => response.json())
            .then(data => {
                const movieList = document.getElementById('movieList');
                movieList.innerHTML = '';
</style>