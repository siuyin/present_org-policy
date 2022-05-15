# org-policy: Defining and enforcing policy at the organisation level

# Requirements

## Feature: Defining policy 
As a regulator in my organisation, I want write policies that can be
automatically enforced  
so that we stay compliant.

### Scenario: Machine interpretable policy
Given I am a regulator in my organisation  
When I have written my policy document  
Then I should see that my policy is enforcible by a computer program.

See [example](https://play.openpolicyagent.org/p/tlpT5tsPBB)
on rego playground.

## Feature: Automating policy enforcement
As a product owner my organisation, I want my service to comply with organisation policy  
so that my product is compliant.

### Scenario: Assess input against Policy and get a decision
Given I am a product owner  
And a machine-readable Policy  
And a current set of Data the Policy references  
When I present a set of Input data to my product  
Then I should receive an approved or denied decision consistent with applying Policy, Data and Input.

[demo](demo.md)
