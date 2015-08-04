---
title: API Reference

language_tabs:
  - shell
  - ruby

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - users
  - errors

search: true
---

# Introduction

Welcome to the Jellytelly API! You can use our API to access Jellytelly API endpoints, which can get information on various users, videos, and series in our database.

We have language bindings in Shell, Ruby! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.


# Authentication

> To authorize, use this code:

```ruby
class ApplicationController < ActionController::Base
  ...

  before_action :set_auth_token

  def set_auth_token
    Jellytelly.auth_token = session[:user_token] if session[:user_token].present?
  end

  ...
end

class Jellytelly < ActiveRestClient::Base
  mattr_accessor :auth_token

  before_request :add_authentication_details

  def add_authentication_details(name, request)
    request.headers["Authorization"] = "Token token=\"#{auth_token}\"" unless auth_token.nil?
  end
end
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H 'Authorization: Token token="auth_token"'
```

> Make sure to replace `auth_token` with your auth_token returned from user login.

Jellytelly uses auth_tokens to allow access to the API. You can retrieve a new Jellytelly auth_token by signing up or logging in.

Jellytelly expects for the auth_token to be included in all API requests to the server in a header that looks like the following:

`Authorization: Token token="auth_token"`

<aside class="notice">
You must replace <code>auth_token</code> with the user auth_token.
</aside>
