# Ruby::Cakemail

Use CakeMail service with Rails ActionMailer
http://cakemail.com

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'ruby-cakemail'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install ruby-cakemail

## Usage

```
CAKEMAIL_SETTINGS = {
  :interface_key => INTERFACE_KEY,
  :interface_id => INTERFACE_ID,
  :email => EMAIL,
  :password => PASSWORD
}

ActiveSupport.on_load :action_mailer do
  ActionMailer::Base.add_delivery_method :cake_mail, CakeMail::Delivery
end

ActionMailer::Base.delivery_method = :cake_mail
```

## Contributing

1. Fork it ( https://github.com/[my-github-username]/ruby-cakemail/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
