# OSATE Roadmap

## Planned OSATE Releases

### OSATE 2.5.0

Release: May 2019

__Public release__

* based on Eclipse 2019-03

__Non-public release__

* TBD

__Development__

* TBD

### OSATE 2.5.1

Release: June/July 2019

__Public release__

* TBD

__Non-public release__

* TBD

__Development__

* TBD

### OSATE 2.6.0

Release: August 2019

__Public release__

* based on Eclipse 2019-06

__Non-public release__

* TBD

__Development__

* TBD

## Roadmap for AADL Language Support

### Support for AADL 2.2

Support for the following AADL language constructs may be added in a future release

* Specification of partial end-to-end flows
  [(issue #7)](https://github.com/saeaadl/aadlv2.1/issues/7)

#### Limitations

There are a couple of rarely used language features that are not fully supported on OSATE. In general, these features are
supported in the declarative model but models containing these features cannot be instantiated.

* Binding-specific property associations (`in binding`)
* Automatic expansion of a property reference value the references an array into a list of references. (Standard document section 11.4 (L6))
* Subcomponent arrays with multiple component implementations
* Aggregate data ports
* Not all classifier matching and substitution rules are fully implemented
    + For `Classifier_Substitution_Rule` only `Classifier_Match` and `Type_Extension` are implemented
    + For `Prototype_Substitution_Rule` only `Classifier_Match` is implemented
    + For `Classifier_Matching_Rule` in the context of feature group connections only `Classifier_Match`, `Equivalence`,
      and `Subset` are implemented
    + For `Classifier_Matching_Rule` in the context of any other connection kind only `Classifier_Match`, `Equivalence`,
      `Subset`, and `Conversion` are implemented
* Internal features and processor features (Standard document section 8.9)
* `none` statement for `requires modes`
* End to end flow specifications

### Support for AADL 3

We are planning to create experimental OSATE releases to prototype AADL 3 language features. Details are still tbd.
