# WannabeOS

### Create a directory for the source files
* You can name this directory however you want, just remember to replace 
* This can be located anywhere (as long as the fs is case-sensitive)

```bash 
mkdir wannabe 
cd wannabe
```

### Install Repo in the created directory

>> [Hint: This might take a long time]

```bash
repo init -u https://github.com/WannabeOS/android_manifest -b emptiness
```

>> [Hint: Want to save some space ? Then use this]

```bash
repo init --depth=1 -u https://github.com/WannabeOS/android_manifest -b emptiness
```

### Download the source
```bash 
repo sync -c --force-sync --no-tags --no-clone-bundle -j$(nproc --all) --optimized-fetch
```

### Get all required packages (if this is your first time building any rom)
```bash
# Clone akhilnarang awesome repo
git clone https://github.com/akhilnarang/scripts scripts
# Get all the packages you need
bash scripts/setup/android_build_env.sh
```

### Build
```bash
# Set up environment
. build/envsetup.sh
# Choose a target
lunch wannabe_<device>-userdebug
# Build the code
make bacon -jX
```

### Credits
 * [**AOSP**](https://android.googlesource.com) 
 * [**ArrowOS**](https://github.com/ArrowOS)
 * [**CrystalOS**](https://github.com/CrystalOS-Temp)
 * [**Syberia Project**](https://github.com/syberia-project)
 * [**AospExtended**]( https://github.com/AospExtended)

 
