# Enterprise Contract Configuration Files

This repo contains a set of `policy.yaml` files which can be used with
Enterprise Contract and the Red Hat Trusted Application Pipeline.

There is a predefined RHTAP Integration Test pipeline definition for each of
these configs which can be used when creating an Integration Test in RHTAP as
per the [documentation
here](https://redhat-appstudio.github.io/docs.appstudio.io/Documentation/main/how-to-guides/proc_managing-compliance-with-the-enterprise-contract/).

The policy configuration files are:

### Default

Includes rules for levels 1, 2 & 3 of SLSA v0.1. This is the default config used for new RHTAP applications.

* URL for Enterprise Contract: `github.com/enterprise-contract/config//default`
* Source: [default/policy.yaml](https://github.com/enterprise-contract/config/blob/main/default/policy.yaml)
* Collections: [@slsa1](https://enterprisecontract.dev/docs/ec-policies/release_policy.html#slsa1), [@slsa2](https://enterprisecontract.dev/docs/ec-policies/release_policy.html#slsa2), [@slsa3](https://enterprisecontract.dev/docs/ec-policies/release_policy.html#slsa3)
* RHTAP Integration Test pipeline definition:
    * Github URL: `https://github.com/redhat-appstudio/build-definitions`
    * Path in repository: [`pipelines/enterprise-contract.yaml`](https://github.com/redhat-appstudio/build-definitions/blob/main/pipelines/enterprise-contract.yaml)

### Red Hat

Includes the full set of rules and policies required internally by Red Hat when building Red Hat products.

* URL for Enterprise Contract: `github.com/enterprise-contract/config//redhat`
* Source: [redhat/policy.yaml](https://github.com/enterprise-contract/config/blob/main/redhat/policy.yaml)
* Collections: [@redhat](https://enterprisecontract.dev/docs/ec-policies/release_policy.html#redhat)
* RHTAP Integration Test pipeline definition:
    * Github URL: `https://github.com/redhat-appstudio/build-definitions`
    * Path in repository: [`pipelines/enterprise-contract-redhat.yaml`](https://github.com/redhat-appstudio/build-definitions/blob/main/pipelines/enterprise-contract-redhat.yaml)

### SLSA3

Rules specifically related to levels 1, 2 & 3 of SLSA v0.1, plus a set of basic checks that are expected to pass for all RHTAP builds.

* URL for Enterprise Contract: `github.com/enterprise-contract/config//slsa3`
* Source: [slsa3/policy.yaml](https://github.com/enterprise-contract/config/blob/main/slsa3/policy.yaml)
* Collections: [@minimal](https://enterprisecontract.dev/docs/ec-policies/release_policy.html#minimal), [@slsa1](https://enterprisecontract.dev/docs/ec-policies/release_policy.html#slsa1), [@slsa2](https://enterprisecontract.dev/docs/ec-policies/release_policy.html#slsa2), [@slsa3](https://enterprisecontract.dev/docs/ec-policies/release_policy.html#slsa3)
* RHTAP Integration Test pipeline definition:
    * Github URL: `https://github.com/redhat-appstudio/build-definitions`
    * Path in repository: [`pipelines/enterprise-contract-slsa3.yaml`](https://github.com/redhat-appstudio/build-definitions/blob/main/pipelines/enterprise-contract-slsa3.yaml)

### Everything

Include every rule in the default policy source. For experiments only. This is not expected to pass for RHTAP builds without excluding some rules.

* URL for Enterprise Contract: `github.com/enterprise-contract/config//everything`
* Source: [everything/policy.yaml](https://github.com/enterprise-contract/config/blob/main/everything/policy.yaml)
* Collections:
* RHTAP Integration Test pipeline definition:
    * Github URL: `https://github.com/redhat-appstudio/build-definitions`
    * Path in repository: [`pipelines/enterprise-contract-everything.yaml`](https://github.com/redhat-appstudio/build-definitions/blob/main/pipelines/enterprise-contract-everything.yaml)

## See also

* [Policy Rule Documentation](https://enterprisecontract.dev/docs/ec-policies/release_policy.html)
* [Getting Started with Enterprise Contract &amp; Red Hat Trusted Application Pipeline](https://enterprisecontract.dev/docs/user-guide/main/getting-started.html)
