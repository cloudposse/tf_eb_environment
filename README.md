<!-- This file was automatically generated by the `build-harness`. Make all changes to `README.yaml` and run `make readme` to rebuild this file. -->


[![Cloud Posse](https://cloudposse.com/logo-300x69.svg)](https://cloudposse.com)

# terraform-aws-elastic-beanstalk-environment

 [![Build Status](https://travis-ci.org/cloudposse/terraform-aws-elastic-beanstalk-environment.svg?branch=master)](https://travis-ci.org/cloudposse/terraform-aws-elastic-beanstalk-environment) [![Latest Release](https://img.shields.io/github/release/cloudposse/terraform-aws-elastic-beanstalk-environment.svg)](https://github.com/cloudposse/terraform-aws-elastic-beanstalk-environment/releases/latest) [![Slack Community](https://slack.cloudposse.com/badge.svg)](https://slack.cloudposse.com)


Terraform module to provision AWS Elastic Beanstalk environment


---

This project is part of our comprehensive ["SweetOps"](https://docs.cloudposse.com) approach towards DevOps. 


It's 100% Open Source and licensed under the [APACHE2](LICENSE).










## Usage

Complete example: [examples/complete](examples/complete)






## Makefile Targets
```
Available targets:

  help                                Help screen
  help/all                            Display help for all targets
  help/short                          This help short screen
  lint                                Lint terraform code

```

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| alb_zone_id | ALB zone id | map | `<map>` | no |
| app | EBS application name | string | - | yes |
| associate_public_ip_address | Specifies whether to launch instances in your VPC with public IP addresses. | string | `false` | no |
| attributes | Additional attributes (e.g. `1`) | list | `<list>` | no |
| autoscale_lower_bound | Minimum level of autoscale metric to remove an instance | string | `20` | no |
| autoscale_lower_increment | How many Amazon EC2 instances to remove when performing a scaling activity. | string | `-1` | no |
| autoscale_max | Maximum instances in charge | string | `3` | no |
| autoscale_measure_name | Metric used for your Auto Scaling trigger | string | `CPUUtilization` | no |
| autoscale_min | Minumum instances in charge | string | `2` | no |
| autoscale_statistic | Statistic the trigger should use, such as Average | string | `Average` | no |
| autoscale_unit | Unit for the trigger measurement, such as Bytes | string | `Percent` | no |
| autoscale_upper_bound | Maximum level of autoscale metric to add an instance | string | `80` | no |
| autoscale_upper_increment | How many Amazon EC2 instances to add when performing a scaling activity | string | `1` | no |
| availability_zones | Choose the number of AZs for your instances | string | `Any 2` | no |
| config_document | A JSON document describing the environment and instance metrics to publish to CloudWatch. | string | `{ "CloudWatchMetrics": {}, "Version": 1}` | no |
| config_source | S3 source for config | string | `` | no |
| delimiter | Delimiter to be used between `name`, `namespace`, `stage`, etc. | string | `-` | no |
| enable_managed_actions | Enable managed platform updates.<br><br>When you set this to true, you must also specify a PreferredStartTime and UpdateLevel. | string | `true` | no |
| env_default_key | Default ENV variable key for Elastic Beanstalk `aws:elasticbeanstalk:application:environment` setting | string | `DEFAULT_ENV_%d` | no |
| env_default_value | Default ENV variable value for Elastic Beanstalk `aws:elasticbeanstalk:application:environment` setting | string | `UNSET` | no |
| env_vars | Map of custom ENV variables to be provided to the Jenkins application running on Elastic Beanstalk, e.g. `env_vars = { JENKINS_USER = 'admin' JENKINS_PASS = 'xxxxxx' }` | map | `<map>` | no |
| force_destroy | Destroy S3 bucket for load balancer logs | string | `false` | no |
| health_streaming_delete_on_terminate | Whether to delete the log group when the environment is terminated. If false, the health data is kept RetentionInDays days. | string | `false` | no |
| health_streaming_enabled | For environments with enhanced health reporting enabled, whether to create a group in CloudWatch Logs for environment health and archive Elastic Beanstalk environment health data. For information about enabling enhanced health, see aws:elasticbeanstalk:healthreporting:system. | string | `false` | no |
| health_streaming_retention_in_days | The number of days to keep the archived health data before it expires. | string | `7` | no |
| healthcheck_url | Application Health Check URL. Elastic Beanstalk will call this URL to check the health of the application running on EC2 instances | string | `/healthcheck` | no |
| http_listener_enabled | Enable port 80 (http) | string | `false` | no |
| instance_refresh_enabled | Enable weekly instance replacement. | string | `true` | no |
| instance_type | Instances type | string | `t2.micro` | no |
| keypair | Name of SSH key that will be deployed on Elastic Beanstalk and DataPipeline instance. The key should be present in AWS | string | - | yes |
| loadbalancer_certificate_arn | Load Balancer SSL certificate ARN. The certificate must be present in AWS Certificate Manager | string | `` | no |
| loadbalancer_managed_security_group | Load balancer managed security group | string | `` | no |
| loadbalancer_security_groups | Load balancer security groups | list | `<list>` | no |
| loadbalancer_type | Load Balancer type, e.g. 'application' or 'classic' | string | `classic` | no |
| name | Solution name, e.g. 'app' or 'jenkins' | string | `app` | no |
| namespace | Namespace, which could be your organization name, e.g. 'eg' or 'cp' | string | - | yes |
| nodejs_version | Elastic Beanstalk NodeJS version to deploy | string | `` | no |
| notification_endpoint | Notification endpoint | string | `` | no |
| notification_protocol | Notification protocol | string | `email` | no |
| notification_topic_arn | Notification topic arn | string | `` | no |
| notification_topic_name | Notification topic name | string | `` | no |
| preferred_start_time | Configure a maintenance window for managed actions in UTC | string | `Sun:10:00` | no |
| private_subnets | List of private subnets to place EC2 instances | list | - | yes |
| public_subnets | List of public subnets to place Elastic Load Balancer | list | - | yes |
| rolling_update_type | Set it to Immutable to apply the configuration change to a fresh group of instances | string | `Health` | no |
| root_volume_size | The size of the EBS root volume | string | `8` | no |
| root_volume_type | The type of the EBS root volume | string | `gp2` | no |
| security_groups | List of security groups to be allowed to connect to the EC2 instances | list | - | yes |
| solution_stack_name | Elastic Beanstalk stack, e.g. Docker, Go, Node, Java, IIS. [Read more](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/concepts.platforms.html) | string | `` | no |
| ssh_listener_enabled | Enable ssh port | string | `false` | no |
| ssh_listener_port | SSH port | string | `22` | no |
| ssh_source_restriction | Used to lock down SSH access to the EC2 instances. | string | `0.0.0.0/0` | no |
| stage | Stage, e.g. 'prod', 'staging', 'dev', or 'test' | string | - | yes |
| tags | Additional tags (e.g. `map('BusinessUnit`,`XYZ`) | map | `<map>` | no |
| tier | Elastic Beanstalk Environment tier, e.g. ('WebServer', 'Worker') | string | `WebServer` | no |
| update_level | The highest level of update to apply with managed platform updates | string | `minor` | no |
| updating_max_batch | Maximum count of instances up during update | string | `1` | no |
| updating_min_in_service | Minimum count of instances up during update | string | `1` | no |
| version_label | Elastic Beanstalk Application version to deploy | string | `` | no |
| vpc_id | ID of the VPC in which to provision the AWS resources | string | - | yes |
| wait_for_ready_timeout |  | string | `20m` | no |
| zone_id | Route53 parent zone ID. The module will create sub-domain DNS records in the parent zone for the EB environment | string | `` | no |

## Outputs

| Name | Description |
|------|-------------|
| all_settings | List of all option settings configured in the environment. These are a combination of default settings and their overrides from setting in the configuration. |
| application | The Elastic Beanstalk Application specified for this environment. |
| autoscaling_groups | The autoscaling groups used by this environment. |
| cname | Fully qualified DNS name for the environment. |
| description | Description of the Elastic Beanstalk environment. |
| ec2_instance_profile_role_name | Instance IAM role name |
| elb_dns_name | ELB technical host |
| elb_zone_id | ELB zone id |
| host | DNS hostname |
| id | ID of the Elastic Beanstalk environment. |
| instances | Instances used by this environment. |
| launch_configurations | Launch configurations in use by this environment. |
| load_balancers | Elastic Load Balancers in use by this environment. |
| name | Name |
| queues | SQS queues in use by this environment. |
| security_group_id | Security group id |
| setting | Settings specifically set for this environment. |
| tier | The environment tier specified. |
| triggers | Autoscaling triggers in use by this environment. |




## Related Projects

Check out these related projects.

- [terraform-aws-jenkins](https://github.com/cloudposse/terraform-aws-jenkins) - Terraform module to build Docker image with Jenkins, save it to an ECR repo, and deploy to Elastic Beanstalk running Docker stack
- [terraform-aws-elastic-beanstalk-application](https://github.com/cloudposse/terraform-aws-elastic-beanstalk-application) - Terraform Module to define an ElasticBeanstalk Application
- [geodesic](https://github.com/cloudposse/geodesic) -  Geodesic is the fastest way to get up and running with a rock solid, production grade cloud platform built on strictly Open Source tools.
- [terraform-aws-elasticache-cloudwatch-sns-alarms](https://github.com/cloudposse/terraform-aws-elasticache-cloudwatch-sns-alarms) -  Terraform module that configures CloudWatch SNS alerts for ElastiCache



## Help

**Got a question?**

File a GitHub [issue](https://github.com/cloudposse/terraform-aws-elastic-beanstalk-environment/issues), send us an [email][email] or join our [Slack Community][slack].

## Commercial Support

Work directly with our team of DevOps experts via email, slack, and video conferencing. 

We provide [*commercial support*][commercial_support] for all of our [Open Source][github] projects. As a *Dedicated Support* customer, you have access to our team of subject matter experts at a fraction of the cost of a full-time engineer. 

[![E-Mail](https://img.shields.io/badge/email-hello@cloudposse.com-blue.svg)](mailto:hello@cloudposse.com)

- **Questions.** We'll use a Shared Slack channel between your team and ours.
- **Troubleshooting.** We'll help you triage why things aren't working.
- **Code Reviews.** We'll review your Pull Requests and provide constructive feedback.
- **Bug Fixes.** We'll rapidly work to fix any bugs in our projects.
- **Build New Terraform Modules.** We'll develop original modules to provision infrastructure.
- **Cloud Architecture.** We'll assist with your cloud strategy and design.
- **Implementation.** We'll provide hands-on support to implement our reference architectures. 


## Community Forum

Get access to our [Open Source Community Forum][slack] on Slack. It's **FREE** to join for everyone! Our "SweetOps" community is where you get to talk with others who share a similar vision for how to rollout and manage infrastructure. This is the best place to talk shop, ask questions, solicit feedback, and work together as a community to build *sweet* infrastructure.

## Contributing

### Bug Reports & Feature Requests

Please use the [issue tracker](https://github.com/cloudposse/terraform-aws-elastic-beanstalk-environment/issues) to report any bugs or file feature requests.

### Developing

If you are interested in being a contributor and want to get involved in developing this project or [help out](https://github.com/orgs/cloudposse/projects/3) with our other projects, we would love to hear from you! Shoot us an [email](mailto:hello@cloudposse.com).

In general, PRs are welcome. We follow the typical "fork-and-pull" Git workflow.

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull Request** so that we can review your changes

**NOTE:** Be sure to merge the latest changes from "upstream" before making a pull request!


## Copyright

Copyright © 2017-2018 [Cloud Posse, LLC](https://cloudposse.com)



## License 

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) 

See [LICENSE](LICENSE) for full details.

    Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

      https://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.









## Trademarks

All other trademarks referenced herein are the property of their respective owners.

## About

This project is maintained and funded by [Cloud Posse, LLC][website]. Like it? Please let us know at <hello@cloudposse.com>

[![Cloud Posse](https://cloudposse.com/logo-300x69.svg)](https://cloudposse.com)

We're a [DevOps Professional Services][hire] company based in Los Angeles, CA. We love [Open Source Software](https://github.com/cloudposse/)!

We offer paid support on all of our projects.  

Check out [our other projects][github], [apply for a job][jobs], or [hire us][hire] to help with your cloud strategy and implementation.

  [docs]: https://docs.cloudposse.com/
  [website]: https://cloudposse.com/
  [github]: https://github.com/cloudposse/
  [commercial_support]: https://github.com/orgs/cloudposse/projects
  [jobs]: https://cloudposse.com/jobs/
  [hire]: https://cloudposse.com/contact/
  [slack]: https://slack.cloudposse.com/
  [linkedin]: https://www.linkedin.com/company/cloudposse
  [twitter]: https://twitter.com/cloudposse/
  [email]: mailto:hello@cloudposse.com


### Contributors

|  [![Erik Osterman][osterman_avatar]][osterman_homepage]<br/>[Erik Osterman][osterman_homepage] | [![Igor Rodionov][goruha_avatar]][goruha_homepage]<br/>[Igor Rodionov][goruha_homepage] | [![Andriy Knysh][aknysh_avatar]][aknysh_homepage]<br/>[Andriy Knysh][aknysh_homepage] | [![Guillaume Delacour][guikcd_avatar]][guikcd_homepage]<br/>[Guillaume Delacour][guikcd_homepage] | [![Viktor Erpylev][velmoga_avatar]][velmoga_homepage]<br/>[Viktor Erpylev][velmoga_homepage] | [![Lucas Pearson][pearson-lucas-dev_avatar]][pearson-lucas-dev_homepage]<br/>[Lucas Pearson][pearson-lucas-dev_homepage] |
|---|---|---|---|---|---|

  [osterman_homepage]: https://github.com/osterman
  [osterman_avatar]: https://github.com/osterman.png?size=150
  [goruha_homepage]: https://github.com/goruha
  [goruha_avatar]: https://github.com/goruha.png?size=150
  [aknysh_homepage]: https://github.com/aknysh
  [aknysh_avatar]: https://github.com/aknysh.png?size=150
  [guikcd_homepage]: https://github.com/guikcd
  [guikcd_avatar]: https://github.com/guikcd.png?size=150
  [velmoga_homepage]: https://github.com/velmoga
  [velmoga_avatar]: https://github.com/velmoga.png?size=150
  [pearson-lucas-dev_homepage]: https://github.com/pearson-lucas-dev
  [pearson-lucas-dev_avatar]: https://github.com/pearson-lucas-dev.png?size=150


