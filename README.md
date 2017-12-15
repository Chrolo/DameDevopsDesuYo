# Dame DevOps Desu Yo

I needed a dev test server for my DDY stuff, but I wanted it to be repeatable in it's deployment, so here's a Vagrant managed VM with Ansible configuration.

Just make sure you have `Vagrant` on your host machine, and then fire off a `vagrant up`.

## What it does:
- creates a VM called `DameDevOpsDesuYo`
  - it's based on the vagrant standard ubuntu image, so it's headless and cli only
- Runs Ansible to configure the VM
  - installs `mysql-server`
    - configures a `subpar` user
    - creates the `subpar` database
  - Installs `nodejs` v8.x
  - Downloads `subpar-project-tracker` and `Mysql-db-builder` projects from Chrolo's github

## What should I do?
throw a `vagrant up` command into a terminal. Then maybe a `vagrant ssh`. Then maybe setup the system with some example data. Then fire up the `subpar-project-tracker`, as explained in it's README