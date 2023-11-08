# Lesson 3

## Tasks

Hello everyone! We will continue the dice roller app today:
1. Inserting a TextView below the ImageButton
2. Writing code to show the rolled dice

## Help

Help for some of the tasks above:
1. Just like in lesson 1, but instead insert a TextView.
2. Going back to the kotlin file, we will first create a variable for the TextView:
   ```kotlin
   val dice_text = findViewById<TextView>(R.id.textView)
   ```
   Then, we will create an array that stores the resource ids of different dice images:
   ```kotlin
   val dice_images = arrayOf(R.drawable.dice_1,
    R.drawable.dice_2,
    R.drawable.dice_3,
    R.drawable.dice_4,
    R.drawable.dice_5,
    R.drawable.dice_6)
   ```
   Finally, using `setImageResource` and setting the text of the TextView in the dice button OnClickListener, we can display the generated value to the user:
   ```kotlin
   dice_button.setImageResource(dice_images[dice_result - 1])
   // we should subtract 1 to get the required array index because arrays start from 0
   dice_text.text = "The dice has rolled a " + dice_result.toString() + "!"
   ```
> [!NOTE]
> You should also remove the default `Greeting` functions. The code will look like this:
> ```kotlin
> package com.example.diceroll
> 
> import android.os.Bundle
> import android.widget.ImageButton
> import android.widget.TextView
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
> val dice_images = arrayOf(R.drawable.dice_1,
>     R.drawable.dice_2,
>     R.drawable.dice_3,
>     R.drawable.dice_4,
>     R.drawable.dice_5,
>     R.drawable.dice_6)
> 
> fun roll_dice(): Int {
>     return (1..6).random()
> }
> 
> class MainActivity : ComponentActivity() {
>     override fun onCreate(savedInstanceState: Bundle?) {
>         super.onCreate(savedInstanceState)
>         setContentView(R.layout.activity_main)
>         val dice_button = findViewById<ImageButton>(R.id.imageButton)
>         val dice_text = findViewById<TextView>(R.id.textView)
>         dice_button.setOnClickListener {
>             val dice_result = roll_dice()
>             dice_button.setImageResource(dice_images[dice_result - 1])
>             dice_text.text = "The dice has rolled a " + dice_result.toString() + "!"
>         }
>     }
> }
> ```

## Summary

Feel free to ask me during training if you have any questions. I have attached a video demo showing the current progress.
