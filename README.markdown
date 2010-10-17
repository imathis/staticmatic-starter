# StaticMatic Starter!
*This is what I use when I start a new StaticMatic project.*

## Setup
This project is now using bundler and an RVM gem sets. This means setup is as simple as opening the console to the project directory and:

<pre><code>
  rvm gemset create 'staticmatic-starter'
  bundle install
</code></pre>

**Note:** If you're not using RVM, you can still install the gems with bundler using `bundle install`. RVM gem sets are great because they let you
isolate your gem libraries per project.

## Compass Configuration

Now StaticMatic automatically detects the compass configuration and loads in your settings from /config/compass.rb. I currently have my
configuration set such that <code>relative_assets = true</code> I often deploy to subdirectories on a development server to share my static prototypes.
If you are deploying to root directories, you will probably want to comment out the relative_assets line or remove it.

## Goodies
- <code>rake build</code> builds the site
- <code>rake watch</code> watches your project directory and automatically recompiles the site as you change files
- <code>rake push</code> deploys the site (via rsync) to your remote server (based on your configurations in the rakefile)
- <code>rake deploy</code> runs build and then push


That's about it, pretty simple really.