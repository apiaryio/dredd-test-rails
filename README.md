# Dredd + Rails example

1. Run `bundle install && rake db:migrate`
2. Install dredd `npm install dredd -g`
3. Start rails server with `rails s`
4. Run `$ dredd apiary.apib http://localhost:3000`
5. You'll see a 201 created in the Rails logs.

6. Tests will pas and exit status will be `0` :
   
   ```
   $ echo $?
   0
   ```


