# Pepper-Roboter-Template-Kotlin
**How to create a starting composable Application for Pepper Roboter**

## First Time using Pepper
You need following things installed before you can code a Pepper Application
- Android Studio Electric Eel | 2022.1.1 Patch 2 February 27, 2023
- Plugin = **Pepper SDK** Version **API 7**
- Android Studio Platform SDK = **Android API 34**
-  Android Studio Tools SDK = **34.0.0**
-  In Android Studio download the Pepper 1.9 APi 34 tablet
> **Note:** In the documentation folder is a more detail instruction on how to set up a running Pepper Environment
## Create a new Roboter application from scratch
1. From Android Studio chose: **New File** > **Project** > **New Project**
2. Chose **Empty Compose Activity**
3. As Language chose **Kotlin**
4. Set Minimum API level to: **API 23: Andriod 6.0 (Marshmallow)**
5. Wait for the project to be build
6. **File** > **New**> **Robot Application**
7. Set Minimum SDK to **API 7**
8. Apply to Module **xxxx.app** > Press Ok
9. **Build** > **Make Project**
10. An Error should show up
11.  Put this code snippet in your **Gradle Scripts** > **settings.gradle** in the **dependencyResolutionManagement**

> maven {
	url 'http://android.aldebaran.com/sdk/maven'
	allowInsecureProtocol = true
}

12. Save changes **Crtl + S**
13. Execute **File** > **Invalidate Caches** 
14. Android Studio will restart automatically
15. Run the app and more errors will appear
16. Under **Gradle Scripts** > **gradle.properties** copy this code snippet

> android.enableJetifier=true

17. **Build** > **Make Project**
18. **Now you have a running Pepper Application**
19. Now replace the MainActivitiy with the MainActivity Code Snippet from **Documentation/MainActivity**
20. Sync build
21. Under **Gralde Scripts** > **build.gralde (Project: Skeleton)** > **buildscript** > **ext** add this following code snippet
> kotlin_version = '1.7.10'
22. In  **Gralde Scripts** > **build.gralde (Module: app)** > **dependencies** add the following dependencies
> implementation fileTree(dir: 'libs', include: ['*.jar'])
 
> implementation "org.jetbrains.kotlin:kotlin-stdlib-jdk7:$kotlin_version"
>
> implementation 'androidx.activity:activity-compose:1.3.1'
>
> implementation 'androidx.appcompat:appcompat:1.5.1'
> 
> implementation "androidx.compose.ui:ui:$compose_ui_version"
> 
> implementation 'androidx.core:core-ktx:1.9.0'
> 
> implementation 'androidx.constraintlayout:constraintlayout:2.1.4'
> 
> implementation 'androidx.lifecycle:lifecycle-runtime-ktx:2.3.1'
> 
> implementation 'androidx.activity:activity-compose:1.3.1'
> 
> implementation "androidx.compose.ui:ui:$compose_ui_version"
> 
> implementation "androidx.compose.ui:ui-tooling-preview:$compose_ui_version"
> 
> implementation 'androidx.compose.material:material:1.2.0'
> 
> testImplementation 'junit:junit:4.13.2'
> 
> androidTestImplementation 'androidx.test.ext:junit:1.2.1'
> 
> androidTestImplementation 'androidx.test.espresso:espresso-core:3.6.1'
> 
> androidTestImplementation "androidx.compose.ui:ui-test-junit4:$compose_ui_version"
> 
> debugImplementation "androidx.compose.ui:ui-tooling:$compose_ui_version"
> 
> debugImplementation "androidx.compose.ui:ui-test-manifest:$compose_ui_version"
> 
> implementation "androidx.navigation:navigation-compose:2.5.3"
> 
> implementation 'com.aldebaran:qisdk:1.7.5'
> 
> implementation 'com.aldebaran:qisdk-design:1.7.5'
> 
> implementation 'com.squareup.retrofit2:retrofit:2.9.0'
> 
> implementation 'com.squareup.retrofit2:converter-gson:2.5.0'

> **Note:** In the documentation folder is a more detail instruction on how to set up a running Pepper Application
