# zebrands-ssessment


* Create [terraform module](https://github.com/ramiroduarteavalos/terraform-eks.git) 

Using infrastructure as code allows you to declare infrastructure components in configuration files that are then used to provision, adjust and tear down infrastructure in various cloud providers. 

### Create pull request
#### Create a new branch in your forked repo named update-tfc-backend.

```
git checkout -b '${cluster}-${env}'
```

#### Update the main.tf file with the Terraform Cloud organization and workspace you created earlier.

```
terraform {
  required_providers {
    aws = {
      source = "hashicorp/aws"
    }
    random = {
      source = "hashicorp/random"
    }
  }

  backend "remote" {
    organization = "zebrands-assessment"

    workspaces {
      name = "zebrands-dev"
    }
  }
}
```

#### Prepare to add your changes to your forked repository.

```
git add .
```

#### Commit these changes with a message.

```
git commit -am 'Add ${cluster}-${env}'
```

#### Push these changes.

```
git push --set-upstream origin ${cluster}-${env}
```

### Review and merge pull request

#### Navigate to your pull request. Your PR will trigger the Terraform Actions workflow. When the workflow completes, it will add a comment with the outcome of each step and a speculative plan.

![](images/gh-actions-pr-plan.gif)

* Install [cert-manager](https://cert-manager.io/docs/installation/helm/)


```
* Execute pipeline [frontend](https://gitlab.com/ramiroduarteavalos/frontend/) && [backend](https://gitlab.com/ramiroduarteavalos/backend/)


| frontend | [url](https://dev.cloude.ar/) |

![](images/react.png)

| backend | [url](https://backend.dev.cloude.ar/welcome/) |

![](images/python.png)

## 🛠️

* [terraform](https://registry.terraform.io/modules/terraform-aws-modules/eks/aws/latest) 
* [Amazon Elastic Kubernetes Service](https://aws.amazon.com/es/eks/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc&eks-blogs.sort-by=item.additionalFields.createdDate&eks-blogs.sort-order=desc)
* [helm](https://helm.sh/)

## Authors
| Name | Position |
| ------ | ------ |
| Ramiro Duarte Avalos | DevOps Engineer / SRE |
