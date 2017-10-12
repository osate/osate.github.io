# OSATE Roadmap

## Planned OSATE Releases

### OSATE 2.3.0

Release: Nov 2017

#### Public release

* Based on Eclipse Oxygen.1
* Reworked fault tree representation
* Improved minimal cut-set calculation
* Plugin contributions as virtual project
* Unified analysis result representation
* New result representation used in latency analysis
* Update from Eclipse actions to commands (internal)

#### Development

* Oomph setup for development environment

### OSATE 2.3.1

Release: Dec 2017

#### Public release

* Based on Eclipse Oxygen.1a, Xtext 2.13
* Graphical editor improvements
* Additional file creation wizards for reqspec, etc
* Consistent reorganization of commands in main menu, toolbar, context menu
* New result representation used in resource budgeting analyses
* Documentation updates

#### Non-public release

* Improvements to resource budgeting workflows
* Additional workflows for safety analyses

#### Development

* Integration of code coverage tool into automated build
* Automated build of pull requests

### OSATE 2.3.2

Release: Feb 2018

#### Public release

* Based on Eclipse Oxygen.2
* Update to Java9 (question)
* Graphical editor improvements
* Analysis result reports generation using BIRT
* Documentation updates

#### Non-public release

* Updated workflows for safety analyses
* Updated workflow documentation

#### Development

* Integration of GUI tests (SWTBot, RCPTT) into automated build
* Test suite for resource budgeting
* Semantic versioning for plugins

### OSATE 2.3.3

Release: Apr 2018

#### Public release

* Graphical editor improvements
* Improved navigational views
* New result representation used in safety analyses
* Revised internal error marker handling
* Documentation updates

#### Non-public release

* Updated workflows for safety analyses
* Updated workflow documentation

#### Development

* Test suite for latency analysis

### OSATE 2.3.4

Release: Jun 2018

#### Public release

* Based on Eclipse Oxygen.3
* Graphical editor improvements
* Improved rename refactoring support
* Documentation updates

#### Development

* Test suite for safety analyses

### OSATE 2.3.5

Release: Aug 2018

#### Public release

* Graphical editor improvements
* Refactoring: moving classifiers between packages
* Documentation updates (TBD)

#### Development

* Expanded test suite for safety analyses

### OSATE 2.3.6

Release: Oct 2018

#### Public release
* TBD

### OSATE 2.3.7

Release: Dec 2018

#### Public release

* TBD

## Roadmap for AADL Language Support

### Support for AADL 2.2

#### OSATE 2.2.1

This version supports AADL 2.1 and a subset of the changes introduced in AADL 2.2. We provide maintenance releases
(update01, update02, ...) that fix bugs but do not change the supported language features or the underlying meta-model.

The next maintenance release (update03) is planned for December 2016.

#### OSATE 2.2.2

This version is under development will implement all laguage changes that were introduced as part of AADL version 2.2.
The following language features are not part of OSATE 2.2.1 but will be implemented for OSATE 2.2.2.

* Specification of partial end-to-end flows
  [(issue #7)](https://github.com/saeaadl/aadlv2.1/issues/7)
* Connections between two subcomponents can connect features nested in feature groups
  [(issue #15)](https://github.com/saeaadl/aadlv2.1/issues/15)
* All changes to predefined properties

#### OSATE 2.2.y (y > 2)

These will be bug fix releases. We don't anticipate further changes to supported language features or the underlying
meta-model.

#### OSATE 2.x (x > 2)

These will add features and new analyses.

#### Limitations

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

### Support for AADL 3

We are planning to create experimental OSATE releases to prototype AADL 3 language features. Details are still tbd.
