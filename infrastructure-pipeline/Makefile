ifndef INFRA_STACK_NAME
$(error INFRA_STACK_NAME is not set)
endif
include infra.env

SHELL := /bin/bash

INFRA_PIPELINE_NAME=$(INFRA_STACK_NAME)-pipeline

all: pipeline
pipeline:
	aws cloudformation deploy    \
      --stack-name $(INFRA_PIPELINE_NAME)   \
      --template-file infra-cfn-pipeline.yml    \
      --capabilities CAPABILITY_NAMED_IAM   \
      --parameter-overrides     \
        InfraStackName=$(INFRA_STACK_NAME) \
        GithubRepo=$(GITHUB_REPO)


delete-all: delete-pipeline
delete-infra-stack:
	./delete-stack-wait-termination.sh $(INFRA_STACK_NAME)
delete-pipeline: delete-infra-stack
	./delete-stack-wait-termination.sh $(INFRA_PIPELINE_NAME)