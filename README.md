## Circle CI Config for Automated AWS ECR / ECS deploy

This config is setup for Node and Postgres but can simply switch the images needed to get your own configuration.

This script uses https://github.com/silinternational/ecs-deploy - check the docs to understand how to setup this layer so you can directly create a new task definition revision + update it.

AWS deploys only occur on Master and Staging branches, after a successful test suite.

AWS ECR Docker images are tagged via the current commit GitHash.

After a successful ECR docker image, ecs-deploy updates your task revision and service.

### Assumptions

This is a just a skeleton so feel free to change any aspect.

The config file expects an initTestDb shell script, expects use of Node, Postgres, yarn, and more.
