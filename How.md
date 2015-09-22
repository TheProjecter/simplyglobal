First thing to do is to set the **locale** that is global to the object

```
SimplyGlobal.locale = :fr
```

**Watch out!** You have to set it to `nil` at the beginning of each request. I suggest you to use a `before_filter` in your `ApplicationController`

To translate a string, just use the `t` method of the `string` object.

```
"welcome".t # will become "bienvenue"
```

You can also use replacement characters

```
"welcome %s".t("Johnny") # will become "Bienvenue Johnny"
```


You can specify the language too

```
"welcome".t(:fr) # returns "Bienvenue"
```

or use `:all` if you want an `hash` of all languages

```
"welcome".t(:all) # will return {:fr => "bienvenue", :es => "bienvenidos"}
```