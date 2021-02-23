# Play MP3 in Termux:
Select a youtube playlist, for example:  
https://m.youtube.com/playlist?list=PLW0qrlJ-5IPme5cgsYre0BErCSJGy9lWp
  
Download it using this web (can be ilegal in your country)  
https://loader.to/
  
I fill 12 in playlist end field (number of youtube playlist songs)
  
Press download and wait, when 100% click again. 
  
Install mpg123:
pkg install mpg123

Move the zip from your storage to wjere you want to extract the songs:  
mkdir ~/musica && mv ~/storage/downlads/Videos.zip ~/musica && unzip ~/musica/Videos.zip && rm ~musica/Videos.zip
  
To play a song run mpg123 filename.mp3  
  
Example:  
mpg123 ~/musica/Silversun\ Pickups\ -\ Don\'t\ Know\ Yet.mp3

I used tab key to autocomplete the name using scape secuences.  
You may want to add an alias in ~/.bashrc file to play like
```
play() {
  mpg123 $1;
}
```

Or maybe make your playlists:
```
silversunpickupsplaylist() {
  mpg123 Silversun\ Pickups\ -\ Don\'t\ Know\ Yet.mp3;

  mpg123 Silversun\ Pickups\ -\ Freakazoid\ \(Official\ Audio\).mp3;

  # add more here
}
```

Run the playlist:  
silversunpickups
