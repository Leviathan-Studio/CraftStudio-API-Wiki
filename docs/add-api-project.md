Adding API to your project
==========================

We are going to see how to simply add the API and use it for your projet

***

## The build.gradle

Add thes lignes to the build.gradle:

```gradle
repositories {
    maven {
        name = "leviathan"
        url = "http://maven.leviathan-studio.com/artifactory/leviathan/"
    }
}

dependencies {
   compile 'com.leviathanstudio:CraftStudio:[API-VERSION]-mc[MINECRAFT-VERSION][-beta]:dev'
}
```

Then change the two parameters:

Replace `[API-VERSION]` by the version of the API (Ex: `0.3.0.86`)<br>
Replace `[MINECRAFT-VERSION]` by the minecraft version of the API, (Ex: `1.11.2`)
Remove the bracket of `[-beta]` if you are using a beta version, completely remove it otherwise.

You should have something like this: `com.leviathanstudio:CraftStudio:0.3.0.86-mc1.11.2-beta`

You can find the list of all version [here](https://github.com/Leviathan-Studio/CraftStudioAPI/releases) or directly on the [maven](http://maven.leviathan-studio.com/artifactory/leviathan/com/leviathanstudio/CraftStudio/)

Once you've add these lignes, just launch a `gradlew setupDecompWorkspace` and a `gradlew eclipse`.

_You are now ready to start your project !_
