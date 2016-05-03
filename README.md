# GradleLibraryDependence
# android studio中对第三方依赖统一管理版本的一个示例。

// Top-level build file where you can add configuration options common to all sub-projects/modules.

buildscript {

    repositories {
        jcenter()
    }
    
    dependencies {
        classpath 'com.android.tools.build:gradle:2.1.0'

        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
    }
}

allprojects {

    repositories {
        jcenter()
    }
}

task clean(type: Delete) {
    delete rootProject.buildDir
}

ext {

    // App dependencies
    
    supportLibraryVersion = '23.3.0'

    buildToolsVersion = "${BUILD_TOOLS_VERSION}"
    compileSdkVersion = COMPILE_SDK_VERSION.toInteger()
    minSdkVersion = MIN_SDK_VERSION;
    targetSdkVersion = TARGET_SDK_VERSION;
}
