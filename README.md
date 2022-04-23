# Pokemon-Game
This is the Pokemon Game project. At the start of the game you set a name and choose your starter Pokemon. Then you have multiple options to choose from.

#### Background Music
I made the background sound method by making a variable for the path. I looped through the while loop wich played the music and wait until the music is over so it will be repeated.
```Java
public static void backgroundMusic() {
        String path = new File("").getAbsolutePath() + "\\src\\PokemonBgMusic.wav";
        //Make a File object with a path to the audio file.
        File sound = new File(path);
        
        while(true){
	        try {
	            AudioInputStream ais = AudioSystem.getAudioInputStream(sound);
	            Clip c = AudioSystem.getClip();
	            c.open(ais); //Clip opens AudioInputStream
	            c.start(); //Start playing audio
	
	            //sleep thread for length of the song
	//            Thread.sleep((int)(c.getMicrosecondLength() * 0.001));
	        } catch (Exception e) {
	            System.out.println(e.getMessage());
	        }	
        	try {
				Thread.sleep(28900);
			} catch (InterruptedException e1) {
				// TODO Auto-generated catch block
				e1.printStackTrace();
			}
        }
```
