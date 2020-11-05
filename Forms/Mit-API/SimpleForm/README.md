# Simple Form

Hier wirst du lernen wie du eine SimpleForm mit FormAPI erstellst.

Unsere End Form soll später 3 Buttons haben.

- Button 1 mit den Namen `Hallo`
- Button 2 mit den Namen `Bye`
- Button 3 mit den Namen `Close`



# Form erstellen

Als erstes erstellen wir eine Variable Namens `form` mit dem Titel `Test`.

```java
SimpleForm form = new SimpleForm("Test");
```



# Content der Form

Als nächtes setzen wir den Content der Form.

```java
form.setContent("Dies ist der beste Content ever");
```

Der content ist quasi eine Beschreibung.



# Buttons

Wie schon gesagt wir wollen eine Form mit 3 Buttons erstellen. Also let's go lasst es uns machen.

```java
form.addButton("Hallo");
from.addButton("Bye");
```

Ich habe den dritten button weg gelassen weil ich davor ein Bild hintun will.



```java
form.addButton("Close", ImageType.PATH, "textures/items/diamond");
```

Der letze Button hat jetzt ein Diamand Bild.



# Form senden und Funktionen bestimmen

Als nächstes wollen wir behandeln wie man Formen sendet und die Funktionen der Buttons bestimmt.

```java
// Hier senden wir die form zum player
form.send(playeristance, (targetplayer, targetform, data) -> {
    // Hier werden wir jetzt die Funktionen von den Buttons bestimmen

    if(data == 0) { // data 0 ist der erste Button

       targetplayer.sendMessage("Hallo, " + targetplayer.getName()); // Ihr könnt auch einfach eure playerinstance nehmen

    } else if(data == 1) { // data 1 ist der zweite button

        targetplayer.sendMessage("Bye, " + targetplayer.getName());

    } else { // Wenn kein Button gedrückt wurde -> return

        return;

    }

});
```

Und somit haben wir eine SimpleForm erstellt.

