## estuary sample bank

### setting up files to add to estuary 
- all audio files need to be .wav files - these are the format that work consistently with chrome which is the best for estuary
- all audio files need to be in a folder both of which are named with short names with no special characters or spaces, and do not start with numbers. Numbers after are fine. 
    - ex. `drums2`, `ddr45`, etc - names that describe are better for remembering but not necessary - short are best for working in estuary. 
- long files are fine but do need to be handled in estuary in particular ways which will become clear. Two approaches are to leave longer files as is and handle in estuary or to separate them into sections. As estuary works with patterns of samples there are more options for a collection of 1 sec files (in one folder) than a 15 sec file. That said, it is nice to have some long files. Minute(s) long start reaching the boundary of too long. Again playing with them is possible as we will see. 
- if you have a single file it needs to be in a folder
- if you have a collection of files it becomes a decision of how to organize them. 
- Having a collection of related files in a folder (segmented longer file, or related files such as pecussion, or simply sounds that work well together for whatever reason) have a wide variety of options in estuary and is the standard setup. It is rarer to only have one files as the list below shows for the default sounds.
- a collection of files in a single folder is known as a `bank`
- organizing files is an interesting task that is an open (for the better) issue

### dropbox link
use this [link](https://www.dropbox.com/request/0l8RIjdTwMvtDAlGHUwM) to send the files to my dropbox so I can upload them

### adding files to estuary - more detail [here](addAudioToEstuary.md)
1. put sound `banks` in `samples` folder in VSC
2. in terminal from `samples` folder run: 
`/Users/audiobeing/estuary/generateAudioResources.sh . > resources.json`
3. commit to github
    - `git add .`
    - `git commit -m "message for commit"`
    - `git push`
4. when build/deploy complete files are accessible to estuary
5. in estuary console run
    - $`!reslist "https://audiobeing.github.io/estuary-sounds/samples/resources.json"`
- The caveat is that you will not be able to update this folder again with the method so create a new samples folder eg. `samples2` and use this as you can add many of these - update estuary command as needed. 
1. add the audio file to an existing sound `bank`
2. commit to github
- in estuary console run 
`!insertsound "https://audiobeing.github.io/estuary-sounds/samples/ff6/ff6_9962.wav" ff6 0`
- the 0 at the end is order of the file in the `bank` so add it to the end or you will replace a file and/or a bug will occur. `banks` start at 0. 
- this does not seem to work if you create a new `bank` folder in the `samples` folder so would be better to create another `samplesN` folder. 

### unordered commands 
- cd ~/samples
- /Users/audiobeing/estuary/generateAudioResources.sh . > resources.json

- !showresources
- !clearresources
- !defaultresources
- !reslist "https://audiobeing.github.io/estuary-sounds/samples/resources.json"
- !reslist "https://audiobeing.github.io/estuary-sounds/samples2/resources.json"

- !reset
- !insertsound "https://audiobeing.github.io/estuary-sounds/samples/ff6/ff6_9962.wav" ff6 0
- !insertsound "https://audiobeing.github.io/estuary-sounds/samples/lau0/seg_3.wav" lau0 1

- !insertsound "https://complete-url-to-sound.wav" nameOfSampleBank 0

### misc commands
- !presetview roulette
- !publishviews roulette
- !resetviews
### to do
- create patch to segment a file into chunks - in max with mubu?
## samples to start: full list [here](samplesList.md)

	
