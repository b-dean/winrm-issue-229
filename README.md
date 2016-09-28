This cookbook is an example of test-kitchen not giving the correct exit status for chef-solo

to use:

    bundle install
    bundle exec kitchen test
    echo $?

I would not expect the exit status of kitchen to be `0` since the tests failed.

if you change the Gemfile to have

    gem 'test-kitchen', '~> 1.7.0'
    gem 'winrm-fs', '~> 0.4'
    
Then the exit status is the expected `10`
