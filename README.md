# log-view-plugin
Gradle plugin for my android app LogView

## Usage
1. Download plugin jar file from releases and place it under your app's project directory. For example i created a new folder `plugins` in root of project, and placed the downloaded `logger-1.0.jar` there.
2. Then in project's `build.gradle` file add the classpath like `classpath files('plugins/logger-1.0.jar')` in `dependencies` block.
3. Now open module's `build.gradle` (usually its `app/build.gradle`) and apply plugin like 
    ```
    apply plugin: com.hax4us.android.AndroidLogPlugin
    ```
5. Now just run task `sh gradlew injectLogger`, now build your app as usual like `sh gradlew assembleDebug` then install it and open **LogView** and you will see your logs there.

## NOTE 
Never forget to run task `cleanLogger` like `sh gradlew cleanLogger` before app's release build.
