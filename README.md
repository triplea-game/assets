# assets
Repository for binary asset files (sound files, images, installer files). These files will be used by the 
game in one way or another, typically packaged with it when the installer is built.

## Git LFS
```
sudo apt install git-lfs
```

### Init git lfs (one-time)

```
git lfs install
git lfs track *.tar.gz
git add .gitattributes
```

Docs: https://git-lfs.github.com/



## Packaging windows 32 bit JRE

Download JRE for windows 32 from:
```
https://adoptopenjdk.net/releases.html
```

Re-repackage into a tar.gz file:
```
unzip OpenJDK11U-jre_x86-32_windows_hotspot_11.0.4_11.zip
cd jdk-11.0.4+11-jre
tar -czvf ../OpenJDK11U-jre_x86-32_windows_hotspot_11.0.4_11.tar.gz *
cd ../
rm -rf jdk-11.0.4+11-jre/ *zip
```

Commit/upload the tar.gz file to:
```
https://github.com/triplea-game/assets/tree/master/install4j
```
