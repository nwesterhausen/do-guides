# Scheduling Jobs and Scripts

There are a couple ways to schedule scripts and automated jobs on Linux:

- [cron](#cron) - a very simple scheduler
- [systemd](#systemd) - allows for more complexity with scheduled jobs

## cron

cron runs based off of a text file stored on your system. That file has two parts:

1. [when](#cron-when-statements) to run the job
2. the job in question (e.g. `/usr/bin/node /opt/jobs/check-api.js`)

Each line in a cron file is arranged like this:

`[when] [what]`

and that in practice looks like this

`0 0 * * * *    /usr/bin/node /opt/jobs/check-api.js`

To add to the cron table, use command `crontab -e` which will open up an editor
in the cron table. You can add your job. As soon as you add the job, it will be
run by cron once its conditions are met. In the example listed above, nodejs will
execute the `check-api.js` script every hour on the hour.

#### How do I find the executable path?

Use the command `which <program-name>` and it will give you the path to use.

### cron 'when' statements

See [cron expression](https://en.wikipedia.org/wiki/Cron#CRON_expression) and a
[generator](https://www.freeformatter.com/cron-expression-generator-quartz.html)

A couple examples:

- `0 */15 * * * *`: every 15 minutes
- `0 0 12 * * SUN,SAT`: Every Saturday and Sunday at noon

## systemd

