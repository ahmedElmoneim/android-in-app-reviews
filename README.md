# Library to wrap Google's new in-app reviews-feature, which let you rate apps without switching to the Play Store!

[![](https://jitpack.io/v/grizzly/android-in-app-reviews.svg)](https://jitpack.io/#grizzly/android-in-app-reviews)

## Install

### Step 1 Add the JitPack repository to your build file

```groovy
allprojects {
  repositories {
    maven { url 'https://jitpack.io' }
  }
}
```

### Step 2 Add the dependency

```groovy
dependencies {
  implementation 'com.github.grizzly:android-in-app-reviews:{latest.version}'
}
```

## Usage

### Configuration

Android In-App-Reviews provides methods to configure its behavior.

```java
@Override
protected void onCreate(Bundle savedInstanceState) {
  super.onCreate(savedInstanceState);
  setContentView(R.layout.activity_main);

  GNTReviewManager.with(this)
      .setInstallDays(2) // default 10, 0 means install day.
      .setLaunchTimes(3) // default 10
      .setRemindInterval(2) // default 1
      .setDebug(false) // default false
      .monitor();

  // Show a dialog if meets conditions
  GNTReviewManager.showRateDialogIfMeetsConditions(this);
}
```

## Contribute

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
  
