# Modal Form

Hier wirst du lernen wie du eine ModalForm erstellst.

Eine Modalform ist eigentlich genauso wie eine Simpleform, aber bei einer Modalform hast du nur 2 buttons zur Auswahl.



# Form erstellen

```java
ModalForm form = new ModalForm("title", "content", "button1", "button2");
```



# Form senden

```java
form.send(playerinstance, (targetplayer, targetform, data) -> {
   // Hier kommen die funktionen der 2 buttons hin
    
    if(data == 1) {
        targetplayer.sendMessage("servus"); // Ihr könnt auch einfach eure playeristance nehmen
    } else { // wenn kein bestimmer button getrageted wurde return wird es einfach
        return;
    }
});
```

Und so mit haben wir eine ModalForm erstellt.

Wie ihr seht könnt ihr in nur 8 zeilen eine ModalForm erstellen ^^.
