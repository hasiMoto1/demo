
EB_ENVIRONMENT=$(aws cloudformation describe-stack-resources --stack-name devsecops-workshop-elasticbeanstalk | jq '.StackResources[] | select(.ResourceType=="AWS::ElasticBeanstalk::Environment").PhysicalResourceId' | tr -d '[\"\n]')

EB_APPLICATION=$(aws cloudformation describe-stack-resources --stack-name devsecops-workshop-elasticbeanstalk | jq '.StackResources[] | select(.ResourceType=="AWS::ElasticBeanstalk::Application").PhysicalResourceId' | tr -d '[\"\n]')

EB_URL=$(aws cloudformation describe-stacks --stack-name devsecops-workshop-elasticbeanstalk | jq '.Stacks[].Outputs[] | select(.OutputKey=="EBEndPointURL").OutputValue' | tr -d '[\"\n]')
