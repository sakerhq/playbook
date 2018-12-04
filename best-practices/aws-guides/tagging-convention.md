# AWS Tagging Convention

## General Best Practices
- When creating a tagging strategy for AWS resources, make sure that it accurately represents organizationally relevant dimensions and adheres to the following tagging best practices:
- Always use a standardized, case-sensitive format for tags, and implement it consistently across all resource types.
- Consider tag dimensions that support the ability to manage resource access control, cost tracking, automation, and organization.
Implement automated tools to help manage resource tags. - The Resource Groups Tagging API enables programmatic control of tags, making it easier to automatically manage, search, and filter tags and resources. It also simplifies backups of tag data across all supported services with a single API call per AWS Region.
- Err on the side of using too many tags rather than too few tags.
- Remember that it is easy to modify tags to accommodate changing business requirements, however consider the ramifications of future changes, especially in relation to tag-based access control, automation, or upstream billing reports.

## Tagging Naming Conventions
A best practice is to combine several of the tag keys and values into compound tags. For example, instead of creating 3 keys called “OwnerName”, “OwnerPhone”, and “OwnerEmail,” the 3 keys could be combined into 1 key called “OwnerContact,” which could contain the compound values of Name, Phone, and Email address using a pipe delimiter (e.g. John Doe|1-555-1212|jdoe@org.com).

### Style Rules
- Tag key names are case-sensitive and can contain mixed-case letters, numbers, underscores, and hyphens.
- Tag key names should use upper CamelCase (a.k.a. Pascal case), a convention that combines words/abbreviations by beginning each word with a capital letter such as “MiscMetadata” and “SupportEndpoints”.
- Externally managed tags -- for example, those supported by managed services partners -- should use a unique tag key name prefix not to exceed 12 characters followed by a hypen (“-“) character (e.g. PartnerName-Contact or 3rdPartyName- SupportEndpoint).
- Tag values are case-sensitive and should not use the semi-colon (“;”), equal sign (“=”), or pipe (“|”) characters as these are used as delimiters in compound values.
- Compound tag value key names should use Pascal case followed by an equal sign (“=”) such as KeyName1=value1|value2|value3;KeyName2=value1|value2|value3

## Tags
- Name 
- Application* 
- Owner
- Environment
- Version
- Billing

These are the primary keys, but other keys can also be added as needed such as Compliance, Sensitivity, Client, Audited, or Application Role. 

## Example 
- Name: Flycatcher-Prod-Bastion
- Application: Flycatcher
- Owner: Steven Comyn
- Environment: Production
- Version: v1.2.3
- Billing: CA0003

## Useful Links
- [AWS Tagging Strategies](https://aws.amazon.com/answers/account-management/aws-tagging-strategies/)
- [Tag Editor](https://resources.console.aws.amazon.com/r/tags)
- [Tagging Your Amazon EC2 Resources](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html)

*Application can be the contract job code or project code name. When a project evolves to a product add a pipe delimiter and include the product name.
