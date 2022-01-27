### ROUGH+INCOMPLETE: adding files to estuary process
1. the quickest way to add files so they are accessible to estuary (due to CORS) is to upload the files to a github pages site.
1. in your IDE (Visual Studio Code) create `samples` folder you haven't already 
1. There are currently two ways to add files on the fly (not having to refresh estuary - though this is not the end of the world)
    1. putting a collection of new `bank(s)` (one to many separate folders of sounds) into a `samples` folder. 
        - drag and drop sound `bank(s)` into the `samples` folder. Having them in a dedicated folder helps with the process below. 
        - in the terminal/console navigate to the `samples` folder
        - run the command 
            - $ `/Users/audiobeing/estuary/generateAudioResources.sh . > resources.json`
            - this will create a `resources.json` file for that `samples` folder
        - **NOTE**: on a mac, .sh files (`generateAudioResources.sh`) must be made ready to execute
            - in the terminal navigate to the `generateAudioResources.sh` file. It is available from `https://github.com/dktr0/estuary` or from the git clone if you have done so. Then run: 
                - $ `chmod 755 generateAudioResources.sh`
        - in the console/terminal navigate back to the main folder of you github pages repository
        - commit the files to the github
            - `git add .`
            - `git commit -m "message for commit"`
            - `git push`
        - wait for the github page to build and deploy - can be monitored in the actions 
            - when complete sounds are available
        - in estuary console run
            - `!reslist "https://audiobeing.github.io/estuary-sounds/samples/resources.json"`
        - the caveat is that you will not be able to update this folder again with the method. Thus if you have another collection that you want to add on the fly create a new samples folder eg. `samples2` and use this as you can add many of these
    2. adding a single file to an existing sound `bank`
        - add the audio file to an existing sound `bank`
        - commit to github
        - in estuary console run 
            - $ `!insertsound "https://audiobeing.github.io/estuary-sounds/samples/ff6/ff6_9962.wav" ff6 0`
            - the 0 at the end is order of the file in the `bank` so add it to the end or you will replace a file and/or a bug will occur. `banks` start at 0. 
        - this does not seem to work if you create a new `bank` folder in the `samples` folder so would be better to create another `samplesN` folder.  
