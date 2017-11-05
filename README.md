## terraform-aws-elastic-beanstalk-environment
<!--------------------------------DO NOT EDIT README.md-------------------------------->
Terraform module to provision AWS Elastic Beanstalk environment


## Input

<!--------------------------------REQUIRE POSTPROCESSING-------------------------------->
|  Name |  Default  |  Description  |
|:------|:---------:|:--------------:|
| alb_zone_id |{} |From: http://docs.aws.amazon.com/general/latest/gr/rande.html#elasticbeanstalk_region Via: https://github.com/hashicorp/terraform/issues/7071   |
| app |__REQUIRED__ |  |
| attributes |[] |  |
| autoscale_lower_bound |"20" |  |
| autoscale_max |"3" |  |
| autoscale_min |"2" |  |
| autoscale_upper_bound |"80" |  |
| config_source |"" |  |
| delimiter |"-" |  |
| env_default_key |"DEFAULT_ENV_%d" |  |
| env_default_value |"UNSET" |  |
| env_vars |{} |  |
| healthcheck_url |"/healthcheck" |  |
| http_listener_enabled |"false" |  |
| instance_type |"t2.micro" |  |
| keypair |__REQUIRED__ |  |
| loadbalancer_certificate_arn |"" |  |
| loadbalancer_type |"classic" |  |
| name |"app" |  |
| namespace |"global" |  |
| notification_endpoint |"" |  |
| notification_protocol |"email" |  |
| notification_topic_arn |"" |  |
| notification_topic_name |"" |  |
| private_subnets |__REQUIRED__ |  |
| public_subnets |__REQUIRED__ |  |
| security_groups |__REQUIRED__ |  |
| solution_stack_name |"" |  |
| ssh_listener_enabled |"false" |  |
| ssh_listener_port |"22" |  |
| stage |"default" |  |
| tags |{} |  |
| updating_max_batch |"1" |  |
| updating_min_in_service |"1" |  |
| vpc_id |__REQUIRED__ |  |
| zone_id |"" |  |
## Output

<!--------------------------------REQUIRE POSTPROCESSING-------------------------------->
|  Name | Description  |
|:------|:------------:|
| elb_dns_name |   |
| elb_zone_id |   |
| host |   |
| name |   |
| security_group_id |   |

## Help

**Got a question?**

File a GitHub [issue](https://github.com/cloudposse/terraform-aws-elastic-beanstalk-environment/issues), send us an [email](mailto:hello@cloudposse.com) or reach out to us on [Gitter](https://gitter.im/cloudposse/).
## Contributing

### Bug Reports & Feature Requests

Please use the [issue tracker](https://github.com/cloudposse/terraform-aws-elastic-beanstalk-environment/issues) to report any bugs or file feature requests.

### Developing

If you are interested in being a contributor and want to get involved in developing `terraform-aws-elastic-beanstalk-environment`, we would love to hear from you! Shoot us an [email](mailto:hello@cloudposse.com).

In general, PRs are welcome. We follow the typical "fork-and-pull" Git workflow.

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull request** so that we can review your changes

**NOTE:** Be sure to merge the latest from "upstream" before making a pull request!
## License

[APACHE 2.0](LICENSE) © 2017 [Cloud Posse, LLC](https://cloudposse.com)

See [LICENSE](LICENSE) for full details.

    Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.
## About

This module is maintained and funded by [Cloud Posse, LLC][website]. Like it? Please let us know at <hello@cloudposse.com>

We love [Open Source Software](https://github.com/cloudposse/)!

See [our other projects][community]
or [hire us][hire] to help build your next cloud-platform.

  [website]: http://cloudposse.com/
  [community]: https://github.com/cloudposse/
  [hire]: http://cloudposse.com/contact/

### Contributors

|[![Erik Osterman][erik_img]][erik_web]<br/>[Erik Osterman][erik_web] |[![Igor Rodionov][igor_img]][igor_web]<br/>[Igor Rodionov][igor_img] |[![Andriy Knysh][andriy_img]][andriy_web]<br/>[Andriy Knysh][andriy_web] |
|---|---|---|

[andriy_img]: https://avatars0.githubusercontent.com/u/7356997?v=4&u=ed9ce1c9151d552d985bdf5546772e14ef7ab617&s=144
[andriy_web]: https://github.com/aknysh/

[erik_img]: http://s.gravatar.com/avatar/88c480d4f73b813904e00a5695a454cb?s=144
[erik_web]: https://github.com/osterman/

[igor_img]: http://s.gravatar.com/avatar/bc70834d32ed4517568a1feb0b9be7e2?s=144
[igor_web]: https://github.com/goruha/

[konstantin_img]: https://avatars1.githubusercontent.com/u/11299538?v=4&u=ed9ce1c9151d552d985bdf5546772e14ef7ab617&s=144
[konstantin_web]: https://github.com/comeanother/

[sergey_img]: https://avatars1.githubusercontent.com/u/1134449?v=4&u=ed9ce1c9151d552d985bdf5546772e14ef7ab617&s=144
[sergey_web]: https://github.com/s2504s/

[valeriy_img]: https://avatars1.githubusercontent.com/u/10601658?v=4&u=ed9ce1c9151d552d985bdf5546772e14ef7ab617&s=144
[valeriy_web]: https://github.com/drama17/

[vladimir_img]: https://avatars1.githubusercontent.com/u/26582191?v=4&u=ed9ce1c9151d552d985bdf5546772e14ef7ab617&s=144
[vladimir_web]: https://github.com/SweetOps/
