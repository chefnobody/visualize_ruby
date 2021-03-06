# VisualizeRuby

Write a Ruby class and see method interactions. Works with procedural code and bare methods.</span>
This is experimental project and does not support all types of code. 
If you'd like it to support more types of code please pull request.

[Demo](https://visualize-ruby.herokuapp.com/)

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'visualize_ruby'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install visualize_ruby

## Usage

```ruby
require "visualize_ruby"

ruby_code = <<-RUBY
  if hungry?
    eat
  else
    work
  end
RUBY

results = VisualizeRuby::Builder.new(ruby_code: ruby_code).build
VisualizeRuby::Graphviz.new(*results).to_graph(png: "example.png")
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/visualize_ruby. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the VisualizeRuby project’s codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/[USERNAME]/visualize_ruby/blob/master/CODE_OF_CONDUCT.md).
