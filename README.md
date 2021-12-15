# Graphhopper Maps Capacitor
[Capacitor](https://capacitorjs.com/) Wrapper for [GraphHopper Maps](https://github.com/graphhopper/graphhopper-maps)

## Install

We provide automatically generated build artifacts for every commit. You can find them in the [actions tab](https://github.com/boldtrn/graphhopper-maps-capacitor/actions).

## Build

Make sure you have all the [required dependencies](https://capacitorjs.com/docs/v2/getting-started/dependencies)

Then run: `./build.sh`

Note: you can either run the app straight away or open it in Android Studio. You can generate an APK in Android Studio,
or debug the app etc.

**Open Android App**

`npx cap run android`

**Open in Android Studio**

`npx cap open android`

## Updating Version

Make sure to pull the latest version of the submodule "graphhopper-maps". (Automated build tools should do this anyway)

Open `android/build.grade` and increment the `versionCode` and set the `versionName`. 
Important for F-Droid: in the [metadata/com.graphhopper.maps.yml](https://gitlab.com/fdroid/fdroiddata/-/blob/master/metadata/com.graphhopper.maps.yml) AutoUpdateMode: Version v%v, so the tag name must be `v<versionName>` 

With the next gradle build, all the version codes and version names in the generated files should get updated as well.