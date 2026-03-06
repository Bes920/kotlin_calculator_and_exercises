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
You can run the individual exercises using the following Gradle tasks. These will compile the code and execute the `main` function for each exercise, printing the output directly to your terminal.

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

This project uses **AndroidX** and **Jetifier**. Ensure your `gradle.properties` includes:
```properties
android.useAndroidX=true
android.enableJetifier=true
```

## Releases

To create a release for the **Kotlin Calculator**:

1.  **Build the APK:** Run `./gradlew :app:assembleDebug`.
2.  **Locate the APK:** The file is at `kotlin_calculator/app/build/outputs/apk/debug/app-debug.apk`.
3.  **GitHub Release:** 
    - Create a new tag (e.g., `calc-v1.0`) on GitHub.
    - Title it "Kotlin Calculator v1.0".
    - Upload the `app-debug.apk` as a release asset.

## GitHub Actions

This repository is configured (via `.github/workflows/android.yml`) to automatically build the APK on every push to `main`. You can download the latest build from the **Actions** tab on GitHub under the **Artifacts** section of the latest successful run.
