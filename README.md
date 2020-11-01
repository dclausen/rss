# rss

RSS parser for Crystal

## Installation

Add this to your application's `shard.yml`:

```yaml
dependencies:
  rss:
    github: ruivieira/rss
```

## Usage

```crystal
require "rss"

feed = RSS.parse "https://news.ycombinator.com/rss"

feed.items.each do |e|
  str = "title: #{e.title}\nlink: #{e.link}\npubDate: #{e.pubDate}\n"
  str += "description: #{e.description}\ncomments: #{e.comments}\n"
  puts str
end
```

Warning:

- Pre-release (API will break)

## Contributing

1. Fork it ( https://github.com/ruivieira/rss/fork )
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create a new Pull Request

## Contributors

- [ruivieira](https://github.com/ruivieira) Rui Vieira - creator, maintainer
- [modsognir](https://github.com/modsognir) modsognir - contributor
- [data-niklas](https://github.com/data-niklas) data-niklas - contributor
- [MineBartekSA](https://github.com/MineBartekSA) - contributor
