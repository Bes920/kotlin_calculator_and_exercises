# Kotlin Learning Projects

A collection of Kotlin-based projects, including an Android Calculator app and a set of programming exercises.

## Project Structure

- **`kotlin_calculator/app`**: An Android application that functions as a calculator/grade calculator.
- **`exercises/`**: A Kotlin JVM module containing various programming exercises.

## Prerequisites

- Android Studio or IntelliJ IDEA
- JDK 17 or higher
- Android SDK (for the calculator app)

## How to Run

### 1. Android Calculator App
To build the debug APK:
```bash
./gradlew :app:assembleDebug
```
The APK will be generated at:
`kotlin_calculator/app/build/outputs/apk/debug/app-debug.apk`

To install it on a connected device:
```bash
./gradlew :app:installDebug
```

### 2. Kotlin Exercises
You can run the individual exercises using the following Gradle tasks.

- **Exercise 1:**
  ```bash
  ./gradlew :exercises:runExercise1
  ```
- **Exercise 2:**
  ```bash
  ./gradlew :exercises:runExercise2
  ```
- **Exercise 3:**
  ```bash
  ./gradlew :exercises:runExercise3
  ```

## Configuration

This project uses **AndroidX**. Ensure your `gradle.properties` includes:
```properties
android.useAndroidX=true
android.enableJetifier=true
```

## Releases & Automation

This repository uses **GitHub Actions** to automate releases and build the APK.

### To Update/Create a Release with a Downloadable APK:

1.  **Commit your changes:**
    ```bash
    git add .
    git commit -m "Your update message"
    git push origin release
    ```

2.  **Create and push a new version tag:**
    (Increment the version number each time, e.g., `v1.1`, `v1.2`)
    ```bash
    git tag v1.1
    git push origin v1.1
    ```

3.  **Monitor the Build:**
    Go to the **Actions** tab on GitHub. The "Build and Release APK" workflow will start.

4.  **Download the APK:**
    Once the action is finished, go to the **Releases** section. Your new release will have the **`app-debug.apk`** in the **Assets** section.

You can monitor the progress in the **Actions** tab of this repository.
