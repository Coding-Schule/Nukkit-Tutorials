# Modal Form

HIer wirdst du lernen wie du eine ModalForm hast.

Eine Modalform ist einglich genauso wie eine Simpleform aber bei einer Modalform hast du nur 2 button zur auswahl.



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

Und so mit haben wir eine ModalForm.

Wie ihr seht könnt ihr in nur 8 zeilen eine ModalForm machen ^^.