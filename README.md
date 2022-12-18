# play-it-music-player-
html , css , java script project of music player in working.

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/jhlywa/chess.js/Node.js%20CI)

generation/validation, piece placement/movement, and check/checkmate/stalemate
detection - basically everything but the AI.

What I use
------------

* JavaScript( ES6 )
* HTML5
* CSS3
* media query for responsiveness


###  Handle play/pause click

```ts
     
     masterPlay.addEventListener('click', ()=>{
    if(audioElement.paused || audioElement.currentTime<=0){
        audioElement.play();
        second();
        masterPlay.classList.remove('fa-play-circle');
        masterPlay.classList.add('fa-pause-circle');
        gif.style.opacity = 1;
    }
    else{
        audioElement.pause();
        first();
        masterPlay.classList.remove('fa-pause-circle');
        masterPlay.classList.add('fa-play-circle');
        gif.style.opacity = 0;
    }
})

```
### Changing song detail

```ts
     Array.from(document.getElementsByClassName('songItemPlay')).forEach((element)=>{
    element.addEventListener('click', (e)=>{ 
        makeAllPlays();
        songIndex = parseInt(e.target.id);
        e.target.classList.remove('fa-play-circle');
        e.target.classList.add('fa-pause-circle');
        audioElement.src = `songs/${songIndex+1}.mp3`;
        changeinimg(songIndex)
        masterSongName.innerText = songs[songIndex].songName;
        audioElement.currentTime = 0;
        audioElement.play();
        gif.style.opacity = 1;
        masterPlay.classList.remove('fa-play-circle');
        masterPlay.classList.add('fa-pause-circle');
    })
})

```

