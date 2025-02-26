![example thing](https://github.com/user-attachments/assets/e4366309-3a1a-426a-8409-70248f042634)

using songrec which uses shazam so like not 100% always right on the song

### Instructions
-
1. okay so like create a text file anywhere (just make sure to change it if not in ~/tmp) and name it song.txt
2. in the .config folder for waybar create a folder titled scripts 
3. in the folder, create a bash file named song.sh
4. add this into song.sh 
```
#!/bin/bash
touch ~/tmp/song.txt | songrec listen | tee ~/tmp/song.txt
```
5. make sure that song.sh runs on launch
6. add this in ur config.jsonc
```
"custom/song": {
        "interval": 1,
        "format": "{}",
        "exec":  "tail -n1 ~/tmp/song.txt"
     },
```
7. and ur done, if something doesnt work for u ill be happy to help!! :3
