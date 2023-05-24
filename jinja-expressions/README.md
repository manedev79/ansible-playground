# jinja-expressions

See what happens with expression blocks like `{% if with_messaging %}` in jinja template. Renders the `=> Conditional Text <=` block when `with_messaging` is boolean `true`.

## Run

`ansible-playbook play.yml` => with_messaging=null => false

`ansible-playbook -e with_messaging=false play.yml` => false

`ansible-playbook -e with_messaging=true play.yml` => true

## Learning

* Setting extra var results in string!
* Must use boolean filter when using value: `with_messaging|bool`.
