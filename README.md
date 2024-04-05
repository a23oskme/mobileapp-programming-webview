
# Rapport Oskar Steise


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
- Kopplade webviewclient till webivew
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
- Skapade några enkla text-element i html-dokumentet 

- Färdigställde metoder för att visa intern och extern hemsida med 'loadUrl'-funktionen och 
inkluderade länkarna. Dessa funktioner blir kallade på när användaren klickar knappen i dropdown-menyn. 
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

![Screenshot External-webpage](Skärmavbild%202024-04-05%20kl.%2011.59.18.png)
![Screenshot Internal-webpage](Skärmavbild%202024-04-05%20kl.%2012.00.33.png)

