# Flask app

Ansible recipe to deploy Flask application. This recipe does not trying to
define your production infrastructure and just:

- Install required system packages to serve python application
- Run pre deploy hooks
- Checkout the latest source code
- Install required application dependencies via `pip`, `npm` (optional) and
  `bower` (optional)
- Run post deploy hooks
- Copy custom application config to remote server.


## Role Variables

| Option               | Description                                          |
|----------------------|------------------------------------------------------|
| `app_name`           | The name of the application, uses to create application directory, e.g. should be a shorthand, lowercase and not contain any whitespaces, e.g. `app`. |
| `app_user`           | The user to run application, e.g. `{{ app_name }}`. |
| `app_directory`      | The directory to keep application source code, e.g. `/home/{{ app_user }}/{{ app_name }}`. |
| `app_log_directory`  | The directory to keep application logs if any. |
| `app_requirements`   | The path to application requirements, e.g. `{{ app_directory }}/requirements.txt`. |
| `app_repository`     | The remote git repository to pull application code from, e.g. `ssh://git@github.com/vitalk/flaskapp.git`. |
| `app_version`        | The version of the repository to checkout. This can be a full 40-character SHA1 hash, a branch or a tag name, e.g. `master`. |
| `app_environment`    | The list of environment variables uses to run most of commands. |
| `app_pre_hooks`      | The list of custom commands to run before deploy. These commands uses previously defined environment to run. |
| `app_post_hooks`     | The list of custom commands to run after deploy. |
| `app_config`         | The path to application config to use when launch application. |
| `app_packages`       | The list of system packages required to build/run application. |
| `app_requires_npm`   | Install `nodejs` and required package dependencies via `npm`? Nope. |
| `app_requires_bower` | Install required frontend dependencies via `bower`? Nope. |


## License

Licensed under the [MIT license](http://mit-license.org/vitalk).


## Self-Promotion

Created by Vital Kudzelka.

Open [a GitHub issue](https://github.com/vitalk/ansible-flask-app/issues) if
you have any suggestion or found a bug.
