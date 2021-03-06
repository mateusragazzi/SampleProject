# Sample with Vue, Vuetify and Cordova

This project was made to save an sample of a project which uses Vue + Vuetify + Cordova to build Android and Web applications. It contains:

- Vue - 2.6.10 or +
- Vuetify - 2.0.0 or +
- Vue Router - 3.0.3 or +
- Vuex - 3.0.1 or +
- Corodova - 2.3.6 or +
- Babel - 10.0.1 or +
- ESlint - 5.0.0 or +

To use this sample, you must install [Node.js and npm](https://nodejs.org/en/download/).

---

## Enviroment

This project was create using the current versions:

- Node - 11.15.0
- npm - 6.10.2
- Vue - 3.10.0
- Cordova - 9.0.0

Besides, to Cordova work properly to build Android applications, you must have install:

- [Android SKD Tools](https://developer.android.com/studio)
- [Gradle](https://gradle.org/install/)
- [Java JDK](https://www.oracle.com/technetwork/java/javase/downloads/index.html)

Also you need to setup PATH variables. In case of Linux, go to your home directory and edit *.bashrc* adding at the end of this file:

```
export ANDROID_HOME=/home/your_user/Android/Sdk
export PATH=${PATH}:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools
```

After that, run: 

```
source ~/.bashrc
```

To be sure that you have everything working, run:

```
cd src-cordova
cordova requirements
```

The output show if there is any missing configurations.


# Using the sample

Use the following command to clone the project:

```
git clone https://github.com/mateusragazzi/SampleProject.git
```

Then, run a couple of commands:

```
cd SampleProject
npm install
```
This will install the project dependencies. After that, you must setup the link between *dist* and Cordova's *www* directory by running:

```
npm run build
cd src-cordova
rm -rf www
ln -s ../dist/ www
```

Finally, add Android in your project:

```
cordova platform add android
```

## Testing in Web

### Running in browser
```
npm run serve
```

### Build a release for Web
```
npm run build
```

## Testing in Android

### Running in Android

1. Deploy an development version
```
npm run cordova-serve-android
```
2. Deploy in device *
```
cordova run android
```
##### * you must have an emulator or target device

### Build a release for Android

```
npm run build 
cd src-cordova
cordova build android --prod
```
##### * this generate an unsigned apk
---

## How the project was created?

In case you want to know, this project was created by doing:

```
npm install vue
npm install @vue/cli
npm install cordova 
vue create <name of project>
cd project_folder
vue add vuetify
vue add cordova
```

> **Important** <br> in order to make build mirror in Cordova build, create a link into "www" folder by doing: 

```
cd src-cordova/
rm -rf www
ln -s ../dist/ www
```
Then you are ready to go!