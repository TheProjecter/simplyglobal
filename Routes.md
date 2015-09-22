You have to set the locale in `SimplyGlobal.locale` at every request. I suggest you creating a `before_filter` in your `ApplicationController` that sets the locale.

**application.rb**
```
class ApplicationController < ActionController::Base
	before_filter :set_locale

	private
		
	# Set the locale
	def set_locale	
		SimplyGlobal.locale = params[:locale]
	end
end
```

Then, create a connection that uses a `locale`. In the above example, we could write URLs like `fr/home/index`.

**routes.rb**
```
map.connect "/:locale/:controller/:action/:id"
	:requirements => {
		:locale => /fr/es/
	}
```