
# Rapport


Ändrade namn på appen genom att ändra variabeln som innehöll namnet i 'strings.xml'
Gav appen tillåtelse till internet genom att lägga till koden nedanför i 'AndroidManifest.xml'
```
<uses-permission android:name="android.permission.INTERNET" />
```

- Skapade ett webview element i layout filen, activity_main.xml
```
    <WebView
        android:id="@+id/my_webview"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />
```

- Skapade private member variabel i main-metoden
```
    private WebView myWebView;
```

- Lokaliserade WebView elementet med WebView ID
- Kopplade webviewclient till webivew med
- Hämtade inställningar för webview och aktiverade javascript
Dom tre punkterna ovanför gjordes med koden nedanför

```
        // lokalisera webview elementet från layout filen
        myWebView = findViewById(R.id.my_webview);

        // koppla webviewclient till webview
        myWebView.setWebViewClient(new WebViewClient());

        // hämta inställningar för webview
        WebSettings webSettings = myWebView.getSettings();

        // aktivera javascript
        webSettings.setJavaScriptEnabled(true);
```

- Skapade en hemsida som asset och döpte den till hemsida.html 
- Skapade struktur i html-dokumentet 

- Färdigställde metoder för att visa intern och extern hemsida med 'loadUrl'-funktionen och 
inkluderade länkarna. 
```
    public void showExternalWebPage(){
        // TODO: Add your code for showing external web page here
        // ladda extern webbsida
        myWebView.loadUrl("https://his.se");
    }

    public void showInternalWebPage(){
        // TODO: Add your code for showing internal web page here
        // ladda intern webbsida
        myWebView.loadUrl("file:///android_asset/hemsida.html");
    }
```

**Skriv din rapport här!**

_Du kan ta bort all text som finns sedan tidigare_.

## Följande grundsyn gäller dugga-svar:

- Ett kortfattat svar är att föredra. Svar som är längre än en sida text (skärmdumpar och programkod exkluderat) är onödigt långt.
- Svaret skall ha minst en snutt programkod.
- Svaret skall inkludera en kort övergripande förklarande text som redogör för vad respektive snutt programkod gör eller som svarar på annan teorifråga.
- Svaret skall ha minst en skärmdump. Skärmdumpar skall illustrera exekvering av relevant programkod. Eventuell text i skärmdumpar måste vara läsbar.
- I de fall detta efterfrågas, dela upp delar av ditt svar i för- och nackdelar. Dina för- respektive nackdelar skall vara i form av punktlistor med kortare stycken (3-4 meningar).

Programkod ska se ut som exemplet nedan. Koden måste vara korrekt indenterad då den blir lättare att läsa vilket gör det lättare att hitta syntaktiska fel.

```
function errorCallback(error) {
    switch(error.code) {
        case error.PERMISSION_DENIED:
            // Geolocation API stöds inte, gör något
            break;
        case error.POSITION_UNAVAILABLE:
            // Misslyckat positionsanrop, gör något
            break;
        case error.UNKNOWN_ERROR:
            // Okänt fel, gör något
            break;
    }
}
```

Bilder läggs i samma mapp som markdown-filen.

![](Skärmavbild%202024-04-05%20kl.%2011.59.18.png)
![](Skärmavbild%202024-04-05%20kl.%2012.00.33.png)

Läs gärna:

- Boulos, M.N.K., Warren, J., Gong, J. & Yue, P. (2010) Web GIS in practice VIII: HTML5 and the canvas element for interactive online mapping. International journal of health geographics 9, 14. Shin, Y. &
- Wunsche, B.C. (2013) A smartphone-based golf simulation exercise game for supporting arthritis patients. 2013 28th International Conference of Image and Vision Computing New Zealand (IVCNZ), IEEE, pp. 459–464.
- Wohlin, C., Runeson, P., Höst, M., Ohlsson, M.C., Regnell, B., Wesslén, A. (2012) Experimentation in Software Engineering, Berlin, Heidelberg: Springer Berlin Heidelberg.
