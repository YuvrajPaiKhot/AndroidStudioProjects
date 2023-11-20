package com.example.formulaspace

import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.Image
import androidx.compose.foundation.background
import androidx.compose.foundation.border
import androidx.compose.foundation.layout.Arrangement
import androidx.compose.foundation.layout.Box
import androidx.compose.foundation.layout.Column
import androidx.compose.foundation.layout.Row
import androidx.compose.foundation.layout.Spacer
import androidx.compose.foundation.layout.fillMaxSize
import androidx.compose.foundation.layout.height
import androidx.compose.foundation.layout.padding
import androidx.compose.foundation.layout.size
import androidx.compose.foundation.layout.width
import androidx.compose.foundation.layout.wrapContentSize
import androidx.compose.material3.Button
import androidx.compose.material3.MaterialTheme
import androidx.compose.material3.Surface
import androidx.compose.material3.Text
import androidx.compose.runtime.Composable
import androidx.compose.runtime.getValue
import androidx.compose.runtime.mutableStateOf
import androidx.compose.runtime.remember
import androidx.compose.runtime.setValue
import androidx.compose.ui.Alignment
import androidx.compose.ui.Modifier
import androidx.compose.ui.graphics.Color
import androidx.compose.ui.res.painterResource
import androidx.compose.ui.res.stringResource
import androidx.compose.ui.text.font.FontWeight
import androidx.compose.ui.text.style.TextAlign
import androidx.compose.ui.tooling.preview.Preview
import androidx.compose.ui.unit.dp
import androidx.compose.ui.unit.sp
import com.example.formulaspace.ui.theme.FormulaSpaceTheme

class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            FormulaSpaceTheme {
                Surface(
                    modifier = Modifier.fillMaxSize(),
                    color = MaterialTheme.colorScheme.background
                ) {
                    formulaLayout()
                }
            }
        }
    }
}

@Composable
fun formulaLayout(modifier: Modifier = Modifier) {
    var result by remember { mutableStateOf(1) }
    var image = when(result){
        1 -> R.drawable.alfa_romeo
        2 -> R.drawable.alphatauri
        3 -> R.drawable.alpine
        4 -> R.drawable.haas
        5 -> R.drawable.aston_martin
        6 -> R.drawable.logo_ferrari_18_
        7 -> R.drawable.mclaren
        8 -> R.drawable.mercedes
        9 -> R.drawable.red_bull
        else -> R.drawable.williams_blue
    }

    var teamName = when(result){
        1 -> R.string.AR
        2 -> R.string.AT
        3 -> R.string.R
        4 -> R.string.H
        5 -> R.string.AM
        6 -> R.string.SF
        7 -> R.string.ML
        8 -> R.string.M
        9 -> R.string.RB
        else -> R.string.W
    }

    Column(
        modifier = modifier
            .fillMaxSize(),
        horizontalAlignment = Alignment.CenterHorizontally,
        verticalArrangement = Arrangement.Center
    ) {
        Box(
            modifier = Modifier
                .background(Color.White)
                .size(350.dp, 280.dp),
            contentAlignment = Alignment.Center
        ) {
            Image(
                painter = painterResource(image),
                contentDescription = null,
                modifier = Modifier
                    .size(300.dp, 250.dp)
            )
        }
        Spacer(modifier = Modifier.height(80.dp))

        Column {
            Text(
                text = stringResource(id = teamName),
                fontSize = 40.sp,
                fontWeight = FontWeight.Bold
            )
        }
        
        Spacer(modifier = Modifier.height(40.dp))

        Row {
            Button(
                onClick = {
                          if(result == 1){
                              result = 10
                          }else{
                              result-=1
                          }
                },
                modifier = Modifier
                    .width(120.dp)
            ) {
                Text(text = "Previous")
            }
            Spacer(modifier = Modifier.width(80.dp))
            Button(
                onClick = {
                          if(result == 10){
                              result = 1
                          }else{
                              result+=1
                          }
                },
                modifier = Modifier
                    .width(120.dp)
            ) {
                Text(text = "Next")
            }
        }
    }
}

@Preview(showBackground = true)
@Composable
fun GreetingPreview() {
    FormulaSpaceTheme {
        formulaLayout()
    }
}
