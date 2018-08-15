# App settings

Much of the configuration of the app is stored in the database in a document with id "settings". To update settings use the [medic-conf](https://github.com/medic/medic-conf) command line tool.

For more details on what you can use in settings, check out the [superset of supported settings](https://github.com/medic/medic-webapp/blob/master/config/standard/app_settings.json).

### Optional Settings (^3.1)

The following settings do not need to be specified. They should only be defined when the default implementation needs to be changed.

| Setting              | Default | Allowed Values      | Description |
|----------------------|---------|---------------------|-------------|
|phone_validation      | full    | full<br/>partial<br/>none | <b>full</b> - full validation of a phone number for a region using length and prefix information.<br/><b>partial</b> - quickly guesses whether a number is a possible phone number by using only the length information, much faster than a full validation.<br/><b>none</b> - allows almost any values but still fails for any phone that contains a-z chars. |