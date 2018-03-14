# SearchLiveo [![](https://jitpack.io/v/rudsonlive/searchliveo.svg)](https://jitpack.io/#rudsonlive/searchliveo)
<br>
Library SearchView material design
<br>
<br>
<img src="https://github.com/rudsonlive/SearchView-MaterialDesign/blob/master/Screenshot/SearchLiveo.png">
<br>

# Gradle
Step 1 - Add the JitPack repository to your root build.gradle file
```gradle
allprojects {
  repositories {
    ...
    maven { url 'https://jitpack.io' }
  }
}
```
Step 2 - Add the dependencies:

```gradle
dependencies {
  implementation 'com.github.rudsonlive:searchliveo:1.0.1'
}
```

# Quick Start

<b>1</b> - Add SearchLiveo to your layout
```xml
    <AppBarLayout...

        <FrameLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content">

            <Toolbar.../>

            <br.com.liveo.searchliveo.SearchLiveo
                android:id="@+id/search_liveo"
                android:layout_width="match_parent"
                android:layout_height="wrap_content" />
        </FrameLayout>

    </AppBarLayout>
```
<b>1</b> - Implementing the listener
```java
  implements SearchLiveo.OnSearchListener
  
  @Override
  public void changedSearch(CharSequence text) {}
```
<b>2</b> - Add to my activity
```java
  mSearchLiveo = findViewById(R.id.search_liveo);
  mSearchLiveo.with(this).build();
```
<b>3</b> - SearchLiveo show
```java
  mSearchLiveo.show();  
```
<b>4</b> - If you need to know when SearchLiveo is closed
```java
  mSearchLiveo.with(this).
    hideSearch(new SearchLiveo.OnHideSearchListener() {
        @Override
        public void hideSearch() {}
    }).
  build();
```

# License
```
Copyright 2018 Rudson Lima

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
