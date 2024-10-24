<!-- DO NOT EDIT THIS FILE! -->
<!-- Instead edit contrib/rollbar.php -->
<!-- Then run bin/docgen -->

# Rollbar Recipe

```php
require 'contrib/rollbar.php';
```

[Source](/contrib/rollbar.php)



## Configuration
- `rollbar_token` – access token to rollbar api
- `rollbar_comment` – comment about deploy, default to
  ```php
  set('rollbar_comment', '_{{user}}_ deploying `{{what}}` to *{{where}}*');
  ```
- `rollbar_username` – rollbar user name
## Usage
Since you should only notify Rollbar channel of a successful deployment, the `rollbar:notify` task should be executed right at the end.
```php
after('deploy', 'rollbar:notify');
```


## Configuration
### rollbar_comment
[Source](https://github.com/deployphp/deployer/blob/master/contrib/rollbar.php#L27)



```php title="Default value"
'_{{user}}_ deploying `{{what}}` to *{{where}}*'
```



## Tasks

### rollbar\:notify {#rollbar-notify}
[Source](https://github.com/deployphp/deployer/blob/master/contrib/rollbar.php#L30)

Notifies Rollbar of deployment.




