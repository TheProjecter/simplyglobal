  1. Execute ./script/plugin install http://simplyglobal.googlecode.com/svn/trunk/simplyglobal
  1. Create a file named _simplyglobal.rb_ in the _config/initializers_ directory
  1. In _simplyglobal.rb_, create hashes of language
```
# français
fr = {
    "hi" => "bonjour",
    "welcome" => "bienvenue"  
}

# espanol
es = {
    "hi" => "hola",
    "welcome" => "bienvenida"
}
```
  1. Add the language hashes to the object
```
SimplyGlobal.add_language_hash(:fr, fr)
SimplyGlobal.add_language_hash(:es, es)
```

You will end up with a file named _simplyglobal.rb_ that looks like this :
```
# français
fr = {
    "hi" => "bonjour",
    "welcome" => "bienvenue"  
}

# espanol
es = {
    "hi" => "hola",
    "welcome" => "bienvenida"
}

SimplyGlobal.add_language_hash(:fr, fr)
SimplyGlobal.add_language_hash(:es, es)
```

In **development**, this file will be loaded every request. In **production**, it is loaded once.