# ButtonStyle

[Source](https://stackoverflow.com/questions/42684717/rounded-corners-on-material-button)

---

|<img src="https://github.com/gzeinnumer/ButtonStyle/blob/master/preview/preview1.jpg"/>|
|--|

```xml
<Button
    android:id="@+id/btn_login"
    style="@style/AppTheme.RoundedCornerMaterialButton"
    android:layout_width="match_parent"
    android:layout_height="48dp"
    android:layout_margin="16dp"
    android:layout_marginTop="@dimen/space"
    android:text="Login"
    android:textSize="@dimen/h3"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintLeft_toLeftOf="parent"
    app:layout_constraintRight_toRightOf="parent"
    app:layout_constraintTop_toTopOf="parent" />
```
```xml
<style name="AppTheme.RoundedCornerMaterialButton" parent="Widget.AppCompat.Button.Colored">
    <item name="android:background">@drawable/button_rounded_shape_green</item>
</style>
```
```xml
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="rectangle">

    <solid android:color="#C82F2F" />

    <corners android:radius="20dp" />

</shape>
```

---

|<img src="https://github.com/gzeinnumer/ButtonStyle/blob/master/preview/preview2.jpg"/>|
|--|

```xml
<com.google.android.material.button.MaterialButton
    style="@style/Widget.MaterialComponents.Button"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_marginTop="@dimen/def_margin"
    android:text="@string/login"
    app:cornerRadius="25dp"
    app:strokeColor="@color/purple_500" />
```

---

|<img src="https://github.com/gzeinnumer/ButtonStyle/blob/master/preview/preview3.jpg"/>|
|--|

```xml
<LinearLayout
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_marginTop="@dimen/def_margin"
    android:gravity="center"
    android:orientation="horizontal">

    <com.google.android.material.button.MaterialButton
        style="@style/MyButtonLeft"
        android:layout_width="100dp"
        android:backgroundTint="@color/purple_500"
        android:textColor="@color/white"
        android:layout_height="wrap_content"
        android:text="@string/login" />

    <com.google.android.material.button.MaterialButton
        style="@style/MyButtonRight"
        android:backgroundTint="@color/teal_200"
        android:textColor="@color/white"
        android:layout_width="100dp"
        android:layout_height="wrap_content"
        android:text="@string/login" />

</LinearLayout>
```
Change Color Programtitcally
```java
binding.btnBtnRight.setBackgroundTintList(ContextCompat.getColorStateList(DistributorAdvisorSubMenuActivity.this, R.color.colorPrimary));
binding.btnBtnLeft.setBackgroundTintList(ContextCompat.getColorStateList(DistributorAdvisorSubMenuActivity.this, R.color.disabled_grey_light));
```
```xml
<style name="MyButtonLeft" parent="Widget.MaterialComponents.Button.OutlinedButton">
    <item name="shapeAppearanceOverlay">@style/MyShapeAppearanceLeft</item>
</style>

<style name="MyShapeAppearanceLeft">
    <item name="cornerFamily">rounded</item>
    <item name="cornerSizeTopLeft">16dp</item>
    <item name="cornerSizeBottomLeft">16dp</item>
    <item name="cornerSizeTopRight">0dp</item>
    <item name="cornerSizeBottomRight">0dp</item>
</style>

<style name="MyButtonRight" parent="Widget.MaterialComponents.Button.OutlinedButton">
    <item name="shapeAppearanceOverlay">@style/MyShapeAppearanceRight</item>
</style>

<style name="MyShapeAppearanceRight">
    <item name="cornerFamily">rounded</item>
    <item name="cornerSizeTopLeft">0dp</item>
    <item name="cornerSizeBottomLeft">0dp</item>
    <item name="cornerSizeTopRight">16dp</item>
    <item name="cornerSizeBottomRight">16dp</item>
</style>
```
Wanna Try?
```xml
<style name="MyButtonLeft" parent="Widget.MaterialComponents.Button.OutlinedButton">
    <item name="shapeAppearanceOverlay">@style/MyShapeAppearanceLeft</item>
</style>

<style name="MyShapeAppearanceLeft">
    <item name="cornerFamily">rounded</item>
    <item name="cornerFamilyTopRight">cut</item>
    <item name="cornerFamilyBottomRight">cut</item>
    <item name="cornerSizeTopLeft">16dp</item>
    <item name="cornerSizeBottomLeft">16dp</item>
</style>

<style name="MyButtonRight" parent="Widget.MaterialComponents.Button.OutlinedButton">
    <item name="shapeAppearanceOverlay">@style/MyShapeAppearanceRight</item>
</style>

<style name="MyShapeAppearanceRight">
    <item name="cornerFamily">rounded</item>
    <item name="cornerFamilyTopLeft">cut</item>
    <item name="cornerFamilyBottomLeft">cut</item>
    <item name="cornerSizeTopRight">16dp</item>
    <item name="cornerSizeBottomRight">16dp</item>
</style>
```

---

```
Copyright 2021 M. Fadli Zein
```
