# Lesson 1

## Tasks

Hello everyone! You are expected to complete the following tasks in lesson:
1. [Creating a new Android Studio project - Basic Activity](https://developer.android.com/studio/projects/create-project)
2. Creating a layout folder in res and creating a layout resource file inside
3. [Adding the given dice images into the project](https://developer.android.com/codelabs/basic-android-kotlin-compose-add-images#1)
4. Adding an ImageButton into the layout xml file
5. Set the activity content from the layout resource file

## Help

Help for some of the tasks above:
1. Please refer to the link.
2. You don't need to do this if it's automatically created for you. If not, right click `res` > New > Android Resource Directory, Resource type: layout. Then, right click the new folder > New > Layout Resource File, File Name: `activity_main.xml`.
3. Please also refer to the link. THe dice images are in the `dice_assets` folder.
4. Double click the `activity_main.xml` file and drag an `ImageButton` onto the layout.
5. Go back to `MainActivity.kt`, and add the following inside the `onCreate` function:
```kotlin
setContentView(R.layout.activity_main)
```
> [!NOTE]
> You should also remove the default `Greeting` functions. The code will look like this:
> ```kotlin
> package com.example.diceroll
> 
> import android.os.Bundle
> import androidx.activity.ComponentActivity
> import androidx.activity.compose.setContent
> import androidx.compose.foundation.layout.fillMaxSize
> import androidx.compose.material3.MaterialTheme
> import androidx.compose.material3.Surface
> import androidx.compose.material3.Text
> import androidx.compose.runtime.Composable
> import androidx.compose.ui.Modifier
> import androidx.compose.ui.tooling.preview.Preview
> import com.example.diceroll.ui.theme.DiceRollTheme
> 
> class MainActivity : ComponentActivity() {
>     override fun onCreate(savedInstanceState: Bundle?) {
>         super.onCreate(savedInstanceState)
>         setContentView(R.layout.activity_main)
>     }
> }
> ```

## Summary

Please make sure you end product looks similar to the picture provided. Next lesson we will scale the button and write code that generates a number when the button is clicked.