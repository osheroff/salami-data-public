SALAMI Data Set version 2.0
===========================

## Osheroff's salami-data fork

This is my fork of the salami-data-public dataset.  I've gone through SALAMI
and retrieved what music I could from spotify.  Since the original dataset is not (easily) accessible,
this dataset is incomplete.  Changes I've made:

- I don't care about anything but the uppercase ("main") annotations in SALAMI.
- getting the SALAMI annotations to match an audio file that's not from the original source was a pain.
  Silence at the beginning of the track was different, had to hunt down files, whole thing was terrible.
- annotations where I changed things (mostly aligning silence, but an occasional editorial fixup) are stored in
	`annotations/XXX/parsed/textfile3_uppercase.txt`.  I occasionally chose
	annotation 2 over annotation 1 as a starting point in cases where I deemed the first annotator incompetent.
- I have yet to vet the internet archive annotations.  I can only take so much pain.  At least the mp3s will match.
- I've begun collecting an additional corpus.  These are files from my collection as well as additional albums ripped from spotify.


If you'd like the matching audio to this dataset drop me an issue and I can
show you the S3 bucket where I keep it.  Probably the ideal scenario is to
distribute the archive as a torrent or something, but that's a long-term eventuality.

I collated my SALAMI dataset using [Sidify Music Converter](https://www.sidify.com/download.html)

Contents
--------

Each piece of music has 1 or 2 associated text files, since one or two listeners annotated each piece. (In the rare case of piece #78, there are 3 files, to indicate a 3-layer annotation by one listener.) The files are all labelled "textfile1.txt" and "textfile2.txt" and organized in directories by their unique SONG_ID: ```~/annotations/[song_id]/textfile[annotator_number].txt```. Each of these folders contains a subfolder, named ```parsed```, which contains separate files for each layer of the annotation: uppercase letters, lowercase letters, and functions.

Annotations are provided as a single file in the format in which they were written. To understand how to parse this format, please look at the Annotator's Guide, included in this repository (see ```SALAMI Annotator Guide.pdf```).

Metadata describing these files, including artist, track name, song duration and information about which annotators described them, are available in ```metadata.csv```. Additional metadata, with specialized fields for each source database, are provided under ```~/metadata```, and described by ```readme_metadata.txt```.

The old website for this dataset was https://ddmal.music.mcgill.ca/research/SALAMI/annotation/, but *this* repository contains the most complete and up-to-date version of the data.


Changelog
---------

Changes made in update to version 2.0 (17 March 2015):

* Added 50% more data! All annotations with SALAMI ID equal to 3 mod 4 were added.
* Metadata files updated to describe new annotated pieces

Changes made in update to version 1.9 (11 March 2015):

* Now hosted on GitHub
* Revision history reaches back to raw input from annotators
* Many, many formatting errors corrected (such as misplaced end times, and annotations erroneously copied into two places). Thanks Thomas Grill and Jan Schlüter for helping to identify errors

Changes made in update to version 1.2 (25 Sept 2012):

* Parsed version of all annotations included

Changes made in update to version 1.1.1 (21 April 2012):

* Metadata for Isophonics files were all incorrect (SALAMI ID #1600-1654), and have been changed. Thanks to Florian Kaiser for spotting the errors.

Changes made in update to version 1.1 (14 March 2012):

* 28 Isophonics annotation files added (SALAMI ID #1600-1654)
* Additional metadata files with separate readme


License
-------

This data is released under a Creative Commons 0 license, effectively dedicating it to the public domain. More information about this dedication and your rights, please see the details here:
http://creativecommons.org/publicdomain/zero/1.0/
http://creativecommons.org/publicdomain/zero/1.0/legalcode


Citing SALAMI
-------------

However, if publishing work based on this data, we kindly ask you to cite the following paper describing its production and contents:

Jordan B. L. Smith, J. Ashley Burgoyne, Ichiro Fujinaga, David De Roure, and J. Stephen Downie. 2011. Design and creation of a large-scale database of structural annotations. *Proceedings of the International Society for Music Information Retrieval Conference*. Miami, FL. 555-60.


Resources
---------

Visit the SALAMI page under DDMAL's Github for some handy community-written resources for managing SALAMI:
https://github.com/DDMAL/SALAMI

Visit the SALAMI homepage for all other information about the SALAMI project:
https://ddmal.music.mcgill.ca/research/SALAMI/

We cannot share the SALAMI audio directly, but we can point you to matching audio files on YouTube. A list of matching items can be found here: https://github.com/jblsmith/matching-salami


References
----------

Some of the music for which we provide annotations was drawn from the RWC Popular, Classical, Jazz and Genre databases. Information on this music can be found in the following articles:

Masataka Goto, Hiroki Hashiguchi, Takuichi Nishimura, and Ryuichi Oka. 2002. RWC Music Database: Popular, Classical, and Jazz Music Databases. *Proceedings of the International Conference on Music Information Retrieval.* Paris, France. 287-8.

Masataka Goto, Hiroki Hashiguchi, Takuichi Nishimura, and Ryuichi Oka. 2003. RWC Music Database: Music Genre Database and Musical Instrument Sound Database. *Proceedings of the International Conference on Music Information Retrieval.* Baltimore, MD. 229-30.

Please consult the RWC website for more details. https://staff.aist.go.jp/m.goto/RWC-MDB/





	       .+++++~ .
	     .I$77$OII==+?=.
	   .7$ZZZZ7Z?=~~+===+
	  .I$ZZZ$Z?==~=~==~~=+
	  .7$$ZZ77=+===~~~.~:=
	  .+ZZ$ZZ?~=~~~:=~=~=?
	 ...$$7$7~+=~~~~=:=~~:
	 ....7$7$:=,~:~..::=~.
	  ..,,~77++++~~~~=?=~
	   ..:=+IIII:=::~=~.     ....  ..
	      .,~=+=:~+,:..  ..~??=~+++++?.
	          ...      .,,+?=++===++?+?+~.
	           ...?$7$?7?Z+?+===~?=++~=+=.
	       ..:$I+7$7??+~++7II=?+===+?+?~?=.
	      .,$I+II77I??+7??+~??I+?+~++?==~.
	      ,?III?77?$7???+?++?+++I$+++~:.
	      .?77??~?7$7+77?+?++?=:?I+~+.
	      .,77?I++=IZ~?77+?+??=?=???I.
	       .:I?I=~?=I?ZZ77I++=?I?II~ .
	          ~$+I77II7I?I~II+=+?,
	              =?~~..



	,---.     |              o
	`---.,---.|    ,---.,-.-..
	    |,---||    ,---|| | ||
	`---'`---^`---'`---^` ' '`

	Structural Analysis of Large Amounts of Music Information.
