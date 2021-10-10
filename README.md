# ButtonStyle

[Source](https://stackoverflow.com/questions/42684717/rounded-corners-on-material-button)

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
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="rectangle">

    <solid android:color="#C82F2F" />

    <corners android:radius="20dp" />

</shape>
```