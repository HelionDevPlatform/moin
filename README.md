# Moin Moin Wiki

[http://moinmo.in/](http://moinmo.in/)

This is a out-of-the-box Moin Moin demo, that keeps all of it's data in HPE
Helion Stackato's persistent filesystem service.

If you are using this in production, you should make regular backups of the
filesystem directory, for example you can use `stackato run`:

  `stackato run rsync -rkvh wiki/ user:@backup:~/wiki`


Or more preferably, you can use [HPE Helion Stackato's cron feature](http://docs.stackato.com/deploy/stackatoyml.html?highlight=cron#cron)
to automate these backups, without needing to use the Stackato client.


## Deploying to HPE Helion Stackato

You should set your $MOIN_SECRET key in manifest.yml:

  `stackato push -n`


