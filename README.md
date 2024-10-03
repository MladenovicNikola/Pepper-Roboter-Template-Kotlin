# Pepper-Roboter-Template-Kotlin
**How to create a starting composable Application for Pepper Roboter**

## First Time using Pepper
You need following things installed before you can code a Pepper Application
- Android Studio Electric Eel | 2022.1.1 Patch 2 February 27, 2023
- Plugin = **Pepper SDK** Version **API 7**
- Android Studio Platform SDK = **Android API 34**
-  Android Studio Tools SDK = **34.0.0**
> **Note:** In the documentation folder is a more detail instruction on how to set up a running Pepper Envouirment
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
15. **Now you have a running Pepper Application**

> **Note:** In the documentation folder is a more detail instruction on how to set up a running Pepper Application