# Sample plugin for Bridgetown

_NOTE: This isn't a real plugin! Copy this sample code and use it to create your own Ruby gem! [Help guide here…](https://www.bridgetownrb.com/docs/plugins)_ 😃

A Bridgetown plugin to [fill in the blank]…

## Installation

Run this command to add this plugin to your site's Gemfile:

```shell
$ bundle add my-awesome-plugin -g bridgetown_plugins
```

## Usage

The plugin will…

### Optional configuration options

The plugin will automatically use any of the following metadata variables if they are present in your site's `_data/site_metadata.yml` file.

…

## Testing

- Run `bundle exec rspec` to run the test suite
- Or run `script/cibuild` to validate with Rubocop and test with rspec together.

## Contributing

1. Fork it (https://github.com/username/my-awesome-plugin/fork)
2. Clone the fork using `git clone` to your local development machine.
3. Create your feature branch (`git checkout -b my-new-feature`)
4. Commit your changes (`git commit -am 'Add some feature'`)
5. Push to the branch (`git push origin my-new-feature`)
6. Create a new Pull Request

---

## Releasing (you can delete this section in your own plugin repo)

To release a new version of the plugin, simply bump up the version number in both `version.rb` and
`package.json`, and then run `script/release`. This will require you to have a registered account
with both the [RubyGems.org](https://rubygems.org) and [NPM](https://www.npmjs.com) registries.
You can optionally remove the `package.json` and `frontend` folder if you don't need to package frontend
assets for Webpack.

If you run into any problems or need further guidance, please check out our [Bridgetown community resources](https://www.bridgetownrb.com/docs/community)
where friendly folks are standing by to help you build and release your plugin or theme.

**NOTE:** make sure you add the `bridgetown-plugin` [topic](https://github.com/topics/bridgetown-plugin) to your
plugin's GitHub repo so the plugin or theme will show up on [Bridgetown's official Plugin Directory](https://www.bridgetownrb.com/plugins)! (There may be a day or so delay before you see it appear.)

## Usage

```bash
mkdir mysite
cd mysite
touch Gemfile
```

Add the following to your Gemfile:

```ruby
gem "bridgetown", "~> 0.15.0.beta"
```

Now go back to the terminal and run:

```bash
bundle install
bundle exec bridgetown new . --force
bundle add bridgetown-plugin-tailwindcss -g bridgetown_plugins
bundle exec bridgetown tailwind init
```

```ruby
# Gemfile

# ...
group :bridgetown_plugins do
  # ...
  gem "bridgetown-plugin-tailwindcss", "~> 0.1.13"
end
```

## Testing

Right now there is one big integration tests which is run via simple:

```bash
bundle install
rake test
```

## Issues

Right now, the script does not do a smart replace of
`webpack.config.js`. If you have a webpack config different from the
stock version of Bridgetown it will be replaced with the default
bridgetown version with a PostCss loader.
