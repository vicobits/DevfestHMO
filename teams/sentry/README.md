BASADO EN: https://github.com/getsentry/onpremise

1. Descargar y ejecutar docker-compose.yml
2. Cambiar `SENTRY_SECRET_KEY` por algun hash
3. Ejecutar como demonio `docker-compose up -d`
4. Ejecutar `docker-compose exec base sentry upgrade` Esto crea la base de datos y un superusuario
5. (*Opcional*) Ejecutar `docker-compose exec sentry pip install sentry-slack` esto si quisieras agregar un pluggin
6. Ejecutar `docker-compose restart sentry` para reiniciar sentry
7. Sentry esta ejecutandose ahora en el puerto `900x`


* https://docs.docker.com/compose/compose-file/#env_file
* https://docs.docker.com/compose/compose-file/#depends_on

Lista de pluggins
===================================
* https://github.com/getsentry/sentry-redmine - Sentry integration for creating Redmine issues
* https://github.com/getsentry/sentry-github - Sentry extension which integrates with GitHub
* https://github.com/getsentry/sentry-phabricator - Sentry extension which integrates with Phabricator
* https://github.com/getsentry/sentry-pagerduty - Sentry plugin for integrating with PagerDuty
* https://github.com/getsentry/sentry-teamwork - Sentry plugin that integrates with Teamwork
* https://github.com/getsentry/sentry-heroku - Sentry extension which integrates Heroku release tracking
* https://github.com/getsentry/sentry-freight - Sentry extension which integrates with Freight release tracking
* https://github.com/getsentry/sentry-youtrack - Sentry extension which integrates with YouTrack
* https://github.com/getsentry/sentry-bitbucket - Sentry extension which integrates with Bitbucket
* https://github.com/getsentry/sentry-jira - Plugin for sentry that lets you create JIRA issues
* https://github.com/getsentry/sentry-irc - Plugin for Sentry that logs errors to an IRC room
* https://github.com/getsentry/sentry-trello - Plugin for Sentry that creates cards on a Trello board
* https://github.com/getsentry/sentry-campfire - Sentry plugin for sending notifications to Campfire
* https://github.com/getsentry/sentry-groveio - Plugin for Sentry that logs errors to an IRC room on Grove.io
* https://github.com/getsentry/sentry-irccat - Plugin for Sentry which sends errors to irccat (or any other service which supports irccat's simple socket-based protocol)
* https://github.com/getsentry/sentry-slack - Slack integration for Sentry

Integración de pluggins
=========================
* https://github.com/linovia/sentry-hipchat - Sentry plugin that integrates with Hipchat
* https://github.com/butorov/sentry-telegram - Plugin for Sentry which allows sending notification via Telegram messenger
* https://github.com/mattrobenolt/sentry-twilio - A plugin for Sentry that sends SMS notifications via Twilio
* https://github.com/Banno/getsentry-kafka - An Apache Kafka plugin for Sentry