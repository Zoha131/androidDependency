
## Architecture

#### Data Binding
```gradle
android {
    ...
    dataBinding {
        enabled = true
    }
}
```
[doc](https://developer.android.com/topic/libraries/data-binding) |  [release](https://developer.android.com/jetpack/androidx/releases/databinding)

---

#### Lifecycle | LiveData | ViewModel
```gradle
dependencies {
    def lifecycle_version = "2.0.0"

    // ViewModel and LiveData
    implementation "androidx.lifecycle:lifecycle-extensions:$lifecycle_version"
   
    kapt "androidx.lifecycle:lifecycle-compiler:$lifecycle_version"
    
    // optional - ReactiveStreams support for LiveData
    implementation "androidx.lifecycle:lifecycle-reactivestreams-ktx:$lifecycle_version"

    // optional - Test helpers for LiveData
    testImplementation "androidx.arch.core:core-testing:$lifecycle_version"
}
```
[doc](https://developer.android.com/topic/libraries/architecture/livedata) |  [release](https://developer.android.com/jetpack/androidx/releases/lifecycle)

---

#### Navigation
```gradle
dependencies {
    def nav_version = "2.1.0-alpha02"

    implementation "androidx.navigation:navigation-fragment-ktx:$nav_version" 
    implementation "androidx.navigation:navigation-ui-ktx:$nav_version" 
}
```
[doc](https://developer.android.com/guide/navigation) |  [release](https://developer.android.com/jetpack/androidx/releases/navigation)

---

#### Paging
```gradle
dependencies {
    def paging_version = "2.1.0"

    implementation "androidx.paging:paging-runtime-ktx:$paging_version"

    // alternatively - without Android dependencies for testing
    testImplementation "androidx.paging:paging-common-ktx:$paging_version"

    // optional - RxJava support
    implementation "androidx.paging:paging-rxjava2-ktx:$paging_version"
}
```
[doc](https://developer.android.com/training/data-storage/room/index.html) |  [release](https://developer.android.com/jetpack/androidx/releases/room)

---

#### Room
```gradle
dependencies {
    def room_version = "2.1.0-alpha06"

    implementation "androidx.room:room-runtime:$room_version"
    kapt "androidx.room:room-compiler:$room_version" // For Java use annotationProcessor instead of kapt

    // optional - Kotlin Extensions and Coroutines support for Room
    implementation "androidx.room:room-ktx:$room_version"

    // optional - RxJava support for Room
    implementation "androidx.room:room-rxjava2:$room_version"

    // optional - Guava support for Room, including Optional and ListenableFuture
    implementation "androidx.room:room-guava:$room_version"

    // Test helpers
    testImplementation "androidx.room:room-testing:$room_version"
}
```
[doc](https://developer.android.com/topic/libraries/architecture/paging/) |  [release](https://developer.android.com/jetpack/androidx/releases/paging)

---

#### WorkManager
```gradle
dependencies {
    def work_version = 2.0.1

    implementation "androidx.work:work-runtime-ktx:$work_version"

    // optional - RxJava2 support
    implementation "androidx.work:work-rxjava2:$work_version"
    
    // optional - Test helpers
    androidTestImplementation "androidx.work:work-testing:$work_version"
}
```
[doc](https://developer.android.com/topic/libraries/architecture/workmanager) |  [release](https://developer.android.com/jetpack/androidx/releases/work)

---

## Foundation

#### AppCompat
```gradle
dependencies {
  implementation 'androidx.appcompat:appcompat:1.0.2'
}
```
[doc](https://developer.android.com/topic/libraries/support-library/packages.html#v7-appcompat) |  [release](https://developer.android.com/jetpack/androidx/releases/appcompat)

---

#### Android KTX
```gradle
dependencies {
  implementation 'implementation 'androidx.core:core-ktx:1.0.1'
}
```
[doc](https://developer.android.com/kotlin/ktx.html) |  [release](https://developer.android.com/jetpack/androidx/releases/core)

---

#### Multidex 
**Therefore, if your minSdkVersion is 21 or higher, you do not need the multidex support library.**
```gradle
dependencies {
  implementation 'com.android.support:multidex:1.0.3'
}
```
[doc](https://developer.android.com/studio/build/multidex.html) |  [release](https://developer.android.com/jetpack/androidx/releases/multidex)

---

#### Test 
[doc](https://developer.android.com/training/testing/) |  [release](https://developer.android.com/jetpack/androidx/releases/test)

---

## Library


#### RecyclerView
```gradle
dependencies {
  implementation 'androidx.recyclerview:recyclerview:1.0.0'
}
```
[doc](https://developer.android.com/guide/topics/ui/layout/recyclerview) | [release](https://developer.android.com/jetpack/androidx/releases/recyclerview)

---

#### Epoxy - Airbnb
```gradle
apply plugin: 'kotlin-kapt'

kapt {
    correctErrorTypes = true
}

dependencies {
  implementation 'com.airbnb.android:epoxy:3.4.0'
  kapt 'com.airbnb.android:epoxy-processor:3.4.0'
}
```
[doc](https://github.com/airbnb/epoxy/wiki) | [release](https://github.com/airbnb/epoxy/releases)

---

#### Paris - Airbnb
```gradle
dependencies {
    implementation 'com.airbnb.android:paris:1.2.1'
    kapt 'com.airbnb.android:paris-processor:1.2.1'
}
```
[doc](https://github.com/airbnb/paris/wiki) | [release](https://github.com/airbnb/paris/releases)

---

#### Lottie - Airbnb
```gradle
dependencies {
    implementation "com.airbnb.android:lottie:3.0.0"
}
```
[doc](https://airbnb.io/lottie/#/android) | [release](https://github.com/airbnb/lottie-android/releases) | [lottiefiles](https://lottiefiles.com)

---

#### MvRx - Airbnb
```gradle
dependencies {
  implementation 'com.airbnb.android:mvrx:1.0.0'
}
```
[doc](https://github.com/airbnb/MvRx/wiki) | [release](https://github.com/airbnb/MvRx/releases)

---

#### Koin
```gradle
repositories {
  jcenter()    
}
dependencies {
    // Koin for Android
    implementation 'org.koin:koin-android:2.0.0-rc-2'
    // or Koin for Lifecycle scoping
    implementation 'org.koin:koin-androidx-scope:2.0.0-rc-2'
    // or Koin for Android Architecture ViewModel
    implementation 'org.koin:koin-androidx-viewmodel:2.0.0-rc-2'
}
```
[doc](https://insert-koin.io/docs/2.0/quick-references/starting-koin/) |  [release](https://github.com/InsertKoinIO/koin/releases)

---

#### Dagger
```gradle
apply plugin: 'kotlin-kapt'

dependencies {
    implementation 'com.google.dagger:dagger:2.22.1'
    kapt 'com.google.dagger:dagger-compiler:2.22.1'
}
```
[doc](https://google.github.io/dagger/users-guide) |  [release](https://github.com/google/dagger/releases)

---

#### okHttp
```gradle
dependencies {
  implementation "com.squareup.okhttp3:okhttp:3.14.1"
  
  testImplementation "com.squareup.okhttp3:mockwebserver:3.14.1"
}
```
[doc](https://github.com/square/okhttp/wiki) |  [release](https://github.com/square/okhttp/releases)

---

#### Retrofit
```gradle
dependencies {
    def retrofit_version = "2.5.0"
    
    implementation "com.squareup.retrofit2:retrofit:$retrofit_version"
    
    //for gson converter
    implementation "com.squareup.retrofit2:converter-gson:$retrofit_version"
    
    //for moshi converter
    implementation "com.squareup.retrofit2:converter-moshi:$retrofit_version"    
    
}
```
[doc](https://square.github.io/retrofit/) |  [release](https://github.com/square/retrofit/releases)

---

#### Gson
```gradle
dependencies {
  implementation 'com.google.code.gson:gson:2.8.5'
}
```
[doc](https://github.com/google/gson) |  [release](https://github.com/google/gson/releases)

---

#### Moshi
```gradle
dependencies {
  implementation "com.squareup.moshi:moshi:1.8.0"
}
```
[doc](https://github.com/square/moshi) |  [release](https://github.com/square/moshi/releases)

---

#### Material
```gradle
dependencies {
  implementation 'com.google.android.material:material:1.0.0'
}

# Compile your app with Android P
# Ensure you are using *AppCompatActivity*
# Change your app theme to inherit from a Material Components theme
```
[doc](https://material.io/develop/android/components/dialog/) |  [release](https://github.com/material-components/material-components-android/releases)

---


























































