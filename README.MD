#Discord log target for Yii2

This is the PHP [Yii2](https://github.com/yiisoft/yii2) plugin for sending log of a yii application through the Discord [WebHook API](https://support.discordapp.com/hc/en-us/articles/228383668-Intro-to-Webhooks).

###Important
You should avoid to use this target on a frequent events because of restriction in 30 messages per 60 seconds for the web-hooks.

##Installation

Execute following command in shell:
```shell
composer require betsuno/yii2-log-discord-target
```

Or add following in your `composer.json` require section, and run `composer install` in your shell
```
"betsuno/yii2-log-discord-target": "*"
```

##Configuration and usage

Add something as following in your yii config into the `components` section
```
'log' => [
    'class'     => '\betsuno\yii\log\DiscordTarget',
    'url'       => 'WEBHOOK_URL',                 // Your WebHook URL
    //'pattern' => "{category}: {level}\n{text}", // Optionally you can override default message pattern
]
```

More info about log targets may be found [here](https://www.yiiframework.com/doc/guide/2.0/en/runtime-logging#log-targets)
