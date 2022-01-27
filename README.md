# live coding in estuary/tidalCycles
## overview
- about me
- estuary
    - start/stop sounds and sequences
    - adding effects
    - patterns/sequences and subsequences
    - transforming patterns
    - transforming effect patterns
    - handling longer samples
- potential
    - setting up and uploading local files 
     - collaboration
- discussion

## adding files to estuary - more detail [here](addAudioToEstuary.md)
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
