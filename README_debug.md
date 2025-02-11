# Bug 1
- when running `bundle install` with errors like
```bash
Gem::Ext::BuildError: ERROR: Failed to build gem native extension.
current directory: /home/........../zelun_code/zelunli.github.io/vendor/bundle/ruby/3.0.0/gems/json-2.10.1/ext/json/ext/generator
/usr/bin/ruby3.0 -I /usr/lib/ruby/vendor_ruby -r ./siteconf20250211-7408-hadsik.rb extconf.rb
checking for whether -std=c99 is accepted as CFLAGS... *** extconf.rb failed ***
Could not create Makefile due to some reason, probably lack of necessary
libraries and/or headers.  Check the mkmf.log file for more details.  You may
need configuration options.
```

- solution:
```bash
$ cd APP_ROOT
$ su
# apt install rbenv
# rbenv global
# gem install bundler
# rbenv rehash
# gem clean
$ bunlde install
# taken from 
# https://stackoverflow.com/questions/57948886/an-error-occurred-while-installing-commonmarker-0-17-13-and-bundler-cannot-co

# Switches to the root user to perform administrative tasks.

# Installs rbenv to manage Ruby versions.

# Checks the current global Ruby version.

# Installs Bundler to manage Ruby project dependencies.

# Updates rbenv shims to recognize newly installed executables.

# Cleans up old or unused gem versions to free up space.
```

