# Release Notes

## Stable Releases

### Version 2.2.1 update 02

#### Release

  - **GIT tag**: 2.2.1-UPDATE02
  - **Release date**: Oct 14, 2016
  - **Eclipse base version**: Mars.2
  - **Java version**: Java 8
  - **Eclipse Update-Site**: <http://www.aadl.info/aadl/osate/stable/2.2.1/update-site>
  - **Download URL**: <http://www.aadl.info/aadl/osate/stable/2.2.1/products>

This is a maintenance release that contains bug fixes and improvements to the ReqSpec language. It also includes
a beta version the Verify and Alisa languages for requirements verification.

#### Notable Changes

1. Added missing `Array_Size_Range` property type
1. Updated help text for flow latency analysis
1. Many small improvements to the graphical editor
1. Various improvements for fault tree generation

#### Fixed Issues

* OSATE core and analyses
  1. Flow sink implementations are now property serialized (#617)
  1. Fixed a crash when creating an instance model that has errors (#712)
  1. Fixed a deadlock during instantiation (#726)
  1. Connections that go through a component (from in port directly to out port) are now flagged as errors (#727, #728)
  1. Validation of feature group connections now flags mismatched feature group types as an error (#709)
  1. Fixed validation to allow references to elements of multi-dimensional arrays in property values (#694)
  1. Fixed a bug that caused missing connections in instance model (#734)
  1. Instance model analyses now take selected system operation mode into account (#736)
  1. Fixed a deadlock during flow latency analysis (#737)
* Graphical Editor
  1. Default port direction is set according to the side of the component (#150)
  1. Fixed bug that prevented adding subcomponent flow to end-to-end flow or flow implementation (#166)
  1. It is now possible to select a component when it is covered by labels (context menu: select container) (#171)
  1. Prevent negative y-coordinates for feature groups (#172)
* Error Model Annex
  1. FHA report was missing hazards (#113)

#### Known Issues

1.  Using the AADL Property View to edit property values results in bad formatting.

### Version 2.2.1 update 01

#### Release

  - **GIT tag**: 2.2.1-UPDATE01
  - **Release date**: May 24, 2016
  - **Eclipse base version**: Mars.2
  - **Java version**: Java 8
  - **Eclipse Update-Site**: <http://www.aadl.info/aadl/osate/stable/2.2.1/update-site>
  - **Download URL**: <http://www.aadl.info/aadl/osate/stable/2.2.1/products>

This is a maintenance release that contains bug fixes and improvements to the ReqSpec language.

#### Notable Changes

1.  Property `Classifier_Matching_Rule => Subset` is now supported for instantiation.
2.  Creating a text file for an instance model works now.
3.  Added documentation for using the AADL Property Values view under OSATE Core Documentation
    -> Getting started -> Viewing and editing property values.
4.  Added a Usage Guide to the Resolute documentation.
5.  Added more types and type checking to the ReqSpec language. The help text has been updated
    to reflect these changes.

#### Known Issues

1.  Using the AADL Property View to edit property values results in bad formatting.

#### Fixed Issues

The full lists of closed issues for this release are available at

<https://github.com/osate/osate2-core/issues?q=is%3Aissue+updated%3A2016-04-19..2016-05-22+is%3Aclosed>

<https://github.com/osate/osate2-plugins/issues?q=is%3Aissue+updated%3A2016-04-19..2016-05-22+is%3Aclosed>

<https://github.com/osate/ErrorModelV2/issues?q=is%3Aissue+updated%3A2016-04-19..2016-05-22+is%3Aclosed>

### Version 2.2.1

#### Release

  - **GIT tag**: 2.2.1-RELEASE-20160418
  - **Release date**: April 18, 2016
  - **Eclipse base version**: Mars.2
  - **Java version**: Java 8
  - **Eclipse Update-Site**: <http://www.aadl.info/aadl/osate/stable/2.2.1/update-site>
  - **Download URL**: <http://www.aadl.info/aadl/osate/stable/2.2.1/products>

#### Notable Changes

1.  We have included the EMFTA tool for fault tree analysis (see Help text).
    The existing export to OpenFTA has been removed
2.  OSATE now includes requirements specification language (ReqSpec) from
    our ALISA project (see Help text)
3.  Implemented approved language errata:
    1.  Abstract features are allowed as mode transition triggers
    2.  Added property Reference_Time
	3.  Abstract features can reference classifiers in addition to prototypes:
	
            prototypes
			  fp: feature;
			  dt: data;
			features
			  -- feature is the prototype actual
			  f1: prototype fp;
			  -- abstract feature referencing a data classifier
			  f2: feature SomeDataType;
			  -- abstract feature referencing a data prototype
			  f3: feature dt;

4.  Added textual representation of instance models. Convert AADL instance model
    file to text via action "Generate Textual Instance" in AADL Navigator context 
	menu
5.  Added BIRT for report generation. An example report for requirements
    traceability is included: Action "Requirements Tracing" in context menu in
    the AADL Navigatior view, active for AADL packages, instance models, system
    requirements and system goals.
    The report sources are in plugin org.osate.reqtrace
6.  Unnecessary plugins were removed to reduce download size
7.  Updated Agree to version 2.1.3
8.  The underlying Eclipse version has been updated to Mars.2

#### Known Issues

1.  Using the AADL Property View to edit property values results in bad
    formatting

#### Fixed Issues

The full lists of closed issues for this release are available at

<https://github.com/osate/osate2-core/issues?q=is%3Aissue+updated%3A2015-12-24..2016-04-18+is%3Aclosed>

<https://github.com/osate/osate2-plugins/issues?q=is%3Aissue+updated%3A2015-12-24..2016-04-18+is%3Aclosed>

<https://github.com/osate/osate-ge/issues?q=is%3Aissue+updated%3A2015-12-24..2016-04-18+is%3Aclosed>

<https://github.com/osate/ErrorModelV2/issues?q=is%3Aissue+updated%3A2015-12-24..2016-04-18+is%3Aclosed>

### Version 2.2.0

#### Release

  - **GIT tag**: 2.2.0-RELEASE-20151223
  - **Release date**: January 5, 2016
  - **Eclipse base version**: Mars.1
  - **Java version**: Java 8
  - **Eclipse Update-Site**:
    <http://www.aadl.info/aadl/osate/stable/2.2.0/update-site>
  - **Download URL**:
    <http://www.aadl.info/aadl/osate/stable/2.2.0/products>

#### Notable changes

1.  OSATE is now based on Eclipse Mars which requires a new full
    installation
2.  Implemented approved errata for properties:
    1.  Process\_Swap\_Execution\_time now applies to virtual processor.
    2.  Add processor, virtual processor in applies to of
        Activate\_Entry\_Point. They are included in the other
        entry\_point properties.
    3.  Code\_Size, Heap\_Size, Data\_Size, and Stack\_Size now apply to
        virtual processors.
    4.  Mark Byte\_Count as deprecated.
    5.  Add Source\_xx\_Size back in and mark as deprecated. These are
        used in the standard, the book, and in the course. Backward
        compatibility.
    6.  Memory\_Binding properties now apply to system and processor.
        Also to virtual processor to model partitions with memory
        budgets.
    7.  Property values are no longer allowed as array index value.
3.  Performance improvements in graphical editor
4.  Outline view can now handle annexes

#### Known Issues

1.  Using the AADL Property View to edit property values results in bad
    formatting

#### Fixed Issues

The full lists of closed issues for this release are available at

<https://github.com/osate/osate2-core/issues?q=is%3Aissue+updated%3A2015-09-05..2015-12-22+is%3Aclosed>

<https://github.com/osate/osate2-plugins/issues?q=is%3Aissue+updated%3A2015-09-05..2015-12-22+is%3Aclosed>

<https://github.com/osate/osate-ge/issues?q=is%3Aissue+updated%3A2015-09-05..2015-12-22+is%3Aclosed>

<https://github.com/osate/ErrorModelV2/issues?q=is%3Aissue+updated%3A2015-09-05..2015-12-22+is%3Aclosed>

### Version 2.1.2

#### Release

  - **GIT tag**: 2.1.2-RELEASE-20150904
  - **Release date**: September 14, 2015
  - **Eclipse base version**: Luna SR2
  - **Java version**: Java 8
  - **Eclipse Update-Site**:
    <http://www.aadl.info/aadl/osate/stable/2.1.2/update-site>
  - **Download URL**:
    <http://www.aadl.info/aadl/osate/stable/2.1.2/products>

#### Major changes

1.  Flows can now be created in the graphical editor by clicking on
    components and connections
2.  The AADL Properties view can be used with the instance model
3.  The text editor automatically un-indents section keywords (features,
    subcomponents, etc.), see preference Window -\> Preferences -\>
    OSATE Preferences -\> Aadl2 Text Editor to control this behavior

#### Known Issues

1.  Using the AADL Property View to edit property values results in bad
    formatting

#### Fixed Issues

The full lists of closed issues for this release are available
at

<https://github.com/osate/osate2-core/issues?q=is%3Aissue+updated%3A2015-07-06..2015-09-04+is%3Aclosed>

<https://github.com/osate/osate2-plugins/issues?q=is%3Aissue+updated%3A2015-07-06..2015-09-04+is%3Aclosed>

<https://github.com/osate/osate-ge/issues?q=is%3Aissue+updated%3A2015-07-06..2015-09-04+is%3Aclosed>

<https://github.com/osate/ErrorModelV2/issues?q=is%3Aissue+updated%3A2015-07-06..2015-09-04+is%3Aclosed>

### Version 2.1.1

#### Release

  - **GIT tag**: 2.1.1-RELEASE-20150702
  - **Release date**: July 6, 2015
  - **Eclipse base version**: Luna SR2
  - **Eclipse Update-Site**:
    <http://www.aadl.info/aadl/osate/stable/2.1.1/update-site>
  - **Download URL**:
    <http://www.aadl.info/aadl/osate/stable/2.1.1/products>

#### Major changes

1.  OSATE now requires Java 8
2.  Automatically add "end" when typing in the text editor, see
    preference Window -\> Preferences -\> OSATE Preferences -\> Aadl2
    Text Editor to control this behavior
3.  New text editor command to organize with clauses
4.  The Plugin\_Resources project has subdirectories to organize
    property sets - existing workspaces should be updated automatically
    (If there is a problem, try to re-create the project using the
    context menu in the AADL Navigator: "Reset/create all Predeclared
    and Annex Properties")
5.  The AADL Property View supports editing of property associations
    declared in the classifier's properties section if the applies to
    contains a single name ("local contained")
6.  The AADL Property View works properly when the instance model editor
    is open
7.  Default values can be hidden in the AADL Property View
8.  It is now possible to navigate from the instance model property to
    the corresponding property Association in the declarative model
9.  The instance model editor now properly reloads the model if it is
    instantiated again
10. The instance model editor shows error markers
11. Updated to Agree version 2.0.0
12. Removed obsolete Lute and ARINC653 plugins from the distribution

#### Known Issues

1.  Using the AADL Property View to edit property values results in bad
    formatting

#### Fixed Issues

The full lists of closed issues for this release are available
at

<https://github.com/osate/osate2-core/issues?q=is%3Aissue+updated%3A2015-05-01..2015-07-05+is%3Aclosed>

<https://github.com/osate/osate2-plugins/issues?q=is%3Aissue+updated%3A2015-05-01..2015-07-05+is%3Aclosed>

<https://github.com/osate/osate-ge/issues?q=is%3Aissue+updated%3A2015-05-01..2015-07-05+is%3Aclosed>

<https://github.com/osate/ErrorModelV2/issues?q=is%3Aissue+updated%3A2015-05-01..2015-07-05+is%3Aclosed>

### Version 2.1.0

#### Release

  - **GIT tag**: 2.1.0-RELEASE-20150501
  - **Release date**: May 2, 2015
  - **Eclipse base version**: Luna SR2
  - **Eclipse Update-Site**:
    <http://www.aadl.info/aadl/osate/stable/2.1.0/update-site>
  - **Download URL**:
    <http://www.aadl.info/aadl/osate/stable/2.1.0/products>

#### Major changes

1.  Additional validations for textual AADL models
2.  Added quick fixes in the AADL text editor
3.  Added Resolute language reference
4.  Performance improvements in the graphical editor
5.  Flow latency analysis handles periodic buses
6.  Various bug fixes related to connection and flow instantiation

#### Known Issues

1.  Running Agree requires Java 8

#### Fixed Issues

The full lists of closed issues for this release are available
at

<https://github.com/osate/osate2-core/issues?q=is%3Aissue+updated%3A2015-02-26..2015-05-01+is%3Aclosed>

<https://github.com/osate/osate2-plugins/issues?q=is%3Aissue+updated%3A2015-02-26..2015-05-01+is%3Aclosed>

<https://github.com/osate/osate-ge/issues?q=is%3Aissue+updated%3A2015-02-26..2015-05-01+is%3Aclosed>

<https://github.com/osate/ErrorModelV2/issues?q=is%3Aissue+updated%3A2015-02-26..2015-05-01+is%3Aclosed>

### Version 2.0.9

#### Release

  - **GIT tag**: 2.0.9-RELEASE-20150301
  - **Release date**: March 2, 2015
  - **Eclipse base version**: Luna
  - **Eclipse Update-Site**:
    <http://www.aadl.info/aadl/osate/stable/2.0.9/update-site>
  - **Download URL**:
    <http://www.aadl.info/aadl/osate/stable/2.0.9/products>

#### Major changes

1.  The AADL Property View has been rewritten to support expansion of
    list and record values. In addition, property values can be edited
    directly in the view.
2.  Instance models can be created from any component **Note:** The
    SystemInstance object now references a ComponentImplementation
    instead of a SystemImplementation. Plugins may need to be adapted.
3.  We have integrated the Resolute and Agree plugins created at
    Rockwell Collins (see <https://github.com/smaccm/smaccm>). **Note:**
    Agree depends on an program (JKind 2.1) which requires Java 8 to
    run.
4.  We have integrated the Ocarina plugin for OSATE 2 (see
    <https://github.com/OpenAADL/osate2-ocarina>).

#### Known Issues

#### Fixed Issues

The full list of closed issues for this release are available
at

<https://github.com/osate/osate2-core/issues?q=is%3Aissue+updated%3A2014-10-01..2015-02-25+is%3Aclosed>

<https://github.com/osate/osate2-plugins/issues?q=is%3Aissue+updated%3A2014-10-01..2015-02-25+is%3Aclosed>

<https://github.com/osate/osate-ge/issues?q=is%3Aissue+updated%3A2014-10-01..2015-02-25+is%3Aclosed>

<https://github.com/osate/ErrorModelV2/issues?q=is%3Aissue+updated%3A2014-10-01..2015-02-25+is%3Aclosed>

### Version 2.0.8

A special page is dedicated to the [release notes of OSATE2
2.0.8](release_notes_of_OSATE2_2.0.8 "wikilink")

#### Release

  - **GIT tag**: 2.0.8-RELEASE
  - **Release date**: September, 5 2014
  - **Eclipse base version**: Luna
  - **Eclipse Update-Site**:
    <http://www.aadl.info/aadl/osate/stable/2.0.8/update-site>
  - **Download URL**:
    <http://www.aadl.info/aadl/osate/stable/2.0.8/products>

#### Major changes

1.  Switched to Eclipse Luna
2.  Refactored many analysis plugins
3.  Excel report for latency analysis
4.  Examples built-in in OSATE

#### Known Issues

1.  After the first start with a new workspace the project
    **Plugin\_Resources** may shown three times in the AADL navigator.
    Restarting OSATE fixes the issue.

### Version 2.0.7

This release was published after the 2014 July AADL meeting hold in
Orlando, Florida, USA.

#### Release

  - **GIT tag**: 2.0.7-RELEASE
  - **Release date**: July, 14 2014
  - **Eclipse base version**: Kepler
  - **Eclipse Update-Site**:
    <http://www.aadl.info/aadl/osate/stable/2.0.7/update-site>
  - **Download URL**:
    <http://www.aadl.info/aadl/osate/stable/2.0.7/products>

#### Major changes

1.  Automatically compute reliability values from sub-components in the
    Reliability Block Diagram plugin
2.  Graphical tool now works with Java 6
3.  Update of EMV2 annex, compliant with the document under ballot
4.  Update of ARINC653 properties, compliant with the version being
    under ballot for the coming September meeting.

### Version 2.0.6

This release was published after the 2014 April AADL meeting hold in
Santa Barbara, USA.

#### Release

  - **GIT tag**: 2.0.6-RELEASE
  - **Release date**: Apr, 28 2014
  - **Eclipse base version**: Kepler
  - **Eclipse Update-Site**:
    <http://www.aadl.info/aadl/osate/stable/2.0.6/update-site>
  - **Download URL**:
    <http://www.aadl.info/aadl/osate/stable/2.0.6/products>

#### Known issues

1.  Using the update site, under Windows7 you may have a file protection
    issue for your installation. Eclipse update is just silently failing
    to update rather than reporting "permission denied." Please check
    the date of the installed OSATE feature (Open Source AADL Tool
    Environment) under Help-\>About and then Installation Details. If it
    did not get updated to the most recent date, please change your
    permissions.
2.  Using the update site, when you are in OSATE (Eclipse) and just
    checked an update site for updates, Eclipse caches that information.
    If someone tells you about a new release on the update site, please
    exit and reenter OSATE so it will actually find the new release.

#### Major changes

1.  Integration of the Graphical Editor
2.  New safety analysis tools

### Version 2.0.5

This release was published after the 2014 February AADL meeting hold in
Toulouse, France.

#### Release

  - **GIT tag**: 2.0.5-RELEASE-201402040847
  - **Release date**: February 4, 2014.
  - **Eclipse base version**: Kepler
  - **Eclipse Update-Site**:
    <http://www.aadl.info/aadl/osate/stable/2.0.5/update-site>
  - **Download URL**:
    <http://www.aadl.info/aadl/osate/stable/2.0.5/products>

#### Known issues

1.  Using the update site, under Windows7 you may have a file protection
    issue for your installation. Eclipse update is just silently failing
    to update rather than reporting "permission denied." Please check
    the date of the installed OSATE feature (Open Source AADL Tool
    Environment) under Help-\>About and then Installation Details. If it
    did not get updated to the most recent date, please change your
    permissions.
2.  Using the update site, when you are in OSATE (Eclipse) and just
    checked an update site for updates, Eclipse caches that information.
    If someone tells you about a new release on the update site, please
    exit and reenter OSATE so it will actually find the new release.

#### Changes and new features

1.  ResolvePrototypeUtil - FeatureGroupPrototypeActual support -
    <https://github.com/osate/osate2-core/issues/285>
2.  Constant property declaration using user-defined property set is not
    working - <https://github.com/osate/osate2-core/issues/286>
3.  Data\_Volume property not defined in AADL\_Project.aadl -
    <https://github.com/osate/osate2-core/issues/287>
4.  standard properties are no longer parsed -
    <https://github.com/osate/osate2-core/issues/302>
5.  Instantiated subcomponent has a component type only" error message -
    <https://github.com/osate/osate2-core/issues/301>
6.  Concrete Syntax Validation Error -
    <https://github.com/osate/osate2-core/issues/299>
7.  Connections are not required to have names -
    <https://github.com/osate/osate2-core/issues/298>
8.  getLocationReference() always returns null -
    <https://github.com/osate/osate2-core/issues/295>
9.  newFormal must be an instance of ComponentPrototype -
    <https://github.com/osate/osate2-core/issues/293>
10. Connection Refinement Issue -
    <https://github.com/osate/osate2-core/issues/291>
11. EMV2.aadl being included with OSATE -
    <https://github.com/osate/osate2-core/issues/290>
12. Mode Transition Trigger Port Reference Issue -
    <https://github.com/osate/osate2-core/issues/289>
13. Cannot resolve units type in constant declaration -
    <https://github.com/osate/osate2-core/issues/288>
14. Connection id is now mandatory -
    <https://github.com/osate/osate2-core/issues/304>
15. add nullity test to "upfgt" in Aadl2InstanceUtil.isSame -
    <https://github.com/osate/osate2-core/issues/305>
16. Issue with Xtext Grammar/Meta Model -
    <https://github.com/osate/osate2-core/issues/306>
17. System subcomponents become Abstract when instantiated -
    <https://github.com/osate/osate2-core/issues/307>
18. Typo in Metamodel -
    <https://github.com/osate/osate2-core/issues/308>
19. Hybrid and Timed literals do not exist in AadlProject -
    <https://github.com/osate/osate2-core/issues/309>
20. OSATE allows subprograms to provide data access -
    <https://github.com/osate/osate2-core/issues/310>
21. getSubcomponentType does not invoke eIsProxy if subcomponentType is
    null... - <https://github.com/osate/osate2-core/issues/311>
22. Question on connecting 'out data port' to 'requires data access' -
    <https://github.com/osate/osate2-core/issues/312>
23. Extra natures added to the Plugin\_Resources project are always
    removed at startup. -
    <https://github.com/osate/osate2-core/issues/319>
24. The name of a subcomponent should be set to null whenever its
    refined subcomponent is set to a non null value. -
    <https://github.com/osate/osate2-core/issues/320>
25. AADL package section elements have a null qualified name. -
    <https://github.com/osate/osate2-core/issues/321>
26. AADL navigator content provider throws null pointer exception for
    the Plugin\_Resources project. -
    <https://github.com/osate/osate2-core/issues/322>
27. AnnexParserAgent.java -
    <https://github.com/osate/osate2-core/pull/284>
28. Error when defining bus binding -
    <https://github.com/osate/ErrorModelV2/issues/39>
29. FHA cannot be generated when using error type -
    <https://github.com/osate/ErrorModelV2/issues/38>

### Version 2.0.4

This release was published after the 2013 Fall AADL meeting hold in
Montreal, Canada.

#### Release

  - **GIT tag**: 2.0.4-RELEASE-201309240847
  - **Release date**: September, 24 2013
  - **Eclipse base version**: Kepler
  - **Eclipse Update-Site**:
    <http://www.aadl.info/aadl/osate/stable/2.0.4/update-site>
  - **Download URL**:
    <http://www.aadl.info/aadl/osate/stable/2.0.4/products>

#### Known issues

1.  Using the update site, under Windows7 you may have a file protection
    issue for your installation. Eclipse update is just silently failing
    to update rather than reporting "permission denied." Please check
    the date of the installed OSATE feature (Open Source AADL Tool
    Environment) under Help-\>About and then Installation Details. If it
    did not get updated to the most recent date, please change your
    permissions.
2.  Using the update site, when you are in OSATE (Eclipse) and just
    checked an update site for updates, Eclipse caches that information.
    If someone tells you about a new release on the update site, please
    exit and reenter OSATE so it will actually find the new release.
3.  If you updated an old Juno installation, you should also add the
    Kepler update site so that the Kepler dependencies can be updated as
    well.

#### Changes and new features

  - EMV2.aadl being included with OSATE -
    <https://github.com/osate/osate2-core/issues/290>
  - Cannot resolve units type in constant declaration -
    <https://github.com/osate/osate2-core/issues/288>
  - Data\_Volume property not defined in AADL\_Project.aadl -
    <https://github.com/osate/osate2-core/issues/287>
  - Constant property declaration using user-defined property set is not
    working - <https://github.com/osate/osate2-core/issues/286>
  - ResolvePrototypeUtil - FeatureGroupPrototypeActual support -
    <https://github.com/osate/osate2-core/issues/285>
  - ResolvePrototypeUtil.resolveFeaturePrototype always returns null -
    <https://github.com/osate/osate2-core/issues/281>
  - Adding a property fails -
    <https://github.com/osate/osate2-core/issues/279>
  - property edition: unit are not recognized -
    <https://github.com/osate/osate2-core/issues/278>
  - Feature Group Connections. Invalid inverse connection is allowed. -
    <https://github.com/osate/osate2-core/issues/276>
  - NullPointerException at
    org.osate.aadl2.properties.PropertyAcc.addLocalContained(PropertyAcc.java:107)
      - <https://github.com/osate/osate2-core/issues/275>
  - GetProperties::getDelayedUnitLiteral always returns null. -
    <https://github.com/osate/osate2-core/issues/273>
  - org.eclipse.sphinx.emf needed and not found -
    <https://github.com/osate/osate2-core/issues/271>
  - Unable to Instantiate System/Qualified names are not unique -
    <https://github.com/osate/osate2-core/issues/270>
  - Defining a property delete other components -
    <https://github.com/osate/osate2-core/issues/268>
  - Refreshing property values -
    <https://github.com/osate/osate2-core/issues/267>
  - Adding a property on a component fails and triggers an exception -
    <https://github.com/osate/osate2-core/issues/266>
  - Most-Recent Develop Build Omits Plug-In Launch(es) -
    <https://github.com/osate/osate2-core/issues/265>
  - Instantiation Warning Not Helpful: Instantiated subcomponent has a
    component type only -
    <https://github.com/osate/osate2-core/issues/264>
  - Update to Kepler - <https://github.com/osate/osate2-core/issues/263>
  - Properties already defined are not shown -
    <https://github.com/osate/osate2-core/issues/261>
  - Cannot add a property value -
    <https://github.com/osate/osate2-core/issues/260>
  - error when building osate -
    <https://github.com/osate/osate2-core/issues/258>
  - Instance Model Viewer: Keep User Position Changes When Inserting
    Subcomponents - <https://github.com/osate/osate2-core/issues/257>
  - Types that are allows in global index are too restrictive. -
    <https://github.com/osate/osate2-core/issues/256>
  - AADL Properties View Issues -
    <https://github.com/osate/osate2-core/issues/254>
  - Setting the type of component implementations and the extended
    component for types and implementations throws unsupported operation
    exception. - <https://github.com/osate/osate2-core/issues/253>
  - Checking properties for connection instances -
    <https://github.com/osate/osate2-core/issues/252>
  - FHA cannot be generated when using error type -
    <https://github.com/osate/ErrorModelV2/issues/38>
  - add severity and likelhood in the hazard record -
    <https://github.com/osate/ErrorModelV2/issues/36>
  - Fail to parse the annex content when not using types -
    <https://github.com/osate/ErrorModelV2/issues/26>
  - Cannot specify the type associated to a state in the composite model
      - <https://github.com/osate/ErrorModelV2/issues/27>
  - Property not being inherited -
    <https://github.com/osate/ErrorModelV2/issues/34>
  - Properties for refined components -
    <https://github.com/osate/ErrorModelV2/issues/35>

### Version 2.0.3

This release was published after the 2013 Summer AADL meeting hold in
Pittsburgh, USA.

#### Release

  - **GIT tag**: 2.0.3-RELEASE-201307220847
  - **Release date**: July, 22 2013
  - **Eclipse base version**: Juno - 4.2
  - **Eclipse Update-Site**:
    <http://www.aadl.info/aadl/osate/stable/2.0.3/update-site>
  - **Download URL**:
    <http://www.aadl.info/aadl/osate/stable/2.0.3/products>
  - **Number of commits since the last stable**: 383

#### Known issues

1.  Using the update site, under Windows7 you may have a file protection
    issue for your installation. Eclipse update is just silently failing
    to update rather than reporting "permission denied." Please check
    the date of the installed OSATE feature (Open Source AADL Tool
    Environment) under Help-\>About and then Installation Details. If it
    did not get updated to the most recent date, please change your
    permissions.
2.  Using the update site, when you are in OSATE (Eclipse) and just
    checked an update site for updates, Eclipse caches that information.
    If someone tells you about a new release on the update site, please
    exit and reenter OSATE so it will actually find the new release.

#### Changes and new features

  - PRISM export now supports error propagation
  - Updated Error Model Support
  - Property editor updated and refined
  - Integration of Sphinx, contribution from Geensyde

#### Issues closed

  - Connection instances not created for feature group connection -
    <https://github.com/osate/osate2-core/issues/228>
  - annex subclauses are not parsed in feature group type -
    <https://github.com/osate/osate2-core/issues/227>
  - Subprogram Problem -
    <https://github.com/osate/osate2-core/issues/226>
  - Error when connecting array of subcomponents -
    <https://github.com/osate/osate2-core/issues/225>
  - Connection instances not created for feature group connection -
    <https://github.com/osate/osate2-core/issues/228>
  - ModelLoadingAdapter returns null instead of a model -
    <https://github.com/osate/osate2-core/issues/229>
  - Update ModelLoadingAdapter.java -
    <https://github.com/osate/osate2-core/issues/230>
  - property parsing error -
    <https://github.com/osate/osate2-core/issues/231>
  - ConnectionReferences in ConnectionInstance is incorrect for arrays -
    <https://github.com/osate/osate2-core/issues/232>
  - Properties Viewer throws null pointer exception -
    <https://github.com/osate/osate2-core/issues/233>
  - when feature group is defined via prototype the connection instances
    connect as if all\_to\_all -
    <https://github.com/osate/osate2-core/issues/235>
  - AnalysisModel does not take bindings information into account -
    <https://github.com/osate/osate2-core/issues/238>
  - Add Preference to turn off \*all\* Xtext background operations until
    file save - <https://github.com/osate/osate2-core/issues/239>
  - Call to getType on AbstractImplementation classifier causes a stack
    trace overflow. - <https://github.com/osate/osate2-core/issues/240>
  - Error when defining a property that applies to package -
    <https://github.com/osate/osate2-core/issues/241>
  - Request - API to retrieve NamedElement by qualified name -
    <https://github.com/osate/osate2-core/issues/242>
  - index order in Connection\_Set issue -
    <https://github.com/osate/osate2-core/issues/243>
  - Calling methods EMFIndexRetrieval too early can cause exception. -
    <https://github.com/osate/osate2-core/issues/244>
  - ConnectionReference holds incorrect values when arrays are involved
      - <https://github.com/osate/osate2-core/issues/245>
  - References to AADL model elements from models of other meta-models
    are shifted when elements are deleted / added in the AADL
    declarative model. -
    <https://github.com/osate/osate2-core/issues/247>
  - Class cast exception thrown when resolving some derived references
    of the meta-model. -
    <https://github.com/osate/osate2-core/issues/248>
  - Setting the name of a package section throws an unsuported operation
    exception and causes problems for model merge.. -
    <https://github.com/osate/osate2-core/issues/249>
  - EcoreUtil.equals does not work on Generalizations -
    <https://github.com/osate/osate2-core/issues/250>
  - connection between data and a subcomponent inside an other data -
    <https://github.com/osate/osate2-core/issues/251>
  - Instance Model Viewer: Keep User Position Changes When Inserting
    Subcomponents - <https://github.com/osate/osate2-core/issues/257>
  - bindings information in AnalysisModel -
    <https://github.com/osate/ErrorModelV2/issues/22>
  - Check of duplicate flow identifiers -
    <https://github.com/osate/ErrorModelV2/issues/23>
  - EM2TypeSetUtil.contains improvement -
    <https://github.com/osate/ErrorModelV2/issues/24>
  - Fail to parse the annex content when not using types -
    <https://github.com/osate/ErrorModelV2/issues/26>
  - Cannot specify the type associated to a state in the composite model
      - <https://github.com/osate/ErrorModelV2/issues/27>

### Version 2.0.2

This release is published after the 2013 Spring AADL meeting hold in
Jacksonville, USA. Please note that this release changed also the
structure of our download area. The testing update site is now available
on <http://www.aadl.info/aadl/osate/testing/>

#### Release

  - **GIT tag**: 2.0.2-RELEASE-201304300847
  - **Release date**: April, 30 1013
  - **Eclipse base version**: Juno version **4.2.2**
  - **Eclipse Update-Site**:
    <http://www.aadl.info/aadl/osate/stable/2.0.2/update-site>
  - **Download URL**:
    <http://www.aadl.info/aadl/osate/stable/2.0.2/products>
  - Number of commits since the last stable: 283 (194 on the core) and
    89 on the plugins.

#### Known issues

1.  Using the update site, under Windows7 you may have a file protection
    issue for your installation. Eclipse update is just silently failing
    to update rather than reporting "permission denied." Please check
    the date of the installed OSATE feature (Open Source AADL Tool
    Environment) under Help-\>About and then Installation Details. If it
    did not get updated to the most recent date, please change your
    permissions.
2.  Using the update site, when you are in OSATE (Eclipse) and just
    checked an update site for updates, Eclipse caches that information.
    If someone tells you about a new release on the update site, please
    exit and reenter OSATE so it will actually find the new release.

#### Changes and new features

  - Integration of the Property View
  - Integration of the IMV viewer with error-model annex
  - Add the Markov-Chain export for the Error-Model
  - Add the Reliability Block Diagram analysis tool for the Error-Model
  - Add the Fault-Tree Analysis tool for the Error-Model
  - Improvements of the Fault Hazard Assessment
  - Clean up the AADL perspective, analysis function being available
    only when using AADL view

#### Issues closed

1.  Using Xtext to create annex-
    <https://github.com/osate/osate2-core/issues/224>
2.  Instanciation exception when using connection datasubcomponent -\>
    call.dataaccess - <https://github.com/osate/osate2-core/issues/222>
3.  inconsistent kind between flow spec and implementation not detected
      - <https://github.com/osate/osate2-core/issues/221>
4.  Instanciation exception when using connection datasubcomponent -\>
    call.parameter - <https://github.com/osate/osate2-core/issues/220>
5.  ConnectionKind in AADL2 Meta model -
    <https://github.com/osate/osate2-core/issues/215>
6.  mode specific property values in instance model -
    <https://github.com/osate/osate2-core/issues/214>
7.  AADL BA wizard examples -
    <https://github.com/osate/osate2-core/issues/212>
8.  conflicting handlers when invoking Content Assist -
    <https://github.com/osate/osate2-core/issues/211>
9.  clock\_period and clock\_period\_range should apply to device -
    <https://github.com/osate/osate2-core/issues/210>
10. Instence creation with prototype binding does not work -
    <https://github.com/osate/osate2-core/issues/209>
11. flow latency calculation not correct for components without flow
    spec - <https://github.com/osate/osate2-core/issues/207>
12. flow implementation without connections accepted without warning or
    error - <https://github.com/osate/osate2-core/issues/206>
13. property association not created in instance model -
    <https://github.com/osate/osate2-core/issues/205>
14. Missing connection instances -
    <https://github.com/osate/osate2-core/issues/204>
15. User Interface Improvements -
    <https://github.com/osate/osate2-core/issues/203>
16. ProeprtyView icon not found -
    <https://github.com/osate/osate2-core/issues/202>
17. Resolution of Device\_Driver property -
    <https://github.com/osate/osate2-core/issues/200>
18. patch proposal - <https://github.com/osate/osate2-core/issues/199>
19. Features direction for subprogram ports and thread ports -
    <https://github.com/osate/osate2-core/issues/198>
20. (Modified) Plugin\_Resources not updated upon 'Create/update
    Predeclared and Annex Properties'' -
    <https://github.com/osate/osate2-core/issues/197>
21. flow path reports incrrectly that the port direction is wrong -
    <https://github.com/osate/osate2-core/issues/196>
22. The AADL meta-models are not declared in the EMF package registry
    for the development time version. -
    <https://github.com/osate/osate2-core/issues/195>
23. Last Connection Reference of a Connection Instance generated from a
    bidirectional feature group bug -
    <https://github.com/osate/osate2-core/issues/194>
24. Aadl Property Viewer does not show values on virtual processor in
    instance model - <https://github.com/osate/osate2-core/issues/193>
25. Some new operations in the meta-model are not implemented in the
    Java classes. - <https://github.com/osate/osate2-core/issues/192>
26. null pointer error on OSATE startup when AADL Properties view is
    open - <https://github.com/osate/osate2-core/issues/191>
27. requires subprogram access causes parsing error -
    <https://github.com/osate/osate2-core/issues/189>
28. osate2-core now has dependency to ErrorModelV2 -
    <https://github.com/osate/osate2-core/issues/188>
29. Problems with classifier matching rules on refined subcomponents. -
    <https://github.com/osate/osate2-core/issues/182>
30. for bidirectional feature group connections false warning about no
    ingoing connection -
    <https://github.com/osate/osate2-core/issues/184>
31. Can wrap illegal features inside legal feature groups -
    <https://github.com/osate/osate2-core/issues/185>
32. class cast exception in validator -
    <https://github.com/osate/osate2-core/issues/186>
33. FlowSpecificationInstance no longer has Source and Destination
    assigned - <https://github.com/osate/osate2-core/issues/187>

### Version 2.0.1

This release is published after the Winter AADL meeting hold on
Valencia, Spain. We thank again our host for hosting this event.

##### Release

  - **GIT tag**: 2.0.1-RELEASE-201302141024
  - **Release date**: 2013, Feb 14
  - **Eclipse base version**: Juno version **4.2.1**
  - **Eclipse Update-Site**:
    <http://www.aadl.info/aadl/osate/stable/2.0.1/update-site>
  - **Download URL**:
    <http://www.aadl.info/aadl/osate/stable/2.0.1/products>

##### Known issues

1.  Using the update site, under Windows7 you may have a file protection
    issue for your installation. Eclipse update is just silently failing
    to update rather than reporting "permission denied." Please check
    the date of the installed OSATE feature (Open Source AADL Tool
    Environment) under Help-\>About and then Installation Details. If it
    did not get updated to the most recent date, please change your
    permissions.
2.  Using the update site, when you are in OSATE (Eclipse) and just
    checked an update site for updates, Eclipse caches that information.
    If someone tells you about a new release on the update site, please
    exit and reenter OSATE so it will actually find the new release.

##### Changes and new features

  - LUTE integration in AADL plug-ins
  - Instance Model Viewer Integration
  - Error Model Annex v1
  - Error Model Annex v2
  - Integration of Ocarina specific property sets
  - Migration to Eclipse/Juno
  - ARINC653 validation functions
  - Support for ARINC653 annex
  - Update of help content within Eclipse (with Java API, plugins
    description, etc.)
  - User feedback when model instantiation fails
  - System Instance can be validated using EMF
  - Property viewer integration
  - Reference Manual integration

##### Bugfixes

1.  Subprogram implementations in call sequences
    (https://github.com/osate/osate2-core/issues/181)
2.  Flows through feature groups (cf.
    <https://github.com/osate/osate2-core/issues/179>)
3.  subcomponent reference required in system instance
    (https://github.com/osate/osate2-core/issues/142)
4.  duplicate flow implementations not reported
    (https://github.com/osate/osate2-core/issues/164)
5.  Implement classifier matching rule other than default rule
    (https://github.com/osate/osate2-core/issues/69)
6.  Semantic checking of flows
    (https://github.com/osate/osate2-core/issues/67)
7.  Semantic checking of access connections
    (https://github.com/osate/osate2-core/issues/66)
8.  Requires subprogram in feature group prototype
    (https://github.com/osate/osate2-core/issues/166)
9.  Nested inverse of feature groups
    (https://github.com/osate/osate2-core/issues/177)
10. Connection Instance property when Multiple properties exist, only
    creates one in certain cases.
    (https://github.com/osate/osate2-core/issues/178)
11. ForAllElement.defaultTraversalAllDeclarativeModels() not working
    (https://github.com/osate/osate2-core/issues/169)
12. Error instantiating model
    (https://github.com/osate/osate2-core/issues/176)
13. AADL connection instance property. "applies to" does not work.
    (https://github.com/osate/osate2-core/issues/174)
14. DATA\_VOLUME\_UNITS is now defined in AADL\_Project
15. AADL\_Project.java file need update for Data\_Volume\_Units
    (https://github.com/osate/osate2-core/issues/173)
16. Invalid ConnectionInstance property value
    (https://github.com/osate/osate2-core/issues/171)
17. Property Association Missing in instantiation -
    <https://github.com/osate/osate2-core/issues/168>
18. Access features are missing the super class of the specific category
    in the Meta model -
    <https://github.com/osate/osate2-core/issues/167>
19. Instantiation error (regression); trace suggests it comes from the
    process component -
    <https://github.com/osate/osate2-core/issues/172>
20. Naming resolution error: subprogram call context not found -
    <https://github.com/osate/osate2-core/issues/170>
21. Incorrect error reporting: "Value for property.. is inconsistent
    along connection" -
    <https://github.com/osate/osate2-core/issues/158>
22. Menu item failures from 2013-01-30 Development Branch. -
    <https://github.com/osate/osate2-core/issues/165>
23. Support of Juno - <https://github.com/osate/osate2-core/issues/139>
24. Cyclic reference error when typing in an alias (renames) -
    <https://github.com/osate/osate2-core/issues/163>
25. Exception when Instantiating System with Warning -
    <https://github.com/osate/osate2-core/issues/162>
26. Type mis-match warning on correct connection -
    <https://github.com/osate/osate2-core/issues/155>
27. Error when instantiating the model -
    <https://github.com/osate/osate2-core/issues/156>
28. Incorrect message for feature direction in flow implementation -
    <https://github.com/osate/osate2-core/issues/161>
29. Incorrect error message on flow between elements of feature groups -
    <https://github.com/osate/osate2-core/issues/160>
30. Error in org.osate.imv.propertydecorations.threads -
    <https://github.com/osate/osate2-core/issues/159>
31. Support for subprogram implementation -
    <https://github.com/osate/osate2-core/issues/153>
32. Visibility differs in subcomponent declaration versus properties
    section - <https://github.com/osate/osate2-core/issues/152>
33. Illegal refinement of category type allowed -
    <https://github.com/osate/osate2-core/issues/150>
34. Instance model error -
    <https://github.com/osate/osate2-core/issues/151>
35. Package visible without being withed -
    <https://github.com/osate/osate2-core/issues/149>
36. Property association classifier type -
    <https://github.com/osate/osate2-core/issues/148>
37. setPropertyValue method in NamedElementImpl -
    <https://github.com/osate/osate2-core/issues/59>
38. Formatting (via I or format command seems to loose the text in
    annexes. - <https://github.com/osate/osate2-core/issues/145>
39. Subset matching for feature group is not supported yet -
    <https://github.com/osate/osate2-core/issues/107>
40. renames causes cyclic lazy resolution -
    <https://github.com/osate/osate2-core/issues/143>
41. Checking type of reference value and classifier value -
    <https://github.com/osate/osate2-core/issues/68>
42. Property constant as value in range -
    <https://github.com/osate/osate2-core/issues/129>
43. Bus classifier not recognized in bus access connection for refined
    features. - <https://github.com/osate/osate2-core/issues/121>
44. Local path in target definition -
    <https://github.com/osate/osate2-core/issues/7>
45. Instance model corrupted when error occurs -
    <https://github.com/osate/osate2-core/issues/135>
46. Verification of duplicate elements -
    <https://github.com/osate/osate2-core/issues/141>
47. Instanciation error with Compute\_Execution\_Time property -
    <https://github.com/osate/osate2-core/issues/140>
48. Check for duplicate packages too restrictive -
    <https://github.com/osate/osate2-core/issues/91>
49. Default port "Complete" is not working -
    <https://github.com/osate/osate2-core/issues/114>
50. Property association omitted at instantiation of virtual processors
      - <https://github.com/osate/osate2-core/issues/126>
51. Inconsistent literals for properties -
    <https://github.com/osate/osate2-core/issues/45>
52. Property sets for AADL annexes -
    <https://github.com/osate/osate2-core/issues/64>
53. Subprogam call name resolution -
    <https://github.com/osate/osate2-core/issues/127>
54. Record values surrounded with () vs. \[\] is inconsistent -
    <https://github.com/osate/osate2-core/issues/137>
55. Non-existent qualified name for a property -
    <https://github.com/osate/osate2-core/issues/138>
56. Enumeration literal not recognized -
    <https://github.com/osate/osate2-core/issues/133>
57. EValidator error when property constant is used as value -
    <https://github.com/osate/osate2-core/issues/134>
58. Incorrect error msg: "Connection between two components that inherit
    features is not supported" -
    <https://github.com/osate/osate2-core/issues/136>
59. Error with OSATE views -
    <https://github.com/osate/osate2-core/issues/128>
60. Bug with creating the connection instance with abstract component -
    <https://github.com/osate/osate2-core/issues/118>
61. About dialog is outdated -
    <https://github.com/osate/osate2-core/issues/123>
62. Method "acceptsProperty" in ComponentInstanceImpl always return true
    whatever the property is. -
    <https://github.com/osate/osate2-core/issues/122>
63. Property applicability clause to classifiers not recognized. -
    <https://github.com/osate/osate2-core/issues/120>
64. Discrepancy between ModeTransition ecore class and Java class -
    <https://github.com/osate/osate2-core/issues/124>
65. OsateResourceUtil bug? -
    <https://github.com/osate/osate2-core/issues/42>
66. Propertyset projects have been replaced by properties projects, this
    has... - <https://github.com/osate/osate2-core/pull/125>
67. Exception at ConnectionInstanceImpl.java (Line 843) -
    <https://github.com/osate/osate2-core/issues/112>
68. null pointer exception on hashcode of PropertyImpl -
    <https://github.com/osate/osate2-core/issues/130>
69. Duplicate Element 'mils\_example' in PublicPackageSection
    'Test\_Package' example.aadl -
    <https://github.com/osate/osate2-core/issues/132>
70. Handling of instantiating a System when the model has errors. -
    <https://github.com/osate/osate2-core/issues/77>
71. Array size via property value -
    <https://github.com/osate/osate2-core/issues/89>
72. Workspace synchronization when instanciate several systems -
    <https://github.com/osate/osate2-core/issues/119>
73. Meta model support for contaiment path in core AADL with annex
    specific segments -
    <https://github.com/osate/osate2-core/issues/146>

This page uses the [Cayman
theme](https://github.com/jasonlong/cayman-theme) by [Jason
Long](https://twitter.com/jasonlong).

