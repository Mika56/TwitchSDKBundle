TwitchSDKBundle
===============

This bundle provides a simple integration of the "[TwitchSDK](https://github.com/jofner/Twitch-SDK)" from "[Josef Ohnheiser](https://github.com/jofner)" into Symfony2.

    <?php
    $twitch_api = $this->get('twitch');

##Installation
### Step 1: Composer require
    $ php composer.phar require "mika56/twitch-sdk-bundle":"dev-master"

### Step 2: Enable the bundle in the kernel
    <?php
    // app/AppKernel.php

    public function registerBundles()
    {
        $bundles = array(
            // ...
            new Mika56\TwitchSDKBundle\Mika56TwitchSDKBundle(),
            // ...
        );
    }

### Step 3: Add parameters
TwitchSDKBundle requires you to add some parameters in your parameters.yml file.
You can either add "no configuration" (API calls will be anonymous) or specify your client_id, client_secret and redirect_uri:

    // app/config/parameters.yml
    twitch_settings: ~
or

    // app/config/parameters.yml
    twitch_settings:
      client_id: "your_twitch_app_client_id"
      client_secret: "your_twitch_app_client_secret"
      redirect_uri: "your_twitch_app_redirect_uri"

That's it!