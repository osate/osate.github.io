# OSATE Roadmap

## Planned OSATE Releases

### OSATE 2.3.0

Release: Oct 2017

__Public release__
* Based on Eclipse Oxygen.1
* Reworked fault tree representation
* Improved minimal cut-set calculation
* Plugin contributions as virtual project
* Unified analysis result representation (internal)
* New result representation used in latency analysis (internal)
* Update from Eclipse actions to commands (internal)

__Development__

* Oomph setup for development environment

### OSATE 2.3.1

Release: Dec 2017

__Public release__

* Based on Eclipse Oxygen.1a, Xtext 2.13
* Graphical editor improvements
* Additional file creation wizards for reqspec, etc
* Consistent reorganization of commands in main menu, toolbar, context menu
* New result representation used in resource budgeting analyses (internal)
* Documentation updates

__Non-public release__

* Improvements to resource budgeting workflows
* Additional workflows for safety analyses

__Development__

* Public build server?
* Integration of code coverage tool into automated build
* Automated build of pull requests

### OSATE 2.3.2

Release: Feb 2018

__Public release__

* Based on Eclipse Oxygen.2
* Update to Java9 (question)
* Graphical editor improvements
* Analysis result reports generated using BIRT
* Documentation updates

__Non-public release__

* Updated workflows for safety analyses
* Updated workflow documentation

__Development__

* Integration of GUI tests (SWTBot, RCPTT) into automated build
* Test suite for resource budgeting
* Semantic versioning for plugins

### OSATE 2.3.3

Release: Apr 2018

__Public release__

* Graphical editor improvements
* Improved navigational views
* New result representation used in safety analyses (internal)
* Revised error marker handling (internal)
* Documentation updates

__Non-public release__

* Updated workflows for safety analyses
* Updated workflow documentation

__Development__

* Test suite for latency analysis

### OSATE 2.3.4

Release: Jun 2018

__Public release__

* Based on Eclipse Oxygen.3
* Graphical editor improvements
* Improved rename refactoring support
* Documentation updates

__Development__

* Test suite for safety analyses

### OSATE 2.3.5

Release: Aug 2018

__Public release__

* Graphical editor improvements
* Refactoring: moving classifiers between packages
* Documentation updates (TBD)

__Development__

* Expanded test suite for safety analyses

### OSATE 2.3.6

Release: Oct 2018

__Public release__

* TBD

### OSATE 2.3.7

Release: Dec 2018

__Public release__

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

### Support for AADL 3

We are planning to create experimental OSATE releases to prototype AADL 3 language features. Details are still tbd.
