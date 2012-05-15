OmniAuth YouTube
================

This is an [OmniAuth 1.0](https://github.com/intridea/omniauth) strategy for authenticating to YouTube.

Get a Google Oauth2.0 API key at their [api console](https://code.google.com/apis/console/)

An example Rails application using omniauth is also available:
<https://github.com/jamiew/omniauth-rails-app>


Usage
-----

In a rack application:

```ruby
use OmniAuth::Builder do
  provider :youtube, ENV['YOUTUBE_KEY'], ENV['YOUTUBE_SECRET']
end
```

For Rails, put this in `config/initializers/omniauth.rb`:

```ruby
Rails.application.config.middleware.use OmniAuth::Builder do
  provider :youtube, ENV['YOUTUBE_KEY'], ENV['YOUTUBE_SECRET']
end
```


License
-------

Copyright (c) 2011 Jamie Wilkinson

This source code released under an MIT license.
