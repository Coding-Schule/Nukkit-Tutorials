# Modal Form

Hier wirst du lernen wie du eine ModalForm erstellst.

Eine Modalform ist eigentlich genauso wie eine Simpleform, aber bei einer Modalform hast du nur 2 Buttons zur Auswahl.



# Form erstellen

```java
ModalForm form = new ModalForm("title", "content", "button1", "button2");
```



# Form senden

```java
form.send(playerinstance, (targetplayer, targetform, data) -> {
   // Hier kommen die Funktionen der 2 Buttons hin

    if(data == 1) {
        targetplayer.sendMessage("servus"); // Ihr könnt auch einfach eure playerinstance nehmen
    } else { // Wenn kein Button gedrückt wurde -> return
        return;
    }
});
```

Und so mit haben wir eine ModalForm erstellt.

Wie ihr seht könnt ihr in nur 8 zeilen eine ModalForm erstellen ^^.
