---
layout: base
title: Student Home 
description: Home Page
hide: true
---

<h1 style="text-align:center; color:green; #4e804f;">☆ Alisha's Blog ☆</h1>

<h3 style="text-align:center;">My name is Alisha Hussain. I'm a Junior at Del Norte High school. </h3>

<h4>My junior year schedule:</h4>

<img src="https://github.com/user-attachments/assets/b12f4e59-bdef-4583-adfa-85f3dd976fa1" alt="My Junior Year Schedule" style="height:400px;">




<div class="hobby-container">
    <img src="images/notebooks/foundation/Sushi.jpeg" alt="Sushi" class="main-image">
   <p class="sushi-text">
            TRY OUT THE BEST SUSHI IN TOWN. I love exploring sushi restaurants, always looking for the freshest sashimi and creative rolls. My favorite type is the spicy tuna roll, but I enjoy trying out new flavors like eel avocado or rainbow rolls. The combination of fresh fish, rice, and delicate sauces always leaves me craving more.
    </p>
    <img src="<img width="441" alt="Screenshot 2024-08-30 at 9 40 14 AM" src="https://github.com/user-attachments/assets/0a6598b7-f8d4-409a-9cea-dd3d995dc405">" alt="Sushi Side Image" class="Side-image">
</div>

<div class="hobby-container">
    <img src="<img width="208" alt="Screenshot 2024-08-30 at 9 38 56 AM" src="https://github.com/user-attachments/assets/f8ad746a-4d2b-4977-a9fd-9a4a72aabcdd">" alt="Favorite Movies" class="main-image2">
    <p class="movie-text">
            Discover some of the greatest movies ever made! I am a huge movie enthusiast and enjoy everything from thrilling action films to heartwarming dramas. One of my all-time favorites is "The Dark Knight," a masterpiece of storytelling and character development. I also love quirky indie films like "Little Miss Sunshine" and animated classics such as "Spirited Away."
    </p>
    <div class="movie-recommendations">
        <label for="genre">Favorite Genre</label>
        <input type="text" id="genre" placeholder="Enter your favorite genre">
        <button id="fetchMovies">Fetch Movies</button>
        <ul id="movieList">
        </ul>
    </div>
</div>

<div class="hobby-container">
    <img src="<img width="306" alt="Screenshot 2024-08-30 at 9 39 31 AM" src="https://github.com/user-attachments/assets/ad9670f1-75e5-4195-a603-a755ca349fed">
" alt="Favorite Songs" class="main-image">
   <p class="song-text">
            Check out my curated playlist! I love listening to music across various genres, from pop and rock to lo-fi and jazz. Some of my top tracks right now include "Blinding Lights" by The Weeknd and "Watermelon Sugar" by Harry Styles. Music helps me relax, focus, and even get energized for my day.
    </p>
    <audio controls class="audio-class">
        <source src="audio/myFavoriteSong.mp3" type="audio/mp3">
        Your browser does not support the audio element.
    </audio>
</div>

<h3>Checkout my Media Links.</h3>
Subscribe to my [YouTube Channel](https://www.youtube.com/@yourchannel) !!

Follow my [Spotify Playlist](https://spotify.com/yourplaylist) !!

<style>
    .hobby-container {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        margin-bottom: 50px;
    }

    .main-image {
        max-width: 500px;
        margin-bottom: 50px;
        animation: moving-glow 2s infinite;
    }

    .main-image2 {
        max-width: 500px;
        margin-bottom: 70px;
        animation: moving-glow2 2s infinite;
    }

    .sushi-text, .movie-text, .song-text {
        position: relative;
        display: inline-block;
        text-align: center;
        max-width: 320px;
    }

    .Side-image {
        display: block;
        margin-left: 40px;
        animation: moving-glow 2s infinite;
    }

    .audio-class {
        animation: moving-glow3 2s infinite;
    }

    .movie-recommendations {
        margin-left: 40px;
        animation: moving-glow2 2s infinite;
    }

    @keyframes moving-glow3 {
        0% {
            box-shadow: 0 0 10px rgba(0, 0, 255, 0.8);
        }
        50% {
            box-shadow: 0 0 30px rgba(0, 0, 255, 0.8);
        }
        100% {
            box-shadow: 0 0 10px rgba(0, 0, 255, 0.8);
        }
    }

    @keyframes moving-glow2 {
        0% {
            box-shadow: 0 0 10px rgba(0, 255, 0, 0.8)
        }
        50% {
             box-shadow: 0 0 30px rgba(0, 255, 0, 0.8)
        }
        100% {
            box-shadow: 0 0 10px rgba(0, 255, 0, 0.8)
        }
    }

    @keyframes moving-glow {
        0% {
            box-shadow: 0 0 10px rgba(255, 0, 0, 0.8);
        }
        50% {
            box-shadow: 0 0 30px rgba(255, 0, 0, 0.8);
        }
        100% {
            box-shadow: 0 0 10px rgba(255, 0, 0, 0.8);
        }
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
    h3 {
        text-align: center;
        margin: 20px 0; 
        margin-bottom: 30px;
        color: #ff4500; 
        animation: bounce 2s infinite;
    }
</style>

<script>
        document.getElementById('fetchMovies').addEventListener('click', () => {
            var genre = document.getElementById('genre').value;
            const endpoint = `https://example.com/api/MoviesByGenre/`+genre;
            if (genre) {
               fetch(endpoint, {
                    method: 'GET'
                })
                .then(response => response.json())
                .then(data => {
                    const movieList = document.getElementById('movieList');
                    movieList.innerHTML = '';
                    data.forEach(movie => {
                        const listItem = document.createElement('li');
                        listItem.textContent = movie.title; 
                        movieList.appendChild(listItem);
                    });
                })
                .catch(error => {
                    console.error('Error:', error);
                });
            } else {
                console.error('Please enter a genre.');
            }
        });
</script>
