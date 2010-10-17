# StaticMatic Starter!
*This is what I use when I start a new StaticMatic project.*

## Setup
**Cutting edge alert**: I'm using a prerelease version of StaticMatic for now. When it is released as stable, I'll update this.
If <code>gem -v</code> shows that you're already on ruby gems 1.3.6 or greater Simply run

    gem install staticmatic --pre

If your ruby gems version is behind, you'll need to update ruby gems first, then install StaticMatic as shown above.

    gem update --system

If you haven't already, you'll also need to install these gems:

    gem install fssm
    gem install compass
    gem install fancy-buttons

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