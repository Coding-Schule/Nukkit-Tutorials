# Simple Form

Hier wirst du lernen wie du eine SimpleForm mit FormAPI erstellst.

Unsere End Form soll später 3 Buttons haben.

- Button 1 mit den namen `Hallo`
- Button 2 mit den namen `Bye`
- Button 3 mit den namen `Close`



# Form erstellen

Als erstes erstellen wir eine Variable names `form` mit dem Title `Test`.

```java
SimpleForm form = new SimpleForm("Test");
```



# Content der Form

Als nächtes setzen wir den Content der form.

```java
form.setContent("Dies ist der beste Content ever");
```

Der content ist quasi eine Beschreibung.



# Buttons

Wie schon gesagt wir wollen eine Form mit 3 Buttons haben. Also let's go lasst es uns machen.

```java
form.addButton("Hallo");
from.addButton("Bye");
```

Ich habe denn dritten button weggelassen weil ich davor ein Bild hintun will.



```java
form.addButton("Close", ImageType.PATH, "textures/items/diamond");
```

Der letze Button hat jetzt ein Diamand Bild.



# Form senden und Funktionen bestimmen

Als nächstes wollen wir behandeln wie man Formen sendet und die Funktionen der Buttons bestimmt.

```java
// Hier senden wir die form zum player
form.send(playeristance, (targetplayer, targetform, data) -> {
    // Hier werden wir jetzt die funktionen bestimmen von den Buttons
    
    if(data == 0) { // data 0 ist der erste Button
        
       targetplayer.sendMessage("Hallo, " + targetplayer.getName()); // ihr könnt auch einfach eure playeristance nehmen
    
    } else if(data == 1) { // data 1 ist der zweite button
        
        targetplayer.sendMessage("Bye, " + targetplayer.getName());
    
    } else { // wenn kein bestimmter button getargeted wurde return wir es einfach
        
        return;
    
    }
    
});
```

Und somit haben wir eine SimpleForm erschaffen.

