# Dredd + Rails test

1. Run `bundle install`
2. Install dredd `npm install dredd -g`
3. Start rails server with `rails s`
4. Run `dredd fails.md http://localhost:3000`
5. You'll see a 400 bad request in the Rails logs.

This happens most likely due to [how Rails parses json][ref1].

Rails [seems to rely][ref2] on the `Content-Length` http header being set.

[ref1]: https://github.com/rails/rails/blob/master/actionpack/lib/action_dispatch/middleware/params_parser.rb#L44
[ref2]: https://github.com/rails/rails/blob/5f3b40e824cce3f6dcdfac63fa47bcd80d67dd5a/actionpack/lib/action_dispatch/http/request.rb#L185

Maybe Dredd should add the `Content-Length` header?


## Successful example

1. Run `dredd success.md http://localhost:3000`
2. You'll see a 201 created in the Rails logs.
