# You can SSM into ECS containers

You need to properly setup the task roles and also enable "execute-command" in
the service

It works for both EC2 an Fargate

Refs:
- https://docs.aws.amazon.com/en_us/AmazonECS/latest/userguide/ecs-exec.html

eg
```bash
export ECS_CONTAINER=my-container ECS_CLUSTER=my-cluster ECS_TASK_ID=some-task-id
aws ecs execute-command --cluster $ECS_CLUSTER --task $ECS_TASK_ID --container $ECS_CONTAINER --interactive --command "/bin/sh"
```

Tool to help debug errors:
https://github.com/aws-containers/amazon-ecs-exec-checker

Also be aware, if resources are too low, the "Managed Agent" might not be able
to start

> tags: aws; ecs;

> uid: 20220307151400Z

> links: 

