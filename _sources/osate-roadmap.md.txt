# Roadmap for AADL Language Support

## Support for AADL 2.2

### OSATE 2.2.1

This version supports AADL 2.1 and a subset of the changes introduced in AADL 2.2. We provide maintenance releases
(update01, update02, ...) that fix bugs but do not change the supported language features or the underlying meta-model.

The next maintenance release (update03) is planned for December 2016.

### OSATE 2.2.2

This version is under development will implement all laguage changes that were introduced as part of AADL version 2.2.
The following language features are not part of OSATE 2.2.1 but will be implemented for OSATE 2.2.2.

* Specification of partial end-to-end flows
  [(issue #7)](https://github.com/saeaadl/aadlv2.1/issues/7)
* Connections between two subcomponents can connect features nested in feature groups
  [(issue #15)](https://github.com/saeaadl/aadlv2.1/issues/15)
* All changes to predefined properties

### OSATE 2.2.y (y > 2)

These will be bug fix releases. We don't anticipate further changes to supported language features or the underlying
meta-model.

### OSATE 2.x (x > 2)

These will add features and new analyses.

### Limitations

There are a couple of rarely used language features that are not fully supported on OSATE. In general, these features are
supported in the declarative model but models containting these features cannot be instantiated.

* Binding-specific property associations (`in binding`)
* Subcomponent arrays with multiple component implementations
* Aggregate data ports
* Not all classifier matching and substitution rules are fully implemented
    + For `Classifier_Substitution_Rule` only `Classifier_Match` and `Type_Extension` are implemented
    + For `Prototype_Substitution_Rule` only `Classifier_Match` is implemented
    + For `Classifier_Matching_Rule` in the context of feature group connections only `Classifier_Match`, `Equivalence`,
      and `Subset` are implemented
    + For `Classifier_Matching_Rule` in the context of any other connection kind only `Classifier_Match`, `Equivalence`,
      `Subset`, and `Conversion` are implemented

## Support for AADL 3

We are planning to create experimental OSATE releases to prototype AADL 3 language features. Details are still tbd.
