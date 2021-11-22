REGION := $(AWS_REGION)
VAULT := aws-vault exec $(AWS_PROFILE) --region $(REGION) --duration=1h --
CP_CMD := $(VAULT) aws s3 cp --recursive

.PHONY: deploy test

deploy:
	$(CP_CMD) ./src/ s3://devopsdreams.io/

test:
	$(CP_CMD) --dryrun ./src/ s3://devopsdreams.io/
