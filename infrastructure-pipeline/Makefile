SHELL := /bin/bash
ifndef INFRASTRUCTURE_NAME
$(error INFRASTRUCTURE_NAME is not set)
endif
include infra.env

pipeline:
	aws cloudformation deploy    \
      --stack-name $(INFRASTRUCTURE_NAME)-cfn-pipeline   \
      --template-file infra-cfn-pipeline.yml    \
      --capabilities CAPABILITY_NAMED_IAM   \
      --parameter-overrides     \
        InfrastructureName=$(INFRASTRUCTURE_NAME) \
        GithubRepo=$(GITHUB_REPO)