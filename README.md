# androidDependency
Finding the gradle dependency has become frustrating for me. In this repository I am going to store all the dependency I am going to use

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

#### Navigation
```gradle
dependencies {
    def nav_version = "2.1.0-alpha02"

    implementation "androidx.navigation:navigation-fragment-ktx:$nav_version" 
    implementation "androidx.navigation:navigation-ui-ktx:$nav_version" 
}
```
[doc](https://developer.android.com/guide/navigation) |  [release](https://developer.android.com/jetpack/androidx/releases/navigation)

#### Navigation
```gradle
dependencies {
    def nav_version = "2.1.0-alpha02"

    implementation "androidx.navigation:navigation-fragment-ktx:$nav_version" 
    implementation "androidx.navigation:navigation-ui-ktx:$nav_version" 
}
```
[doc](https://developer.android.com/guide/navigation) |  [release](https://developer.android.com/jetpack/androidx/releases/navigation)

## Foundation

#### AppCompat
```gradle
dependencies {
  implementation 'androidx.appcompat:appcompat:1.0.2'
}
```
[doc](https://developer.android.com/topic/libraries/support-library/packages.html#v7-appcompat) |  [release](https://developer.android.com/jetpack/androidx/releases/appcompat)

#### Android KTX
```gradle
dependencies {
  implementation 'implementation 'androidx.core:core-ktx:1.0.1'
}
```
[doc](https://developer.android.com/kotlin/ktx.html) |  [release](https://developer.android.com/jetpack/androidx/releases/core)

#### Multidex 
**Therefore, if your minSdkVersion is 21 or higher, you do not need the multidex support library.**
```gradle
dependencies {
  implementation 'com.android.support:multidex:1.0.3'
}
```
[doc](https://developer.android.com/studio/build/multidex.html) |  [release](https://developer.android.com/jetpack/androidx/releases/multidex)

#### Test 
[doc](https://developer.android.com/training/testing/) |  [release](https://developer.android.com/jetpack/androidx/releases/test)



























































