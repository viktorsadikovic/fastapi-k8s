Inside the [docker-compose](docker/docker-compose.yaml) file you have the following containers/services defined: 

- <b>backend</b>: atanastrpceski/fastapi
- <b>celeryworker</b>: atanastrpceski/fastapi-worker.<br/>
- <b>db: postgres:13.4</b>: A postgres db that is needed for all of this to work.<br/>
- <b>adminer: adminer</b>: A web UI for postgres.<br/>
- <b>queue: rabbitmq:3-management</b>: RabbitMQ queue needed for the backend / celeryworker to communicate between each other.<br/>
- <b>flower: mher/flower</b>: A web UI for Celery, so you can see your job progress.<br/>
- <b>mailhog: mailhog/mailhog</b>. A dummy SMTP server, very convenient for testing.<br/>

You need to expose the folloing services to the ouside world:

- [backend](images/backend.png)<br/>
- [adminer](images/adminer.png)<br/>
- [flower](images/flower.png)<br/>
- [mailhog](images/mailhog.png)