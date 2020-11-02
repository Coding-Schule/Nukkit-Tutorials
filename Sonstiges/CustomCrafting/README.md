# Custom Crafting Recipe

Hier wirdst du sehen wie man ein Custom Crafting Recipe erstellt.
```java
ShapedRecipe recipe = new ShapedRecipe(result, shape, items, extraresults);
```

In diesen Tutorial werden wir ein enchantes Item als end produkt erhalten.

# End Produkt
```java
Item item = new Item(Item.STICK);
item.addEnchantment(Enchantment.get(Enchantment.ID_DAMAGE_ALL).setLevel(5, false));
item.setCustomName("§l§cSTICK");
```
Damit haben wir festgelegt welchen Item man am ende Bekommen soll.
Das Item wird Sharpness 5 haben und den name <br>*STICK*</br> in Rot.

# Shape
```java
String[] shape = new String[]{"DDD", "DGD", "DDD"};
```
*String[] shape = new String[]{"zeile1", "zeile2", "zeile3"};*

Damit haben wir die Shape festgelegt für das Recipe.
Überall wo nix hin soll haben wir ein leerzeichen gemacht.
Die *D* werden wir später durch ein Item replacen.

# Items
```java
Map<Character, Item> items = new HashMap<Character, Item>();
items.put('D', Item.get(Item.DIAMOND));
items.put('G', Item.get(Item.GOLD_BLOCK));
```
Hier replacen wir alle *D* durch ein Diamond und da *G* durch ein Goldblock.

# Extraresults
```java
List<Item> extraresults = new ArrayList<Item>();
```
Das können wir einglich leer lassen weil man ja kein extra result raus bekommen soll.
Ihr könnt hir ein extraresult rein machen wenn ihr z.B ein einmer zurück bekommen soll wenn man Lava craftet.

# Recipe
```java
ShapedRecipe recipe = new ShapedRecipe(item, shape, items, extraresults);
```
Somit haben wir und ein Custom Crafting Recipe gemacht aber es würde ja nicht gehen wenn wir das recipe nicht regestrieren würden und das
CraftingPacket nicht rebuilden würden.

# Recipe regestrieren und Packet rebuilen.
```java
this.getServer().getCraftingManager().registerRecipe(recipe);
this.getServer().getCraftingManager().rebuildPacket();
```