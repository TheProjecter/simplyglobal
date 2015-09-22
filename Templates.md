# Show views in the specified language #

## The view that will be used ##
The plugin will look for a template file called [action](action.md)_[language](language.md).html.erb._

```
class HomeController < ApplicationController
	# This will try to render the template 'home/index_fr.html.erb'
	# If it does not exist, it will render 'home/index.html.erb'
	def index
		SimplyGlobal.locale = :fr
	end
end
```

## The partial that will be used ##
It also works with the partial!