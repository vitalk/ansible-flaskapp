# Flask app

Ansible recipe to deploy Flask application. This recipe does not trying to
define your production infrastruncture and just:

- Install required system packages to serve python application
- Run pre deploy hooks
- Checkout the latest source code
- Install required application dependencies via `pip`, `npm` and `bower`
- Run post deploy hooks
- Copy custom application config to remote server.


## License

Licensed unser the [MIT license](http://mit-license.org/vitalk).


## Self-Promotion

Created by Vital Kudzelka.

Open [a GitHub issue](https://github.com/vitalk/ansible-flask-app/issues) if
you have any suggestion or found a bug.
