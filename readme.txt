# beatbox

*In English*

The `beatbox` project was created during Python for Data Processing and Analysis classes. Its main idea was built some kind of application that allows to create simple demo of some song. My `beatbox` can create following demos:

  * the opening theme song from Game of Thrones;
  
  * the Hedwig's theme from Harry Potter;
  
  * Szła dzieweczka do laseczka -- Polish folk song;
  
  * Mam chusteczke... -- also Polish folk song.
  

### How to create a demo using `beatbox`?

To create any demo you shoud type the following onto a line in the terminal to get started:

```{pyton}
python beatbox.py name_demo
```


where `name_demo` can be one of the following names: winter_is_coming, harry_potter, szla_dzieweczka, mam_chusteczke.

The demo was saved in the current directory. To play the created demo you can use following command, eg.:
 
 
```{python}
mplayer name_demo.wav
```

Have fun! :)

*In Polish*

Repozytorium `'beatbox'` zawiera następujące pliki oraz foldery:

* `beatbox.py`: główna aplikacja, która wykorzystuje ponadto poniższe moduły:

	* `read_song.py`: moduł do odczytywania definicji utworu, oraz kolejności tracków oraz sampli;

	* `create_song.py`: moduł do tworzenia demo, uwzględniając definicje utworu, w szczególności takie charakterystyki jak: bpm, attack, decay;

	* `save_song.py`: moduł do zapisu stworzonego wektora częstotliwości do pliku z rozszerzeniem .wav;

	* `nutes.py`: modul pomocniczy: generowanie nutek, podstawowa nutka oparta jest na funkcji $\sin$;

	* `instruments.py`: modul pomocniczy: generowanie dźwięków z dowolnego instrumentu, w poniższych utworach została wykorzystana kombinacja funckji $\sin$, ale można również użyć innych kształtów fali, np. fala piłokształtna.


Wykorzystując powyższe moduły, w szczególności główną aplikację beatbox.py
można wygenerować demo poniższych utworów:

  `mam_chusteczke/`

  `szla_dzieweczka/`

  `harry_potter/`

  `winter_is_coming/`


Każdy folder składa się:

  * `defs.txt`: definicja utworu, informacje na temat bpm, attack, decay;

	* `song.txt`: kolejność odtwarzania tracków;

	* `trackXY.txt`: kolejność odwarzania sampli (sample w tym samym wierszu odtwarzane są w tej samej chwili);

	* `sampleXY.wav/txt`: sample w formacie .wav lub .txt 
	  definicja instrumentu, kazdy plik sampleXY.txt powinien zawierać informacje na temat: 
	  
	    * "id": nazwa instrumentu, 
	  
	    * "fun": funkcja z której generujemy nutki dla wybranego instrumentu, 
	  
	    * "duration": czas trwania grania nutki, 
	  
	    * "vol": głosność nutek generowanych z wybranego instrumentu, 
	  
	    * "attack", 
	  
	    * "decay".


Utworzone demo można znaleźć w bieżącym katalogu, gdzie nazwa jest taka sama jak nazwa katalogu. Każde demo jest zapisywane w formacie .wav.

