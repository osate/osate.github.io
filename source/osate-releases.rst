Release Notes
=============

Stable Releases
---------------

Version 2.11.0
~~~~~~~~~~~~~~

Release
^^^^^^^

-  **GIT tag**: 2.11.0-RELEASE
-  **Release date**: June 16, 2022
-  **Eclipse base version**: 2022-03
-  **Java version**: Java 17
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.11.0/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.11.0/products

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   f9764b7db6b923812a759b6190b0dec1ba06827fb2bdd808ee4f716d27a190e7  osate2-2.11.0-vfinal-linux.gtk.x86_64.tar.gz
   825cda0c902d648a9130e4af456da85bfe894c7a34d2a98cb83125821c979141  osate2-2.11.0-vfinal-macosx.cocoa.aarch64.tar.gz
   780e842da13f083dc12467bf51cf275b26d57a6f5048665e30e935ea81c53e9c  osate2-2.11.0-vfinal-macosx.cocoa.x86_64.tar.gz
   9990f9d23605b773da33068d976505bb36f27f61fc3c132a0cb3d83f36c6945d  osate2-2.11.0-vfinal-win32.win32.x86_64.zip

Notable changes
^^^^^^^^^^^^^^^

-  This version contains the first part of an instantiatior for error model annex subclauses. This functionality 
   is experimental and can be enabled by adding a line ``-Dorg.osate.emv2.instance=true`` to the _osate.ini_ file.
-  OSATE now requires Java 17. It comes with an embedded JVM version 17.0.3.
-  We have added an OSATE build for Apple silicon

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Add ACVIP Example
       (`2586 <https://github.com/osate/osate2/issues/2586>`__)
   2.  Generated property getter methods don't handle the case when the property doesn't apply
       (`2593 <https://github.com/osate/osate2/issues/2593>`__)
   3.  Annexes should be able to use a customized resource description strategy
       (`2751 <https://github.com/osate/osate2/issues/2751>`__)
   4.  Improve annex instantiation API
       (`2769 <https://github.com/osate/osate2/issues/2769>`__)
   5.  ConnectionReference not instantiated properly for reach down into feature groups
       (`2773 <https://github.com/osate/osate2/issues/2773>`__)
   6.  FTA fails on example model
       (`2772 <https://github.com/osate/osate2/issues/2772>`__)
   7.  Bound resource allocations analysis report not generated
       (`2782 <https://github.com/osate/osate2/issues/2782>`__)
   8.  Update to Eclipse 2022-03 and Xtext 2.26
       (`2724 <https://github.com/osate/osate2/issues/2724>`__)
   9.  Build uses outdated spotbugs version
       (`2752 <https://github.com/osate/osate2/issues/2752>`__)
   10. Add version for Apple silicon
       (`2774 <https://github.com/osate/osate2/issues/2774>`__)
   11. EASE dependency incorrect
       (`2799 <https://github.com/osate/osate2/issues/2799>`__)

-  Error Model and Analysis Plugins

   1.  Incorrect global scope for error model
       (`2750 <https://github.com/osate/osate2/issues/2750>`__)
   2.  Instantiate basic EMV2 elements
       (`2802 <https://github.com/osate/osate2/issues/2802>`__)

-  Graphical Editor

   1.  Add API for building JavaFX scene graph for transient diagram views
       (`2778 <https://github.com/osate/osate2/issues/2778>`__)
   2.  Graphical editor can throw concurrent modification exception when laying out docked nodes
       (`2795 <https://github.com/osate/osate2/issues/2795>`__)
       
Known issues
^^^^^^^^^^^^

-  MacOS users must run the command
   ``sudo xattr -rd com.apple.quarantine osate2.app/`` to be able to run
   OSATE.
-  Installing from the update site into an existing Eclipse requires additional
   steps (see https://groups.google.com/g/osate/c/Hpw6wX_GND4)
-  Installing the OSATE plugins into “Eclipse for RCP and RAP
   Developers” may prevent Eclipse from starting. See `issue
   2061 <https://github.com/osate/osate2/issues/2061>`__.
-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.11.0 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.

Version 2.10.2
~~~~~~~~~~~~~~

Release
^^^^^^^

-  **GIT tag**: 2.10.2-RELEASE
-  **Release date**: February, 2022
-  **Eclipse base version**: 2021-03
-  **Java version**: Java 11
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.10.2/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.10.2/products

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   c7c1b21f58fde881a088ed11d9ac66186c96029884fa551fda4ea31742f4e2a1  osate2-2.10.2-vfinal-linux.gtk.x86_64.tar.gz
   7a80741ab2a45ea74ef5d24ff7500350a20cb8f8879d5efa7af86e20b1c1adad  osate2-2.10.2-vfinal-macosx.cocoa.x86_64.tar.gz
   31090f0571451f939c78c546b715fa02596ff10996358ae44f709942bb63b5de  osate2-2.10.2-vfinal-win32.win32.x86_64.zip

Notable changes
^^^^^^^^^^^^^^^

-  We have added a new preference setting to disable processing of selected annexes

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Add a way to disable unused contributed property sets and packages
       (`2474 <https://github.com/osate/osate2/issues/2474>`__)
   2.  Generated property getter methods don't handle the case when the property doesn't apply
       (`2593 <https://github.com/osate/osate2/issues/2593>`__)
   3.  Missing icons for instance objects
       (`2596 <https://github.com/osate/osate2/issues/2596>`__)
   4.  Use better icons for *.aadl and *.aaxl2 files
       (`2598 <https://github.com/osate/osate2/issues/2598>`__)
   5.  NPE when instantiating when file not saved
       (`2613 <https://github.com/osate/osate2/issues/2613>`__)
   6.  Generate Getters for Property Constants
       (`2632 <https://github.com/osate/osate2/issues/2632>`__)
   7.  Missing validation for reserved thread ports
       (`2652 <https://github.com/osate/osate2/issues/2652>`__)
   8.  OSATE does not allow multiple call sequences in threads
       (`2718 <https://github.com/osate/osate2/issues/2718>`__)
   9.  ConnectionInstances need to consider the modes of the endpoints
       (`2722 <https://github.com/osate/osate2/issues/2722>`__)
   10. OSATE doesn't support dropins directory to install plugins
       (`2727 <https://github.com/osate/osate2/issues/2727>`__)
   11. Generate Javadoc during build
       (`2185 <https://github.com/osate/osate2/issues/2185>`__)
   12. Remove build dependency on jboss repository-utils maven plugin
       (`2710 <https://github.com/osate/osate2/issues/2710>`__)
   13. Update Java from 11.0.2 to 11.0.12
       (`2729 <https://github.com/osate/osate2/issues/2729>`__)
   14. Update to Java 11.0.13
       (`2745 <https://github.com/osate/osate2/issues/2745>`__)
   15. Bundled JVM has larger size than necessary
       (`2746 <https://github.com/osate/osate2/issues/2746>`__)

-  Error Model and Analysis Plugins

   1.  Exception when serializing EMV2 annex
       (`2648 <https://github.com/osate/osate2/issues/2648>`__)
   2.  An exception occurs during EMV2 serialization
       (`2690 <https://github.com/osate/osate2/issues/2690>`__)
       
Known issues
^^^^^^^^^^^^

-  MacOS users must run the command
   ``sudo xattr -rd com.apple.quarantine osate2.app/`` to be able to run
   OSATE.
-  Installing from the update site into an existing Eclipse requires additional
   steps (see https://groups.google.com/g/osate/c/Hpw6wX_GND4)
-  Installing the OSATE plugins into “Eclipse for RCP and RAP
   Developers” may prevent Eclipse from starting. See `issue
   2061 <https://github.com/osate/osate2/issues/2061>`__.
-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.10.2 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.

Version 2.10.1
~~~~~~~~~~~~~~

OSATE 2.10.1 had a build issue. We have removed the download and re-released the
corrected build as version 2.10.2.

Version 2.10.0
~~~~~~~~~~~~~~

Release
^^^^^^^

-  **GIT tag**: 2.10.0-RELEASE
-  **Release date**: October 8, 2021
-  **Eclipse base version**: 2021-03
-  **Java version**: Java 11
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.10.0/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.10.0/products

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   78312dd33458e0db5db0be039b561e9b26eb94e572ecfc9fc8ddf831f84405d9  osate2-2.10.0-vfinal-linux.gtk.x86_64.tar.gz
   a5c2d1ba693b231316798e763628e5f393f19f371ce730dc7d50e6724b227ad7  osate2-2.10.0-vfinal-macosx.cocoa.x86_64.tar.gz
   19ae0a9b984cfba06be976f6c4d26036590adad18276c3e2eb9b2cd8529c94d1  osate2-2.10.0-vfinal-win32.win32.x86_64.zip

Notable changes
^^^^^^^^^^^^^^^

-  Switched the underlying framework for the graphical editor.
-  This release requires Java 11. A Java 11 JDK is bundled with OSATE, so
   there is no need to install Java 11 separately.

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Upgrade to Eclipse 2021-03, Xtext 2.25, Xsemantics 1.20, Java 11
       (`2310 <https://github.com/osate/osate2/issues/2310>`__)
   2.  Wrong icons for calls and parameter connections
       (`2605 <https://github.com/osate/osate2/issues/2605>`__)
   3.  Update icons
       (`2611 <https://github.com/osate/osate2/issues/2611>`__)
   4.  Preference to ignore annex breaks standalone mode
       (`2693 <https://github.com/osate/osate2/issues/2693>`__)
   5.  Preference to ignore missing property set breaks standalone mode
       (`2695 <https://github.com/osate/osate2/issues/2695>`__)
   6.  Replace use of GetProperties with generated property getters in FlowAnalysis, and BusLoadAnalysis
       (`2574 <https://github.com/osate/osate2/issues/2574>`__)
   7.  Make NewAbstractAaxlHandler publicly visible
       (`2705 <https://github.com/osate/osate2/issues/2705>`__)
   8.  Latency CSV report cannot be written in standalone mode
       (`2707 <https://github.com/osate/osate2/issues/2707>`__)
   9.  Include JVM in OSATE download
       (`2420 <https://github.com/osate/osate2/issues/2420>`__)
 
-  Graphical Editor

   1.  Implement GEF based graphical editor
       (`1183 <https://github.com/osate/osate2/issues/1183>`__)
   2.  Provide opaque or obscuring background for text labels
       (`1184 <https://github.com/osate/osate2/issues/1184>`__)
   3.  Allow arbitrary positioning of ports on component exteriors
       (`1186 <https://github.com/osate/osate2/issues/1186>`__)
   4.  Indicate illegal object positions with halted intermediary representation
       (`1188 <https://github.com/osate/osate2/issues/1188>`__)
   5.  GE SVG Export isn't editable / high quality
       (`1461 <https://github.com/osate/osate2/issues/1461>`__)
   6.  Text can be clipped when zooming
       (`1547 <https://github.com/osate/osate2/issues/1547>`__)
   7.  In GE, action to change the orientation of buses
       (`2198 <https://github.com/osate/osate2/issues/2198>`__)
   8.  NPE when exporting diagrams as SVG
       (`2410 <https://github.com/osate/osate2/issues/2410>`__)
   9.  Behavior annex action is incorrectly displayed in graphical editor
       (`2655 <https://github.com/osate/osate2/issues/2655>`__)
   10. Allow flow tools to be used when there are warnings in referenced packages
       (`2663 <https://github.com/osate/osate2/issues/2663>`__)
   11. Layout exception is thrown for self loops on the same side
       (`2674 <https://github.com/osate/osate2/issues/2674>`__)
   12. Diagram export results in an empty image.
       (`2678 <https://github.com/osate/osate2/issues/2678>`__)
   13. 2683 Add missing icons to graphical editor
       (`2685 <https://github.com/osate/osate2/issues/2685>`__)
       
Known issues
^^^^^^^^^^^^

-  MacOS users must run the command
   ``sudo xattr -rd com.apple.quarantine osate2.app/`` to be able to run
   OSATE.
-  Installing the OSATE plugins into “Eclipse for RCP and RAP
   Developers” may prevent Eclipse from starting. See `issue
   2061 <https://github.com/osate/osate2/issues/2061>`__.
-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.10.0 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.

Version 2.9.2
~~~~~~~~~~~~~

Release
^^^^^^^

-  **GIT tag**: 2.9.2-RELEASE
-  **Release date**: June 8, 2021
-  **Eclipse base version**: 2020-06
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.9.2/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.9.2/products

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   2d34cc2bb6bef5296fa66b67e883aead2989cd5541254304fb4eedcb66750347  osate2-2.9.2-vfinal-linux.gtk.x86_64.tar.gz
   10ae6949046b21333c8bec251dd7d7e11892b5210652d880a410a3ac084f12f4  osate2-2.9.2-vfinal-macosx.cocoa.x86_64.tar.gz
   a74b0a6f8ed42900ddf23a4e3843e059733ea35a6bd931ad86ea4b3bbf2d4fd9  osate2-2.9.2-vfinal-win32.win32.x86_64.zip

Notable changes
^^^^^^^^^^^^^^^

-  There is a new preference setting to ignore an installed annex
   plugin.
-  Another new preference setting allows ignoring errors that are caused
   by a missing property set, e.g., when a model uses properties from a
   property set that is included in a plugin, but that plugin is not
   installed.
-  This is the last release that will work with Java 8. Starting with
   the next release OSATE will require Java 11.

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Flows in Subprogram Groups
       (`1563 <https://github.com/osate/osate2/issues/1563>`__)
   2.  Configuration flag for deactivating an annex
       (`2288 <https://github.com/osate/osate2/issues/2288>`__)
   3.  Add option to suppress errors related to missing property sets
       (`2478 <https://github.com/osate/osate2/issues/2478>`__)
   4.  Error in flow precedence with refining/extends
       (`2533 <https://github.com/osate/osate2/issues/2533>`__)
   5.  New JUnit tests sometimes fail on Jenkins
       (`2567 <https://github.com/osate/osate2/issues/2567>`__)
   6.  Generate property set accessor code for
       org.osate.contribution.sei
       (`2573 <https://github.com/osate/osate2/issues/2573>`__)
   7.  The warning squiggly line for “expected feature xxx to have
       classifier yyy” is placed under the wrong classifier
       (`2580 <https://github.com/osate/osate2/issues/2580>`__)
   8.  Example AADL Project label is missing
       (`2584 <https://github.com/osate/osate2/issues/2584>`__)
   9.  Mylyn is missing in the OSATE product build
       (`2585 <https://github.com/osate/osate2/issues/2585>`__)
   10. Missing error/warning markers in AADL navigator view
       (`2609 <https://github.com/osate/osate2/issues/2609>`__)
   11. Missing error/warning markers on instance model elements
       (`2612 <https://github.com/osate/osate2/issues/2612>`__)
   12. Update bus load analysis internal model to use ecore
       (`2555 <https://github.com/osate/osate2/issues/2555>`__)
   13. Add RAMSES to the list of installable components
       (`2056 <https://github.com/osate/osate2/issues/2056>`__)

-  Error Model and Analysis Plugins

   1. Error transition same state causes stack overflow
      (`2546 <https://github.com/osate/osate2/issues/2546>`__)
   2. Typeset with target state of error transition not marked as error
      (`2579 <https://github.com/osate/osate2/issues/2579>`__)
   3. Typeset used as target error type not marked as error
      (`2604 <https://github.com/osate/osate2/issues/2604>`__)

-  Graphical Editor

   1. Visualization and editing of behavior annex state automata
      (`2130 <https://github.com/osate/osate2/issues/2130>`__)
   2. Allow editing of behavior annex dispatch conditions
      (`2131 <https://github.com/osate/osate2/issues/2131>`__)
   3. Support for editing the behavior annex action language
      (`2132 <https://github.com/osate/osate2/issues/2132>`__)
   4. Assign names to behavior transitions created in the graphical
      editor (`2640 <https://github.com/osate/osate2/issues/2640>`__)

-  ALISA

   1. Reqtrace plugin uses inefficient property tester
      (`2498 <https://github.com/osate/osate2/issues/2498>`__)

-  Behavior Annex

   1. In BA plugin, fail referencing fields of a subprogram data access
      or input parameter when calling another one
      (`2466 <https://github.com/osate/osate2/issues/2466>`__)
   2. In the BA plugin, BehaviorVariable’s lose their DataClassifier’s
      namespace reference after modification
      (`2550 <https://github.com/osate/osate2/issues/2550>`__)
   3. In BA plugin, fail to open provided examples
      (`2583 <https://github.com/osate/osate2/issues/2583>`__)

Known issues
^^^^^^^^^^^^

-  MacOS users must run the command
   ``sudo xattr -rd com.apple.quarantine osate2.app/`` to be able to run
   OSATE.
-  Installing the OSATE plugins into “Eclipse for RCP and RAP
   Developers” may prevent Eclipse from starting. See `issue
   2061 <https://github.com/osate/osate2/issues/2061>`__.
-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.9.1 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.

Version 2.9.1
~~~~~~~~~~~~~

.. _release-1:

Release
^^^^^^^

-  **GIT tag**: 2.9.1-RELEASE
-  **Release date**: February 1, 2021
-  **Eclipse base version**: 2020-06
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.9.1/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.9.1/products

.. _sha256-hashes-for-the-downloads-1:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   11941a75b931a350a4459ce4d5c3c2acce17e5f3b34195fb9e57f4f6cc249790  osate2-2.9.1-vfinal-linux.gtk.x86_64.tar.gz
   bc0672e175a8190ff6cd1db1900bca970709e97addff35afd7f6c6591e0c1a6d  osate2-2.9.1-vfinal-macosx.cocoa.x86_64.tar.gz
   0b45fb174af6386d739e17d7a21570b2b3807324a0b14cb4ae95be81848296f3  osate2-2.9.1-vfinal-win32.win32.x86_64.zip

.. _notable-changes-1:

Notable changes
^^^^^^^^^^^^^^^

-  Performance improvements when handling larger models

   1. Expanding models in the navigator view is much faster
   2. Creation of context menu items no longer parses AADL source files
      behind the scenes
   3. OSATE no longer blocks the UI with a “Synchronizing EMF models”
      message after instantiation

-  Improved functionality of the classifier information view
-  The graphical editor now has partial error model annex support

.. _fixed-issues-1:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Add a keyboard shortcut for instantiation
       (`2074 <https://github.com/osate/osate2/issues/2074>`__)
   2.  Bidirectional feature group connection produces incorrect
       connection instance
       (`2318 <https://github.com/osate/osate2/issues/2318>`__)
   3.  Clean up the utility classes and methods
       (`2383 <https://github.com/osate/osate2/issues/2383>`__)
   4.  Can’t instantiate reference to property with default value
       (`2387 <https://github.com/osate/osate2/issues/2387>`__)
   5.  Flow implementation validation doesn’t check if the sequence is
       properly connected
       (`2416 <https://github.com/osate/osate2/issues/2416>`__)
   6.  Clean up plugin.xml “definition” extensions
       (`2418 <https://github.com/osate/osate2/issues/2418>`__)
   7.  Expanding AADL element in the AADL navigator is very slow
       (`2430 <https://github.com/osate/osate2/issues/2430>`__)
   8.  Rename refactoring of port misses references in flow
       implementations
       (`2434 <https://github.com/osate/osate2/issues/2434>`__)
   9.  Classifier information view is not updated when AADL text is
       edited and saved
       (`2435 <https://github.com/osate/osate2/issues/2435>`__)
   10. Classifier information view should show subtype hierarchy
       (`2436 <https://github.com/osate/osate2/issues/2436>`__)
   11. Open classifier information view from more places
       (`2439 <https://github.com/osate/osate2/issues/2439>`__)
   12. No icons for flows in outline view
       (`2440 <https://github.com/osate/osate2/issues/2440>`__)
   13. Missing flow implementation name in outline view
       (`2441 <https://github.com/osate/osate2/issues/2441>`__)
   14. No distinction between flow source/path/sink in outline view
       (`2442 <https://github.com/osate/osate2/issues/2442>`__)
   15. Implementation labels in outline view are too long
       (`2443 <https://github.com/osate/osate2/issues/2443>`__)
   16. OSATE hangs with “Synchronizing EMF models”
       (`2448 <https://github.com/osate/osate2/issues/2448>`__)
   17. Instantiation can be started while workspace is building
       (`2456 <https://github.com/osate/osate2/issues/2456>`__)
   18. Classifier information view doesn’t show unimplemented flow
       specifications
       (`2472 <https://github.com/osate/osate2/issues/2472>`__)
   19. Connections are expandable in the outline view
       (`2485 <https://github.com/osate/osate2/issues/2485>`__)
   20. Components without children are marked as having children in the
       outline (`2486 <https://github.com/osate/osate2/issues/2486>`__)
   21. Classifier Info View should show the contents of the classifier
       selected in the hierarchy tree
       (`2491 <https://github.com/osate/osate2/issues/2491>`__)
   22. Classifier Info View Leaves stray “goto” marker
       (`2496 <https://github.com/osate/osate2/issues/2496>`__)
   23. Annex parser throws exception on BA block beginning with LF.
       (`2497 <https://github.com/osate/osate2/issues/2497>`__)
   24. Import additional example models
       (`2536 <https://github.com/osate/osate2/issues/2536>`__)
   25. Packages are linking to the wrong default property set resources
       (`2537 <https://github.com/osate/osate2/issues/2537>`__)
   26. OSATE commands are hidden in the key bindings preferences
       (`2553 <https://github.com/osate/osate2/issues/2553>`__)
   27. Run analysis on implementation
       (`841 <https://github.com/osate/osate2/issues/841>`__)
   28. Formatting issues in flow latency analysis CSV report
       (`2427 <https://github.com/osate/osate2/issues/2427>`__)
   29. Flow latency analysis Excel report generates invalid worksheet
       names (`2428 <https://github.com/osate/osate2/issues/2428>`__)
   30. Checking binding constraints cannot be canceled
       (`2461 <https://github.com/osate/osate2/issues/2461>`__)
   31. Checking binding constraints doesn’t give indication of progress
       (`2462 <https://github.com/osate/osate2/issues/2462>`__)

-  Error Model and Analysis Plugins

   1. EMV2 ErrorType qualified name is incomplete
      (`1634 <https://github.com/osate/osate2/issues/1634>`__)
   2. Error propagation in feature group type result in errors.
      (`2408 <https://github.com/osate/osate2/issues/2408>`__)
   3. Error Type cyclical extensions cause the text editor to lock up
      (`2455 <https://github.com/osate/osate2/issues/2455>`__)
   4. Exception during EMV2 Serialization
      (`2483 <https://github.com/osate/osate2/issues/2483>`__)
   5. Exception when serializing error model library which extends error
      model library
      (`2512 <https://github.com/osate/osate2/issues/2512>`__)
   6. Error propagation name sometimes disappears when editing in the GE
      (`2518 <https://github.com/osate/osate2/issues/2518>`__)

-  Graphical Editor

   1. Add partial EMV2 support to graphical editor
      (`2450 <https://github.com/osate/osate2/issues/2450>`__)
   2. Graphical editor uses inefficient property tester
      (`2499 <https://github.com/osate/osate2/issues/2499>`__)
   3. Graphical editor unnecessarily parses AADL file to enable handlers
      (`2500 <https://github.com/osate/osate2/issues/2500>`__)
   4. Diagram elements without labels are being displayed in outline
      (`2542 <https://github.com/osate/osate2/issues/2542>`__)
   5. Secondary labels of connections are treated as immovable.
      (`2544 <https://github.com/osate/osate2/issues/2544>`__)

-  ALISA

   1. Remove binpacker from ALISA
      (`2463 <https://github.com/osate/osate2/issues/2463>`__)

-  Behavior Annex

   1. Null data access reference in SharedDataAction objects
      (`2372 <https://github.com/osate/osate2/issues/2372>`__)
   2. Support unparsing when behavior annex has resolution errors
      (`2459 <https://github.com/osate/osate2/issues/2459>`__)
   3. In BA plugin, port dequeue actions are not resolved properly
      (`2523 <https://github.com/osate/osate2/issues/2523>`__)
   4. In BA plugin, editor crashes when using a dequeue action on
      something that is not an event [data] port
      (`2525 <https://github.com/osate/osate2/issues/2525>`__)

.. _known-issues-1:

Known issues
^^^^^^^^^^^^

-  MacOS users must run the command
   ``sudo xattr -rd com.apple.quarantine osate2.app/`` to be able to run
   OSATE.
-  Installing the OSATE plugins into “Eclipse for RCP and RAP
   Developers” may prevent Eclipse from starting. See `issue
   2061 <https://github.com/osate/osate2/issues/2061>`__.
-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.9.1 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.
-  There is a minor bug (#2569) in OSATE 2.9.1 that prevents setting the
   AADL perspective as the default perspective in a new workspace. The
   bug also prevents the application icon from being shown and puts an
   entry “Product osate2 could not be found” into the error log at each
   start.This can be fixed manually by adding the following line to the
   osate.ini file.

::

   -Declipse.product=org.osate.branding.osate2

Version 2.9.0
~~~~~~~~~~~~~

.. _release-2:

Release
^^^^^^^

-  **GIT tag**: 2.9.0-RELEASE
-  **Release date**: October 30, 2020
-  **Eclipse base version**: 2020-06
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.9.0/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.9.0/products

.. _sha256-hashes-for-the-downloads-2:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   3e67b1b8b2230ace279d4cf6224e4bbd59a95b691eafb88fd8845388b58f0424  osate2-2.9.0-vfinal-linux.gtk.x86_64.tar.gz
   e2ada5b747ab042367fd88b198c12c58d00389f0f4720a7691eda95c58a508f8  osate2-2.9.0-vfinal-macosx.cocoa.x86_64.tar.gz
   f53542361a04da3d5e2bf597490585a8086abaacdaab4286b7c8eecbc936d9fb  osate2-2.9.0-vfinal-win32.win32.x86_64.zip

.. _notable-changes-2:

Notable changes
^^^^^^^^^^^^^^^

-  New example wizard and new/updated AADL examples
-  New model statistics command
-  Improved performance for very large AADL files by updating outline
   view in a background thread
-  New advanced feature to override contributed property sets for a
   workspace via an OSATE preference setting (Warning: changing
   contributed property sets this way can break analysis plugins)
-  Underlying Eclipse version updated to 2020-06

.. _fixed-issues-2:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Clean up examples repository on github and add examples to OSATE
       (`1016 <https://github.com/osate/osate2/issues/1016>`__)
   2.  Users need a way to override contributed property sets
       (`1134 <https://github.com/osate/osate2/issues/1134>`__)
   3.  Annex implementations cannot use new Xtext (>= 2.9) workflows
       (`1818 <https://github.com/osate/osate2/issues/1818>`__)
   4.  Feature direction is not checked when a feature group is refined
       to a specific feature group sub-feature in a flow implementation
       (`1991 <https://github.com/osate/osate2/issues/1991>`__)
   5.  Generate Java code for property types and constants
       (`2113 <https://github.com/osate/osate2/issues/2113>`__)
   6.  Move outline tree computation to background thread
       (`2320 <https://github.com/osate/osate2/issues/2320>`__)
   7.  AADL formatter exception when formatting annex without an EMF
       write transaction
       (`2349 <https://github.com/osate/osate2/issues/2349>`__)
   8.  Format annexes without parsing them again
       (`2402 <https://github.com/osate/osate2/issues/2402>`__)
   9.  Upgrade to new Xtext code generation workflows
       (`2405 <https://github.com/osate/osate2/issues/2405>`__)
   10. Validation does not catch flow source/sink in the middle of a
       flow path
       (`2415 <https://github.com/osate/osate2/issues/2415>`__)
   11. PropertyIsModalException in validator
       (`2417 <https://github.com/osate/osate2/issues/2417>`__)
   12. NPE in classifier information view
       (`2429 <https://github.com/osate/osate2/issues/2429>`__)
   13. The model statistics command disappeared
       (`1375 <https://github.com/osate/osate2/issues/1375>`__)
   14. Codegen checker does not log exceptions
       (`2327 <https://github.com/osate/osate2/issues/2327>`__)
   15. Latency analysis does not produce any result for certain end to
       end flows
       (`2423 <https://github.com/osate/osate2/issues/2423>`__)
   16. Bad plugin information
       (`2331 <https://github.com/osate/osate2/issues/2331>`__)
   17. Upgrade to Eclipse 2020-06
       (`2377 <https://github.com/osate/osate2/issues/2377>`__)
   18. Upgrade to ELK 0.7.0
       (`2464 <https://github.com/osate/osate2/issues/2464>`__)

-  Error Model and Analysis Plugins

   1. Expand displayed probability in FTA table
      (`2359 <https://github.com/osate/osate2/issues/2359>`__)
   2. Qualified names removed from EMV2 type aliases
      (`2398 <https://github.com/osate/osate2/issues/2398>`__)

-  Graphical Editor

   1.  Additional flow editing capabilities
       (`1212 <https://github.com/osate/osate2/issues/1212>`__)
   2.  Experimental visualization and editing capability for EMV2 flow
       propagations
       (`1546 <https://github.com/osate/osate2/issues/1546>`__)
   3.  Remove support for Graphiti file format
       (`2324 <https://github.com/osate/osate2/issues/2324>`__)
   4.  Refactor, cleanup, and rework API for graphical editor
       (`2336 <https://github.com/osate/osate2/issues/2336>`__)
   5.  Stack overflow error when highlighting flows with cycles
       (`2350 <https://github.com/osate/osate2/issues/2350>`__)
   6.  Fix graphical flow editing issues
       (`2392 <https://github.com/osate/osate2/issues/2392>`__)
   7.  Fix renaming of refined elements
       (`2394 <https://github.com/osate/osate2/issues/2394>`__)
   8.  Cleanup flow tools
       (`2396 <https://github.com/osate/osate2/issues/2396>`__)
   9.  Copying and pasting of elements that have a source and/or
       destination cause exceptions
       (`2411 <https://github.com/osate/osate2/issues/2411>`__)
   10. Created business objects not are not added to the diagram
       (`2424 <https://github.com/osate/osate2/issues/2424>`__)

-  ALISA

   1. Assurance View does not correctly render subclaims
      (`2381 <https://github.com/osate/osate2/issues/2381>`__)

-  Behavior Annex

   1. AADL file does not open in Editor when there is a Syntax error on
      subcomponent type and BA clause in Component
      (`2401 <https://github.com/osate/osate2/issues/2401>`__)

.. _known-issues-2:

Known issues
^^^^^^^^^^^^

-  MacOS users must run the command
   ``sudo xattr -rd com.apple.quarantine osate2.app/`` to be able to run
   OSATE.
-  Installing the OSATE plugins into “Eclipse for RCP and RAP
   Developers” prevents Eclipse from starting. See `issue
   2061 <https://github.com/osate/osate2/issues/2061>`__.
-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.9.0 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.

Version 2.8.0
~~~~~~~~~~~~~

.. _release-3:

Release
^^^^^^^

-  **GIT tag**: 2.8.0-RELEASE
-  **Release date**: July 9, 2020
-  **Eclipse base version**: 2020-03
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.8.0/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.8.0/products

.. _sha256-hashes-for-the-downloads-3:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   cc8f43a0bab18eec55afd9641c7aab424f3c8890b00f77b8cbfa1a8ca0c4fac7  osate2-2.8.0-vfinal-linux.gtk.x86_64.tar.gz
   6cd0eda26468bbf6aefc2fa374d81764e0e873c8d584ebb1bb51eac66c6510db  osate2-2.8.0-vfinal-macosx.cocoa.x86_64.tar.gz
   ee014c259fdda208bd08fb80c86eff147d4dc7f69c6a3bae0f05a9367e00c05e  osate2-2.8.0-vfinal-win32.win32.x86_64.zip

.. _notable-changes-3:

Notable changes
^^^^^^^^^^^^^^^

-  Underlying Eclipse version updated to 2020-03

.. _fixed-issues-3:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Missing consistency checks for connection instances
       (`582 <https://github.com/osate/osate2/issues/582>`__)
   2.  Performance issue when editing AADL text
       (`1832 <https://github.com/osate/osate2/issues/1832>`__)
   3.  Missing validation for reference value with array indices
       (`2159 <https://github.com/osate/osate2/issues/2159>`__)
   4.  Connection properties are not inherited from containing component
       (`2264 <https://github.com/osate/osate2/issues/2264>`__)
   5.  Instantiate action should work on .aadl files in the AADL
       Navigator
       (`2272 <https://github.com/osate/osate2/issues/2272>`__)
   6.  Instantiation results dialog is annoying when instantiation is
       successful
       (`2274 <https://github.com/osate/osate2/issues/2274>`__)
   7.  Add dependency views to perspective
       (`2275 <https://github.com/osate/osate2/issues/2275>`__)
   8.  Stack overflow in validator for cyclic constants
       (`2282 <https://github.com/osate/osate2/issues/2282>`__)
   9.  Null pointer exception in end to end flow instantiation
       (`2287 <https://github.com/osate/osate2/issues/2287>`__)
   10. Update docs for instantiation
       (`2294 <https://github.com/osate/osate2/issues/2294>`__)
   11. ‘in modes’ clause on behavior specification stopped working in
       OSATE 2.7.1.
       (`2295 <https://github.com/osate/osate2/issues/2295>`__)
   12. Annex instantiation invoked before properties and connection
       patterns (`2299 <https://github.com/osate/osate2/issues/2299>`__)
   13. Problem serialization of event data PortSpecification instances
       (`2300 <https://github.com/osate/osate2/issues/2300>`__)
   14. Upgrade to Eclipse 2020-03
       (`2309 <https://github.com/osate/osate2/issues/2309>`__)
   15. Refinement of abstract features allows removal of classifier
       (`2319 <https://github.com/osate/osate2/issues/2319>`__)
   16. Aadl2JavaValidator doesn’t check CLASSIFIER_MATCH correctly
       (`2344 <https://github.com/osate/osate2/issues/2344>`__)
   17. Fan-in for data ports should be forbidden
       (`2356 <https://github.com/osate/osate2/issues/2356>`__)
   18. Fix BLESS plugin installation as additional OSATE component
       (`2357 <https://github.com/osate/osate2/issues/2357>`__)
   19. Flow latency analysis window is not sized based on content
       (`2039 <https://github.com/osate/osate2/issues/2039>`__)
   20. ClassCastException when running codegen checker
       (`2054 <https://github.com/osate/osate2/issues/2054>`__)
   21. Memory budget ignores Memory_Size on system and virtual
       processors and related issues
       (`2169 <https://github.com/osate/osate2/issues/2169>`__)
   22. BusLoad analysis results should include the data overhead for
       each bus in the report
       (`2278 <https://github.com/osate/osate2/issues/2278>`__)
   23. Flow latency report should include flow names in leaf components
       (`2289 <https://github.com/osate/osate2/issues/2289>`__)

-  Error Model and Analysis Plugins

   1. no changes

-  Graphical Editor

   1. DirtyState Issue / NPE When Refactoring
      (`1180 <https://github.com/osate/osate2/issues/1180>`__)
   2. Improved validation in graphical flow creation tools
      (`1204 <https://github.com/osate/osate2/issues/1204>`__)
   3. Add graphical editing support for prototypes
      (`1540 <https://github.com/osate/osate2/issues/1540>`__)
   4. Adjust graphical editor tests to close all unnecessary views
      (`2293 <https://github.com/osate/osate2/issues/2293>`__)
   5. Refined flow segments are not highlighted
      (`2304 <https://github.com/osate/osate2/issues/2304>`__)
   6. Graphical editor AADL properties section of refined elements
      doesn’t work
      (`2306 <https://github.com/osate/osate2/issues/2306>`__)
   7. Improve layout capabilities for flow source and sink
      specifications.
      (`2317 <https://github.com/osate/osate2/issues/2317>`__)
   8. Improve performance with the flow contribution item
      (`2328 <https://github.com/osate/osate2/issues/2328>`__)
   9. Tags are incorrectly displayed in the graphical editor outline.
      (`2333 <https://github.com/osate/osate2/issues/2333>`__)

-  Behavior Annex

   1. Value constant not accepted for behavior annex
      (`2184 <https://github.com/osate/osate2/issues/2184>`__)
   2. Memory leak when using the Behavior Annex
      (`2352 <https://github.com/osate/osate2/issues/2352>`__)
   3. Null data access reference in SharedDataAction objects
      (`2372 <https://github.com/osate/osate2/issues/2372>`__)

.. _known-issues-3:

Known issues
^^^^^^^^^^^^

-  MacOS users must run the command
   ``sudo xattr -rd com.apple.quarantine osate2.app/`` to be able to run
   OSATE.
-  Installing the OSATE plugins into “Eclipse for RCP and RAP
   Developers” prevents Eclipse from starting. See `issue
   2061 <https://github.com/osate/osate2/issues/2061>`__.
-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.8.0 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.

Version 2.7.1
~~~~~~~~~~~~~

.. _release-4:

Release
^^^^^^^

-  **GIT tag**: 2.7.1-RELEASE
-  **Release date**: April 21, 2020
-  **Eclipse base version**: 2019-12
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.7.1/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.7.1/products

.. _sha256-hashes-for-the-downloads-4:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   6f898deb856e17096c37751603455d14557ebd0065506318bcfaaaf17cf4f16f  osate2-2.7.1-vfinal-linux.gtk.x86_64.tar.gz
   9b9b3d57e03834a0b288cbdfe9a139da81b05222c684d4d81531d3804600781c  osate2-2.7.1-vfinal-macosx.cocoa.x86_64.tar.gz
   bc0181249bef3e4c83864b41fa009cda8c485ac0c21d8f4f98919e73e0fe1864  osate2-2.7.1-vfinal-win32.win32.x86_64.zip

.. _notable-changes-4:

Notable changes
^^^^^^^^^^^^^^^

-  The bus load analysis now handles bandwidth budgets and capacities
   for virtual buses.
-  The flow latency analysis now considers queuing latency for
   non-periodic buses.
-  The flow latency analysis can now processes user-supplied thread
   response times instead of the execution time.
-  Various bug fixes in the priority inversion checker.
-  Instantiation and re-instantiation are more flexible to use, and
   exceptions are reported to the user.
-  We have implemented proper type checking for property constants.

.. _fixed-issues-4:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Remove QuickSort
       (`1365 <https://github.com/osate/osate2/issues/1365>`__)
   2.  Redesign reinstantiation handlers
       (`1553 <https://github.com/osate/osate2/issues/1553>`__)
   3.  Abstract features allow all component classifiers
       (`1926 <https://github.com/osate/osate2/issues/1926>`__)
   4.  Content assist should propose property constants
       (`2073 <https://github.com/osate/osate2/issues/2073>`__)
   5.  Display AADLDoc for all elements
       (`2075 <https://github.com/osate/osate2/issues/2075>`__)
   6.  Add dialog proposing to save files prior to instantiation
       (`2083 <https://github.com/osate/osate2/issues/2083>`__)
   7.  Check for null containing classifier in
       Aadl2LinkingService::getLinkedObjects
       (`2139 <https://github.com/osate/osate2/issues/2139>`__)
   8.  Missing help text for property group filter in AADL Properties
       view (`2187 <https://github.com/osate/osate2/issues/2187>`__)
   9.  Various exceptions in AADL Property Values view
       (`2191 <https://github.com/osate/osate2/issues/2191>`__)
   10. Closing a project can lead to unresolved references to
       predeclared properties
       (`2195 <https://github.com/osate/osate2/issues/2195>`__)
   11. OSATE allows aadl2 file extension for AADL files
       (`2197 <https://github.com/osate/osate2/issues/2197>`__)
   12. Enable annex instantiation
       (`2208 <https://github.com/osate/osate2/issues/2208>`__)
   13. Plug-in contributions and referenced projects are no longer shown
       first in AADL navigator
       (`2217 <https://github.com/osate/osate2/issues/2217>`__)
   14. NPE when closing OSATE
       (`2221 <https://github.com/osate/osate2/issues/2221>`__)
   15. Incomplete type checking for property constants
       (`2222 <https://github.com/osate/osate2/issues/2222>`__)
   16. Renaming property set drops property set prefix from references
       to constants
       (`2223 <https://github.com/osate/osate2/issues/2223>`__)
   17. Newly created instance model references elements in other
       resource set(s)
       (`2241 <https://github.com/osate/osate2/issues/2241>`__)
   18. Having the same property association as a contained property
       association and direct association causes instantiation exception
       (`2259 <https://github.com/osate/osate2/issues/2259>`__)
   19. Rename refactoring misses a reference
       (`2262 <https://github.com/osate/osate2/issues/2262>`__)
   20. Instantiation does not log exceptions
       (`2263 <https://github.com/osate/osate2/issues/2263>`__)
   21. Actual_Connection_Binding is not overridden by contained property
       association
       (`2265 <https://github.com/osate/osate2/issues/2265>`__)
   22. Missing queuing latency handling for buses
       (`1148 <https://github.com/osate/osate2/issues/1148>`__)
   23. Flow latency analysis uses compute execution time instead of
       response time
       (`2122 <https://github.com/osate/osate2/issues/2122>`__)
   24. Bus load analysis should take virtual buses into account
       (`2205 <https://github.com/osate/osate2/issues/2205>`__)
   25. Priority inversion check misinterprets priority property and
       other bugs
       (`2243 <https://github.com/osate/osate2/issues/2243>`__)
   26. Missing p2 site for yakindu plugin
       (`2193 <https://github.com/osate/osate2/issues/2193>`__)
   27. Add comparison with baseline to build
       (`2194 <https://github.com/osate/osate2/issues/2194>`__)
   28. API Analysis builder reports bogus API changes
       (`2204 <https://github.com/osate/osate2/issues/2204>`__)
   29. Automate update of dependency versions for coverage report
       (`2213 <https://github.com/osate/osate2/issues/2213>`__)

-  Error Model and Analysis Plugins

   1. EMV2: error_detection_effect not allow port in feature group
      (`2128 <https://github.com/osate/osate2/issues/2128>`__)
   2. Wrong validation of error conditions
      (`2209 <https://github.com/osate/osate2/issues/2209>`__)

-  Graphical Editor

   1. Support Creating a Flow Implementation without Flow Specification
      being Visible
      (`1202 <https://github.com/osate/osate2/issues/1202>`__)
   2. Add action to add all elements that are connected to a selected
      element (`1543 <https://github.com/osate/osate2/issues/1543>`__)
   3. Add action to show all elements that participate in a flow or mode
      to a diagram
      (`1544 <https://github.com/osate/osate2/issues/1544>`__)
   4. End to End flow creation in Graphical Editor requires extra clicks
      (`1774 <https://github.com/osate/osate2/issues/1774>`__)
   5. Review graphical editor actions
      (`2219 <https://github.com/osate/osate2/issues/2219>`__)
   6. GE Showing Flow With Errors
      (`2270 <https://github.com/osate/osate2/issues/2270>`__)

-  Behavior Annex

   1. Property associations for behavior variables are not supported
      (`2190 <https://github.com/osate/osate2/issues/2190>`__)
   2. Behavior Annex: Null pointer exception when calling
      getContainingFeature() on an instance of StructUnionElement
      (`2199 <https://github.com/osate/osate2/issues/2199>`__)
   3. Behavior annex plugin throws an error if subprogram call action
      refers to something else than a subprogram classifier
      (`2200 <https://github.com/osate/osate2/issues/2200>`__)
   4. In BA plugin, error with type checking of get/release resource
      behavior actions
      (`2234 <https://github.com/osate/osate2/issues/2234>`__)
   5. In BA plugin, unparser fails on objects of type
      BehaviorIntegerLiteral and BehaviorRealLiteral
      (`2236 <https://github.com/osate/osate2/issues/2236>`__)

.. _known-issues-4:

Known issues
^^^^^^^^^^^^

-  MacOS users must run the command
   ``sudo xattr -rd com.apple.quarantine osate2.app/`` to be able to run
   OSATE.

-  Installing the OSATE plugins into “Eclipse for RCP and RAP
   Developers” prevents Eclipse from starting. See `issue
   2061 <https://github.com/osate/osate2/issues/2061>`__.

-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.7.0 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.
   If newer versions are provided by
   `loonwerks <http://loonwerks.com>`__ in an update site, we may make
   them available via the “Install Additional OSATE Components” dialog.

   **After installing Resolute you must perform a clean build of your
   workspace, otherwise Resolute verification methods will fail with a
   class cast exception.**

Version 2.7.0
~~~~~~~~~~~~~

.. _release-5:

Release
^^^^^^^

-  **GIT tag**: 2.7.0-RELEASE
-  **Release date**: February 7, 2020
-  **Eclipse base version**: 2019-12
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.7.0/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.7.0/products

.. _sha256-hashes-for-the-downloads-5:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   1aa7cfa397d5ece55d4e785fce1461e5e8a56d7b293e0d0623abb304125f0754  osate2-2.7.0-vfinal-linux.gtk.x86_64.tar.gz
   2bcb707d7a777c4d2f0b8f915e1314646848c294c498ac4039ac8d7c5553c352  osate2-2.7.0-vfinal-macosx.cocoa.x86_64.tar.gz
   cae2e11f58406181450a5fca0b5b69518172197df1c3075f55fcd55bd0fbc039  osate2-2.7.0-vfinal-win32.win32.x86_64.zip

.. _notable-changes-5:

Notable changes
^^^^^^^^^^^^^^^

-  We have changed instantiation of data and subprogram access
   connections, they no longer end at thread boundaries. As a result
   more flows can be instantiated. See issues #1941, #2009, #2032,
   #2059, and #2161 for details.
-  This version of OSATE is based on Eclipse 2019-12, so the context
   menu in the outline view does no longer disappear.
-  The first start after installation is significantly faster (seconds
   instead of minutes).
-  The Ocarina Connector plugin is now a separate component that can be
   installed via ``Help`` -> ``Install Additional OSATE Components``.
-  OSATE plugins and feature now use semantic versions. Developers of
   additional components can (and should!) make use of them to assure
   that their components are installed in a compatible OSATE version.

.. _fixed-issues-5:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Add property group filter to AADL property view
       (`521 <https://github.com/osate/osate2/issues/521>`__)
   2.  End to end flow instance is not created if subprogram access
       connections are involved
       (`1941 <https://github.com/osate/osate2/issues/1941>`__)
   3.  Instantiator ignores in modes for end to end flows
       (`2005 <https://github.com/osate/osate2/issues/2005>`__)
   4.  End to end flow instantiation creates nonsense flow
       (`2009 <https://github.com/osate/osate2/issues/2009>`__)
   5.  Shared subprogram access yields too many connection instances in
       instance model
       (`2032 <https://github.com/osate/osate2/issues/2032>`__)
   6.  Instantiation of feature group connections can create unnecessary
       connection instances
       (`2059 <https://github.com/osate/osate2/issues/2059>`__)
   7.  Name resolution failures for package names with white space
       (`2089 <https://github.com/osate/osate2/issues/2089>`__)
   8.  Remove obsolete AADL 1 reference manual
       (`2140 <https://github.com/osate/osate2/issues/2140>`__)
   9.  NPE when deleting package name
       (`2141 <https://github.com/osate/osate2/issues/2141>`__)
   10. Renaming a package or property set doesn’t update name at the end
       (`2143 <https://github.com/osate/osate2/issues/2143>`__)
   11. Typo in error message for duplicates package
       (`2145 <https://github.com/osate/osate2/issues/2145>`__)
   12. Code generated from the AADL metamodel has compile errors
       (`2156 <https://github.com/osate/osate2/issues/2156>`__)
   13. Some data-access connections are not being instantiated.
       (`2161 <https://github.com/osate/osate2/issues/2161>`__)
   14. Latency analysis does not interpret execution time on feature
       (entrypoint) of thread
       (`1940 <https://github.com/osate/osate2/issues/1940>`__)
   15. Power analysis produces empty info messages
       (`2028 <https://github.com/osate/osate2/issues/2028>`__)
   16. OSATE plugin versions should change when its dependencies change
       (`776 <https://github.com/osate/osate2/issues/776>`__)
   17. Update license for OSATE
       (`1740 <https://github.com/osate/osate2/issues/1740>`__)
   18. Upgrade to Eclipse 2019-12
       (`2064 <https://github.com/osate/osate2/issues/2064>`__)
   19. Ocarina plugin should be an additional component
       (`2067 <https://github.com/osate/osate2/issues/2067>`__)
   20. Exception when typing an ‘a’ in the new project wizard filter
       field (`2076 <https://github.com/osate/osate2/issues/2076>`__)
   21. Remove BIRT report designer from OSATE
       (`2078 <https://github.com/osate/osate2/issues/2078>`__)
   22. Code coverage on sonarcloud is incorrect
       (`2106 <https://github.com/osate/osate2/issues/2106>`__)
   23. Replace copied code with external plugin
       (`2119 <https://github.com/osate/osate2/issues/2119>`__)
   24. Remove unnecessary dependency on Papyrus UML editor
       (`2120 <https://github.com/osate/osate2/issues/2120>`__)
   25. Code generated from the AADL metamodel has compile errors
       (`2156 <https://github.com/osate/osate2/issues/2156>`__)
   26. Add a way to build with mirrored p2 repositories
       (`2162 <https://github.com/osate/osate2/issues/2162>`__)

-  Error Model and Analysis Plugins

   1. Reach-Down subcomponent hierarchy does not set property
      EMV2::OccurrenceDistribution
      (`2112 <https://github.com/osate/osate2/issues/2112>`__)
   2. Fault trace generation does not show all steps in trace
      (`2123 <https://github.com/osate/osate2/issues/2123>`__)
   3. In Fault trace/FTA the incorrect component instance is associated
      with the trace step representing the subcomponent state condition
      (`2124 <https://github.com/osate/osate2/issues/2124>`__)
   4. Error states with error types should not be triggered by error
      events without types or non-matching types
      (`2125 <https://github.com/osate/osate2/issues/2125>`__)
   5. ClassCastException in FTA
      (`2177 <https://github.com/osate/osate2/issues/2177>`__)

-  Graphical Editor

   1. Wrong button size in ‘Create End to End Flow Specification’ wizard
      (`1856 <https://github.com/osate/osate2/issues/1856>`__)
   2. Implement virtual bus access support in the graphical editor
      (`2010 <https://github.com/osate/osate2/issues/2010>`__)
   3. Graphical editor SWTBot tests failing
      (`2018 <https://github.com/osate/osate2/issues/2018>`__)
   4. Modify subcomponent array dimensions throws exception
      (`2030 <https://github.com/osate/osate2/issues/2030>`__)
   5. Select all action doesn’t select all diagram elements.
      (`2108 <https://github.com/osate/osate2/issues/2108>`__)
   6. Check that graphical viewer is valid before setting context help
      (`2149 <https://github.com/osate/osate2/issues/2149>`__)
   7. Update GE license to EPL 2.0
      (`2171 <https://github.com/osate/osate2/issues/2171>`__)

-  ALISA - no changes
-  Behavior Annex

   1. Unable to reference port in feature group from Behavior Annex
      specification.
      (`2146 <https://github.com/osate/osate2/issues/2146>`__)
   2. Unable to use on port as transition condition in the Behavior
      Annex (`2147 <https://github.com/osate/osate2/issues/2147>`__)
   3. Update BA license to EPL 2.0
      (`2170 <https://github.com/osate/osate2/issues/2170>`__)
   4. In BA plugin, name resolution in actions fails when classifier
      with the same name exists
      (`2175 <https://github.com/osate/osate2/issues/2175>`__)

.. _known-issues-5:

Known issues
^^^^^^^^^^^^

-  MacOS users must run the command
   ``sudo xattr -rd com.apple.quarantine osate2.app/`` to be able to run
   OSATE.

-  Installing the OSATE plugins into “Eclipse for RCP and RAP
   Developers” prevents Eclipse from starting. See `issue
   2061 <https://github.com/osate/osate2/issues/2061>`__.

-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.7.0 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.
   Once newer versions are provided by
   `loonwerks <http://loonwerks.com>`__ in an update site, we will make
   them available via the “Install Additional OSATE Components” dialog.

   **After installing Resolute you must perform a clean build of your
   workspace, otherwise Resolute verification methods will fail with a
   class cast exception.**

Version 2.6.1
~~~~~~~~~~~~~

.. _release-6:

Release
^^^^^^^

-  **GIT tag**: 2.6.1-RELEASE
-  **Release date**: December 20, 2019
-  **Eclipse base version**: 2019-09
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.6.1/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.6.1/products

.. _sha256-hashes-for-the-downloads-6:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   c2f39cde12da4dea492be16d6167834092e0c37eadb29b45143c120ad0fe0708  osate2-2.6.1-vfinal-linux.gtk.x86_64.tar.gz
   7d2630efda4f9884f098a5f26fcd0fee944cf52919a5d486a501dd3db3bc0439  osate2-2.6.1-vfinal-macosx.cocoa.x86_64.tar.gz
   f2c4198cae85d1400b95aa883f821150a1238566df0e21fa51251ac2e1ea08a0  osate2-2.6.1-vfinal-win32.win32.x86_64.zip

.. _notable-changes-6:

Notable changes
^^^^^^^^^^^^^^^

-  This is a bug fix release.

.. _fixed-issues-6:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Renaming elements in text editor does not work
       (`359 <https://github.com/osate/osate2/issues/359>`__)
   2.  Difficult to determine direction of access feature instances
       (`758 <https://github.com/osate/osate2/issues/758>`__)
   3.  PackageSection not defined when printing the stack after an
       exception (`905 <https://github.com/osate/osate2/issues/905>`__)
   4.  Some OSATE help pages are titled “THROW THIS PAGE AWAY”
       (`1496 <https://github.com/osate/osate2/issues/1496>`__)
   5.  Misleading warning on feature reference in parameter connection
       (`1988 <https://github.com/osate/osate2/issues/1988>`__)
   6.  Infinite loop when building workspace
       (`2007 <https://github.com/osate/osate2/issues/2007>`__)
   7.  Remove deprecated code
       (`2044 <https://github.com/osate/osate2/issues/2044>`__)
   8.  When renaming a port references in a connection declaration are
       not renamed
       (`2046 <https://github.com/osate/osate2/issues/2046>`__)
   9.  AadlFileTypePropertyTester is very inefficient
       (`2048 <https://github.com/osate/osate2/issues/2048>`__)
   10. Add “Instantiate” command to navigator context menu
       (`2052 <https://github.com/osate/osate2/issues/2052>`__)
   11. Outline view shows “Type Extension” instead of name of extended
       type (`2053 <https://github.com/osate/osate2/issues/2053>`__)
   12. Connection_Pattern ignored when instantiating data access
       connection
       (`2057 <https://github.com/osate/osate2/issues/2057>`__)
   13. Formatting issues with property sets
       (`2058 <https://github.com/osate/osate2/issues/2058>`__)
   14. Rename refactoring fails for record fields
       (`2077 <https://github.com/osate/osate2/issues/2077>`__)
   15. Various improvements to “mark occurrences”
       (`2086 <https://github.com/osate/osate2/issues/2086>`__)
   16. Rename refactoring does not work in ‘applies to’ and reference
       value (`2088 <https://github.com/osate/osate2/issues/2088>`__)
   17. Code for budget analyses should be cleaned up
       (`1964 <https://github.com/osate/osate2/issues/1964>`__)
   18. AnalysisResult description for flow latency analysis is outdated
       (`2027 <https://github.com/osate/osate2/issues/2027>`__)
   19. Use Sonarcloud for code analysis
       (`2055 <https://github.com/osate/osate2/issues/2055>`__)
   20. ELK repository URL is incomplete
       (`2062 <https://github.com/osate/osate2/issues/2062>`__)
   21. Unexpected Xtext version change when installing updates from
       2.6.0 update site
       (`2097 <https://github.com/osate/osate2/issues/2097>`__)
   22. Add test support plugin to p2 repository
       (`2105 <https://github.com/osate/osate2/issues/2105>`__)

-  Error Model and Analysis Plugins

   1. NullPointerException in Check Unhandled Faults
      (`2092 <https://github.com/osate/osate2/issues/2092>`__)
   2. FHA: IndexOutOfBoundsException if likelihood unspecified
      (`2093 <https://github.com/osate/osate2/issues/2093>`__)

-  ALISA

   1. Add JUnit test that uses Resolute
      (`2038 <https://github.com/osate/osate2/issues/2038>`__)
   2. ArrayIndexOutOfBounds exception in CommonScopeProvider
      (`2042 <https://github.com/osate/osate2/issues/2042>`__)
   3. Validations on reqspec and verify files should be executed while
      typing (`2049 <https://github.com/osate/osate2/issues/2049>`__)

-  Behavior Annex

   1. OSATE editor crashes with index out of bounds exception with model
      using behavior annex
      (`2065 <https://github.com/osate/osate2/issues/2065>`__)

.. _known-issues-6:

Known issues
^^^^^^^^^^^^

-  Under certain conditions the outline view displays no context menu
   menu on right click. As a workaround close and re-open the editor.
   See `issue 2050 <https://github.com/osate/osate2/issues/2050>`__.

-  MacOS users must run the command
   ``sudo xattr -rd com.apple.quarantine osate2.app/`` to be able to run
   OSATE.

-  Installing the OSATE plugins into “Eclipse for RCP and RAP
   Developers” prevents Eclipse from starting. See `issue
   2061 <https://github.com/osate/osate2/issues/2061>`__.

-  The first startup of OSATE can take a rather long (up to a couple of
   minutes).

-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.6.1 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.
   Once newer versions are provided by
   `loonwerks <http://loonwerks.com>`__ in an update site, we will make
   them available via the “Install Additional OSATE Components” dialog.

   **After installing Resolute you must perform a clean build of your
   workspace, otherwise Resolute verification methods will fail with a
   class cast exception.**

Version 2.6.0
~~~~~~~~~~~~~

.. _release-7:

Release
^^^^^^^

-  **GIT tag**: 2.6.0-RELEASE
-  **Release date**: November 6, 2019
-  **Eclipse base version**: 2019-09
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.6.0/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.6.0/products

.. _sha256-hashes-for-the-downloads-7:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   20eef0b6c801ba3090a856aea05ec7807da1621e8768da953566875c50e42031  osate2-2.6.0-vfinal-linux.gtk.x86_64.tar.gz
   2b57e60a8c19893d27b686093c90df60467b80668bf270e7ef772685ccac3c89  osate2-2.6.0-vfinal-macosx.cocoa.x86_64.tar.gz
   cac1146f9c7bf967174264bddb831433f35568d12308b40d8ca7c0979654327e  osate2-2.6.0-vfinal-win32.win32.x86_64.zip

.. _notable-changes-7:

Notable changes
^^^^^^^^^^^^^^^

-  We have upgraded the underlying Eclipse version to 2019-09.
-  The plugins are now signed. There should no longer be a warning about
   installing unsigned plugins when installing into an existing Eclipse
   installation.

.. _fixed-issues-7:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Flow through data component cannot be instantiated
       (`643 <https://github.com/osate/osate2/issues/643>`__)
   2.  Instantiator merges access connections
       (`676 <https://github.com/osate/osate2/issues/676>`__)
   3.  Allow subprogram access parameter as flow start and end point
       (`730 <https://github.com/osate/osate2/issues/730>`__)
   4.  Error on data access in the middle of end to end flow
       (`1124 <https://github.com/osate/osate2/issues/1124>`__)
   5.  End to end flow not instantiated in component with refined
       features in the flow
       (`1830 <https://github.com/osate/osate2/issues/1830>`__)
   6.  End to end flow instantiation broken for flows through threads
       (`1953 <https://github.com/osate/osate2/issues/1953>`__)
   7.  Subprogram parameters are allowed as feature connection ends
       (`1954 <https://github.com/osate/osate2/issues/1954>`__)
   8.  Serializer fails on programmatically added property constant.
       (`1972 <https://github.com/osate/osate2/issues/1972>`__)
   9.  Wrong validation of end to end flow across data access
       (`1974 <https://github.com/osate/osate2/issues/1974>`__)
   10. Bidirectional access connections are not instantiated correctly
       (`1977 <https://github.com/osate/osate2/issues/1977>`__)
   11. Using feature-group specific flow paths has instance model errors
       for the “path not taken”.
       (`1984 <https://github.com/osate/osate2/issues/1984>`__)
   12. Error message on connection when starting a flow source
       implementation with a data subcomponent
       (`1987 <https://github.com/osate/osate2/issues/1987>`__)
   13. Add isSubClassifier method to AadlUtil
       (`1989 <https://github.com/osate/osate2/issues/1989>`__)
   14. Out of memory exception on OSATE 2.6.0 (testing)
       (`1997 <https://github.com/osate/osate2/issues/1997>`__)
   15. Instantiation of feature connection instances fails with nested
       components
       (`1998 <https://github.com/osate/osate2/issues/1998>`__)
   16. CoreException when selecting a file in the navigator
       (`2014 <https://github.com/osate/osate2/issues/2014>`__)
   17. Formatter indents comments too much
       (`2025 <https://github.com/osate/osate2/issues/2025>`__)
   18. Annex formatter sometimes throws IllegalStateException
       (`2036 <https://github.com/osate/osate2/issues/2036>`__)
   19. IndexOutOfBoundsException when generating Excel spreadsheet for
       latency analysis
       (`1985 <https://github.com/osate/osate2/issues/1985>`__)
   20. Flow latency analysis crashes when run from instance model editor
       (`2013 <https://github.com/osate/osate2/issues/2013>`__)
   21. Installing OSATE from the update site gives a warning about
       unsigned content
       (`530 <https://github.com/osate/osate2/issues/530>`__)
   22. Upgrade to Eclipse 2019-09
       (`1888 <https://github.com/osate/osate2/issues/1888>`__)
   23. Update pom files to use Xtext BOM
       (`2017 <https://github.com/osate/osate2/issues/2017>`__)

-  Error Model and Analysis Plugins

   1. EMV2Util.getErrorType(EMV2Path ep) returns null for
      bindings.NetworkError
      (`1975 <https://github.com/osate/osate2/issues/1975>`__)
   2. K ormore calculates failure probability wrong
      (`1976 <https://github.com/osate/osate2/issues/1976>`__)
   3. Error model validations should be executed while typing
      (`2034 <https://github.com/osate/osate2/issues/2034>`__)

-  AADL Diagram Editor

   1. GE-tests (`1219 <https://github.com/osate/osate2/issues/1219>`__)
   2. Element hidden during rename
      (`1992 <https://github.com/osate/osate2/issues/1992>`__)

-  ALISA

   1. Arithmetic bugs in ALISA
      (`2031 <https://github.com/osate/osate2/issues/2031>`__)

.. _known-issues-7:

Known issues
^^^^^^^^^^^^

-  Installing the OSATE plugins into “Eclipse for RCP and RAP
   Developers” prevents Eclipse from starting. See `issue
   2061 <https://github.com/osate/osate2/issues/2061>`__.

-  MacOS users must run the command
   ``sudo xattr -rd com.apple.quarantine osate2.app/`` to be able to run
   OSATE.

-  The first startup of OSATE can take a rather long (up to a couple of
   minutes).

-  Under certain conditions the outline view displays no context menu
   menu on right click. As a workaround close and re-open the editor.
   See `issue 2050 <https://github.com/osate/osate2/issues/2050>`__.

-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.6.0 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.
   Once newer versions are provided by
   `loonwerks <http://loonwerks.com>`__ in an update site, we will make
   them available via the “Install Additional OSATE Components” dialog.

   **After installing Resolute you must perform a clean build of your
   workspace, otherwise Resolute verification methods will fail with a
   class cast exception.**

Version 2.5.2
~~~~~~~~~~~~~

.. _release-8:

Release
^^^^^^^

-  **GIT tag**: 2.5.2-RELEASE
-  **Release date**: August 31, 2019
-  **Eclipse base version**: 2019-03
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.5.2/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.5.2/products

.. _sha256-hashes-for-the-downloads-8:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   84992dad5f14d2e9ff54fe1d99af0619d15d3f16d564670c2ebffefcb6414d0c  osate2-2.5.2-vfinal-linux.gtk.x86_64.tar.gz
   24875995fb405e8ac31ce2576418b1c283d107186eae405d27a6ef2c75a28e00  osate2-2.5.2-vfinal-macosx.cocoa.x86_64.tar.gz
   6ccfe9401e57d773935c9979fd29bf381f4ee4c0d01be8caf89cb874768f1b0e  osate2-2.5.2-vfinal-win32.win32.x86_64.zip

.. _notable-changes-8:

Notable changes
^^^^^^^^^^^^^^^

-  This release contains various improvements to the fault tree
   analysis.

.. _fixed-issues-8:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Flow path implementation incorrectly has error marking when
       components are modal
       (`1909 <https://github.com/osate/osate2/issues/1909>`__)
   2.  Annex parsing errors are not converted into markers
       (`1884 <https://github.com/osate/osate2/issues/1884>`__)
   3.  Missing validation for duplicate name
       (`1841 <https://github.com/osate/osate2/issues/1841>`__)
   4.  AnnexParseUtil silently discards exceptions
       (`1808 <https://github.com/osate/osate2/issues/1808>`__)
   5.  Outdated list of p2 repositories for installation
       (`1965 <https://github.com/osate/osate2/issues/1965>`__)
   6.  Flow instantiation fails silently in some conditions
       (`1809 <https://github.com/osate/osate2/issues/1809>`__)
   7.  Missing validation on call sequences
       (`1564 <https://github.com/osate/osate2/issues/1564>`__)
   8.  Online help: Scheduling analysis documentation is missing
       (`1853 <https://github.com/osate/osate2/issues/1853>`__)
   9.  Latency analysis does not produce report when model has no modes
       (`1897 <https://github.com/osate/osate2/issues/1897>`__)
   10. Unused handlers
       (`1763 <https://github.com/osate/osate2/issues/1763>`__)
   11. Documentation missing for semantic analysis of connection binding
       consistency
       (`1852 <https://github.com/osate/osate2/issues/1852>`__)
   12. MIPS budget analysis reports error if Reference_Processor is not
       specified
       (`1952 <https://github.com/osate/osate2/issues/1952>`__)
   13. Latency analysis does not scale execution time if thread is bound
       to virtual processor
       (`1966 <https://github.com/osate/osate2/issues/1966>`__)
   14. Latency analysis help is missing explanation about
       Reference_Processor and execution time scaling
       (`1956 <https://github.com/osate/osate2/issues/1956>`__)

-  Error Model and Analysis Plugins

   1.  Fault tree table shows no text in first column if it represents
       an error event
       (`1958 <https://github.com/osate/osate2/issues/1958>`__)
   2.  FTA maps error type to super error type unnecessarily
       (`1915 <https://github.com/osate/osate2/issues/1915>`__)
   3.  FTA does not handle data access, bus access correctly
       (`1899 <https://github.com/osate/osate2/issues/1899>`__)
   4.  FTA treats multiple out propagation conditions for the same our
       propagation and type incorrectly
       (`1961 <https://github.com/osate/osate2/issues/1961>`__)
   5.  FTA includes undeveloped in propagation event when type is not
       propagated
       (`1913 <https://github.com/osate/osate2/issues/1913>`__)
   6.  Support “k or more” in fault tree generation
       (`1837 <https://github.com/osate/osate2/issues/1837>`__)
   7.  FTA does not handle types with subtypes and type products well
       (`1927 <https://github.com/osate/osate2/issues/1927>`__)
   8.  FTA fails when the model is modal
       (`1907 <https://github.com/osate/osate2/issues/1907>`__)
   9.  Fault tree generator ignores fault contributors when encountering
       a trace cycle in HW
       (`1893 <https://github.com/osate/osate2/issues/1893>`__)
   10. Fault tree table does not show error source correctly under the
       first column
       (`1928 <https://github.com/osate/osate2/issues/1928>`__)
   11. Error event in FTA sometimes does not show an error type even
       when one is defined
       (`1962 <https://github.com/osate/osate2/issues/1962>`__)

-  AADL Diagram Editor

   1. OSATE Graphical Editor should move bend points when both ends are
      moved together
      (`1476 <https://github.com/osate/osate2/issues/1476>`__)
   2. Add context sensitive help to graphical editor
      (`1194 <https://github.com/osate/osate2/issues/1194>`__)
   3. Allow creating classifier when setting classifier
      (`1198 <https://github.com/osate/osate2/issues/1198>`__)

-  ALISA

   1. In case of an expression evaluation error the exception message is
      not shown in ALISA
      (`1921 <https://github.com/osate/osate2/issues/1921>`__)
   2. Common expression interpreter has problems with ‘val’ assigned a
      property whose type is RangeValue
      (`1933 <https://github.com/osate/osate2/issues/1933>`__)
   3. ALISA expression language cannot operations on range values
      (`1918 <https://github.com/osate/osate2/issues/1918>`__)
   4. The ReqSpec documentation indicates URI as reference to external
      documents but does not provide syntax details
      (`1917 <https://github.com/osate/osate2/issues/1917>`__)

.. _known-issues-8:

Known issues
^^^^^^^^^^^^

-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.5.2 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.
   Once newer versions are provided by
   `loonwerks <http://loonwerks.com>`__ in an update site, we will make
   them available via the “Install Additional OSATE Components” dialog.

   **After installing Resolute you must perform a clean build of your
   workspace, otherwise Resolute verification methods will fail with a
   class cast exception.**

Version 2.5.1
~~~~~~~~~~~~~

.. _release-9:

Release
^^^^^^^

-  **GIT tag**: 2.5.1-RELEASE
-  **Release date**: July 26, 2019
-  **Eclipse base version**: 2019-03
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.5.1/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.5.1/products

.. _sha256-hashes-for-the-downloads-9:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   21b8da862f5d53864966552b5b9c533a3ea99a8a37317250eba788ce291ebd72  osate2-2.5.1-vfinal-linux.gtk.x86_64.tar.gz
   5283f691cdde4f2ba72c870b9be3fb937ccbefb4e0802f33bda00831aeeafe09  osate2-2.5.1-vfinal-macosx.cocoa.x86_64.tar.gz
   cdded4ff77d6b240f63eb8ceafa6074bd46f50a6a2a3ffdbd04e90d93be05bbc  osate2-2.5.1-vfinal-win32.win32.x86_64.zip

.. _notable-changes-9:

Notable changes
^^^^^^^^^^^^^^^

-  Hiding and showing elements in AADL diagrams has been simplified, see
   issue `#1542 <https://github.com/osate/osate2/issues/1542>`__

.. _fixed-issues-9:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Reduce tabs in autoformatting of records and lists
       (`1825 <https://github.com/osate/osate2/issues/1825>`__)
   2.  Missing validation for number values
       (`1100 <https://github.com/osate/osate2/issues/1100>`__)
   3.  Hover text in AADL text editor is not annex aware
       (`1828 <https://github.com/osate/osate2/issues/1828>`__)
   4.  OSATE does not handle "_" in real literals
       (`1653 <https://github.com/osate/osate2/issues/1653>`__)
   5.  Cannot view flow properties in an instance file
       (`1060 <https://github.com/osate/osate2/issues/1060>`__)
   6.  Annex registry should have standalone mode
       (`1387 <https://github.com/osate/osate2/issues/1387>`__)
   7.  End to end flow not instantiated in component with refined
       features in the flow
       (`1830 <https://github.com/osate/osate2/issues/1830>`__)
   8.  Checking property consistency along connection instance does not
       work correctly
       (`665 <https://github.com/osate/osate2/issues/665>`__)
   9.  Error in instantiation when using unnamed mode transitions
       (`1839 <https://github.com/osate/osate2/issues/1839>`__)
   10. Cycle in hierarchy causes property resolution to never complete
       (`1842 <https://github.com/osate/osate2/issues/1842>`__)
   11. Property not attached to flow spec instance for instance root
       component
       (`1815 <https://github.com/osate/osate2/issues/1815>`__)
   12. Property sets and packages cannot be contributed in standalone
       mode (`1388 <https://github.com/osate/osate2/issues/1388>`__)
   13. Error and warning icon decorations in AADL Navigator are not
       updated (`1824 <https://github.com/osate/osate2/issues/1824>`__)
   14. Class OsateResourceUtil should be cleaned up
       (`1492 <https://github.com/osate/osate2/issues/1492>`__)
   15. Implementation in ExecuteJavaUtil is way too convoluted
       (`1827 <https://github.com/osate/osate2/issues/1827>`__)
   16. Cyclic project references are not detected
       (`1004 <https://github.com/osate/osate2/issues/1004>`__)
   17. Error markers when creating a flow path implementation that
       includes refined connections
       (`1831 <https://github.com/osate/osate2/issues/1831>`__)
   18. XML parser exception when opening a .gitignore file in OSATE
       (`1840 <https://github.com/osate/osate2/issues/1840>`__)
   19. Instantiation does not check overriding of constant property
       associations
       (`1447 <https://github.com/osate/osate2/issues/1447>`__)
   20. Latency analysis is run on end to end flows not part of an SOM
       (`1872 <https://github.com/osate/osate2/issues/1872>`__)
   21. Latency report improvements: SOM name
       (`1850 <https://github.com/osate/osate2/issues/1850>`__)
   22. Latency report improvements: “No latency”
       (`1851 <https://github.com/osate/osate2/issues/1851>`__)

-  Error Model and Analysis Plugins

   1. Fault trees do not always get refreshed
      (`1904 <https://github.com/osate/osate2/issues/1904>`__)
   2. Performance issue in minimal cutset calculation
      (`1880 <https://github.com/osate/osate2/issues/1880>`__)
   3. Fault trace has unnecessary events when outgoing propagation is
      specified (`1882 <https://github.com/osate/osate2/issues/1882>`__)

-  AADL Diagram Editor

   1. Hide selected elements via context menu/keyboard shortcut
      (`1542 <https://github.com/osate/osate2/issues/1542>`__)
   2. Making parameter connections in graphical editor fails
      (`1865 <https://github.com/osate/osate2/issues/1865>`__)
   3. Exception with ELK 0.5.0
      (`1911 <https://github.com/osate/osate2/issues/1911>`__)
   4. Allow diagram exporter to output to a stream
      (`1835 <https://github.com/osate/osate2/issues/1835>`__)
   5. Notes cause diagram to appear as dirty
      (`1844 <https://github.com/osate/osate2/issues/1844>`__)

-  ALISA

   1. Assure subsystem does not include verification plans if
      subcomponent only has type
      (`1816 <https://github.com/osate/osate2/issues/1816>`__)
   2. ALISA: Verification fails with class cast exception when
      verification target does not exist in instance model
      (`1812 <https://github.com/osate/osate2/issues/1812>`__)
   3. Null pointer exception in ALISA when model contains connection
      instances without cross connection
      (`1811 <https://github.com/osate/osate2/issues/1811>`__)
   4. ALISA design goal does not resolve reference to VAL
      (`1873 <https://github.com/osate/osate2/issues/1873>`__)

.. _known-issues-9:

Known issues
^^^^^^^^^^^^

-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.5.1 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.
   Once newer versions are provided by
   `loonwerks <http://loonwerks.com>`__ in an update site, we will make
   them available via the “Install Additional OSATE Components” dialog.

/ **After installing Resolute you must perform a clean build of your
workspace, otherwise Resolute verification methods will fail with a
class cast exception.**

Version 2.5.0
~~~~~~~~~~~~~

.. _release-10:

Release
^^^^^^^

-  **GIT tag**: 2.5.0-RELEASE
-  **Release date**: May 24, 2019
-  **Eclipse base version**: 2019-03
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.5.0/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.5.0/products

.. _sha256-hashes-for-the-downloads-10:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   0f7655e9fecff40b1bb3b464294e0d5bb89aa53f9a49749cee67aecfda59b723  osate2-2.5.0-vfinal-linux.gtk.x86_64.tar.gz
   97a4a313d0964b41da0d74e7ae3b3a1bf389f051f49d9827a2ace1d82d53c57c  osate2-2.5.0-vfinal-macosx.cocoa.x86_64.tar.gz
   18207ba8114eb94576ce32a01e86c4d8b6980a794677553d4e45cd1e0793cbf2  osate2-2.5.0-vfinal-win32.win32.x86_64.zip

.. _notable-changes-10:

Notable changes
^^^^^^^^^^^^^^^

-  We have updated the underlying Eclipse version to Eclipse 2019-03

.. _fixed-issues-10:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1. Missing validation for applicability of property reference
      (`1770 <https://github.com/osate/osate2/issues/1770>`__)
   2. Instance model files: References to plugin-contributed AADL
      elements are serialized as relative URIs
      (`1805 <https://github.com/osate/osate2/issues/1805>`__)
   3. Wrong feature group type validation
      (`1671 <https://github.com/osate/osate2/issues/1671>`__)
   4. AADL Navigator: New AADL package is not inserted in correct order
      (`1622 <https://github.com/osate/osate2/issues/1622>`__)
   5. OSATE doesn’t reject connection arrays in property associations
      (`1746 <https://github.com/osate/osate2/issues/1746>`__)
   6. Migrate build to Jenkins pipeline
      (`1739 <https://github.com/osate/osate2/issues/1739>`__)
   7. Upgrade to Eclipse 2019-03
      (`1762 <https://github.com/osate/osate2/issues/1762>`__)
   8. Streamline maven setup
      (`1758 <https://github.com/osate/osate2/issues/1758>`__)

-  Error Model and Analysis Plugins

   1. EMV2 doesn’t check legality of type products
      (`1222 <https://github.com/osate/osate2/issues/1222>`__)
   2. Incorrect inverse by EMV2 validator
      (`1735 <https://github.com/osate/osate2/issues/1735>`__)
   3. EMV2 properties do not handle property constants as values
      (`1792 <https://github.com/osate/osate2/issues/1792>`__)

-  AADL Diagram Editor

   1. Diagrams are always marked as changed after opening
      (`1682 <https://github.com/osate/osate2/issues/1682>`__)

-  ALISA

   1. ALISA predicate evaluation always false due to inconsistent result
      type from latency analysis
      (`1777 <https://github.com/osate/osate2/issues/1777>`__)
   2. ALISA does not support FTA for occurrence probability results
      (`1799 <https://github.com/osate/osate2/issues/1799>`__)
   3. ALISA does not allow use of val as parameter in Rationale text
      (`1790 <https://github.com/osate/osate2/issues/1790>`__)

.. _known-issues-10:

Known issues
^^^^^^^^^^^^

-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.5.0 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.
   Once newer versions are provided by
   `loonwerks <http://loonwerks.com>`__ in an update site, we will make
   them available via the “Install Additional OSATE Components” dialog.

   **After installing Resolute you must perform a clean build of your
   workspace, otherwise Resolute verification methods will fail with a
   class cast exception.**

Version 2.4.1
~~~~~~~~~~~~~

.. _release-11:

Release
^^^^^^^

-  **GIT tag**: 2.4.1-RELEASE
-  **Release date**: April 5, 2019
-  **Eclipse base version**: 2018-12
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.4.1/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.4.1/products

.. _sha256-hashes-for-the-downloads-11:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   e8dcc8606c3f800ae67be9fb86dda22965ffba24a19d50238c5798c6151580af  osate2-2.4.1-vfinal-linux.gtk.x86_64.tar.gz
   d0ec44739ce5fb89169dfd27a9a59dc4ac887beebe5475dc0a855c3e17f57391  osate2-2.4.1-vfinal-macosx.cocoa.x86_64.tar.gz
   e511dae3962cdec280a77cbb75ef30be20046e71c474829f51c60b2df6199440  osate2-2.4.1-vfinal-win32.win32.x86_64.zip

.. _notable-changes-11:

Notable changes
^^^^^^^^^^^^^^^

-  New view to show project and package dependencies.
-  Added Eclipse Mylyn support for AADL files.
-  More intuitive usage of classifier information view.
-  Improved “Install Additional OSATE Features” dialog.

.. _fixed-issues-11:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Missing property association on mode transition instance
       (`#1096 <https://github.com/osate/osate2/issues/1096>`__)
   2.  Confusing error message when installing an already installed
       OSATE component
       (`#1386 <https://github.com/osate/osate2/issues/1386>`__)
   3.  Missing validation for initial modes
       (`#1549 <https://github.com/osate/osate2/issues/1549>`__)
   4.  AADL Navigator: Replace references to EObjects with URIs
       (`#1571 <https://github.com/osate/osate2/issues/1571>`__)
   5.  Running the Instance Model Creator without Eclipse Workbench
       (`#1617 <https://github.com/osate/osate2/issues/1617>`__)
   6.  EValidator Error
       (`#1629 <https://github.com/osate/osate2/issues/1629>`__)
   7.  Project references view
       (`#1663 <https://github.com/osate/osate2/issues/1663>`__)
   8.  Add initial mylyn support to OSATE
       (`#1675 <https://github.com/osate/osate2/issues/1675>`__)
   9.  Help text describing how to find Plugin Contributed Properties in
       OSATE (`#1686 <https://github.com/osate/osate2/issues/1686>`__)
   10. Memory leak in AADL workspace build
       (`#1726 <https://github.com/osate/osate2/issues/1726>`__)
   11. org.osate.results has unnecessary dependency to org.osate.aadl
       (`#1728 <https://github.com/osate/osate2/issues/1728>`__)
   12. NPE in AADL Navigator
       (`#1732 <https://github.com/osate/osate2/issues/1732>`__)
   13. Populating classifier info view should be more intuitive
       (`#1748 <https://github.com/osate/osate2/issues/1748>`__)
   14. Textual instance model doesn’t resolve referenes to mode
       transition instances
       (`#1753 <https://github.com/osate/osate2/issues/1753>`__)
   15. Deprecate unused and questionable methods
       (`#1755 <https://github.com/osate/osate2/issues/1755>`__)
   16. Broken image links in help
       (`#1765 <https://github.com/osate/osate2/issues/1765>`__)
   17. Use SpotBugs to spot bugs.
       (`#1552 <https://github.com/osate/osate2/issues/1552>`__)
   18. Add separate repository project to build
       (`#1720 <https://github.com/osate/osate2/issues/1720>`__)
   19. Use git master branch for development
       (`#1727 <https://github.com/osate/osate2/issues/1727>`__)

-  ALISA

   1. Assure test fails
      (`#1716 <https://github.com/osate/osate2/issues/1716>`__)

.. _known-issues-11:

Known issues
^^^^^^^^^^^^

-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.4.1 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.
   Once newer versions are provided by
   `loonwerks <http://loonwerks.com>`__ in an update site, we will make
   them available via the “Install Additional OSATE Components” dialog.

   **After installing Resolute you must perform a clean build of your
   workspace, otherwise Resolute verification methods will fail with a
   class cast exception.**

Version 2.4.0
~~~~~~~~~~~~~

.. _release-12:

Release
^^^^^^^

-  **GIT tag**: 2.4.0-RELEASE
-  **Release date**: March 5, 2019
-  **Eclipse base version**: 2018-12
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.4.0/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.4.0/products

.. _sha256-hashes-for-the-downloads-12:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   a7324c5217d8ac8db2379bd5f0f6a24f6c551857e837abba93a17f331a0a3f29  osate2-2.4.0-vfinal-linux.gtk.x86_64.tar.gz
   eb7a509eacb87a9554c603b60512a5b1c273386c98baa2381aa4a399e5439df0  osate2-2.4.0-vfinal-macosx.cocoa.x86_64.tar.gz
   fd65bdea01c49019f9281a8b56e2c189d417a7e44e13e1ed69a9391bf1b7b0cd  osate2-2.4.0-vfinal-win32.win32.x86_64.zip

.. _notable-changes-12:

Notable changes
^^^^^^^^^^^^^^^

-  Added new functionality to find unused classifiers in a package.
-  Added a classifier information view that shows all features,
   subcomponents, etc., of a classifier including inherited.
-  Removed execution of Java and Python verification methods that are
   located in a project in the workspace.
-  OSATE is now based on Eclipse 2018-12
-  Resolute and AGREE are no longer integrated. The versions included in
   OSATE 2.3.7 can be installed into OSATE 2.4.0 from
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates.
   Once newer versions are provided by
   `loonwerks <http://loonwerks.com>`__ we will make them available via
   the “Install Additional OSATE Components” dialog.

.. _fixed-issues-12:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Upgrade to Eclipse 2018-09
       (`#1466 <https://github.com/osate/osate2/issues/1466>`__)
   2.  Upgrade to Eclipse 2018-12
       (`#1670 <https://github.com/osate/osate2/issues/1670>`__)
   3.  Nightly build version in Testing fails to start up on any
       workspace
       (`#1695 <https://github.com/osate/osate2/issues/1695>`__)
   4.  SMACCM stubs are included in product build
       (`#1719 <https://github.com/osate/osate2/issues/1719>`__)
   5.  Need a way to find unused classifiers in a package
       (`#1135 <https://github.com/osate/osate2/issues/1135>`__)
   6.  AADL Classifier View
       (`#1657 <https://github.com/osate/osate2/issues/1657>`__)
   7.  Exception when updating AADL property view
       (`#1685 <https://github.com/osate/osate2/issues/1685>`__)
   8.  ListType.ownedElementType Not Formatted
       (`#1697 <https://github.com/osate/osate2/issues/1697>`__)
   9.  CyberPhysical Properties and Data Types as Contributions
       (`#1703 <https://github.com/osate/osate2/issues/1703>`__)
   10. AADL Navigator: Wrong context menu entry
       (`#1705 <https://github.com/osate/osate2/issues/1705>`__)
   11. Classifier Information: Non-standard “link with editor” icon
       (`#1707 <https://github.com/osate/osate2/issues/1707>`__)
   12. OSATE contains two definitions of weight units
       (`#1721 <https://github.com/osate/osate2/issues/1721>`__)
   13. Too much underlining after unused classifier analysis
       (`#1704 <https://github.com/osate/osate2/issues/1704>`__)
   14. Invoke interface without preference switches for Latency Analysis
       got lost
       (`#1710 <https://github.com/osate/osate2/issues/1710>`__)

-  Error Model and Analysis Plugins

   1. EMV2 validation exception when using branch probabilities with
      underscores.
      (`#1647 <https://github.com/osate/osate2/issues/1647>`__)

-  Graphical Editor

   1. Font scaling calculation for diagrams is wrong on Linux
      (`#1661 <https://github.com/osate/osate2/issues/1661>`__)

-  ALISA

   1. ALISA executes code that is part of models
      (`#1604 <https://github.com/osate/osate2/issues/1604>`__)
   2. ALISA references outdated safety/security checker
      (`#1687 <https://github.com/osate/osate2/issues/1687>`__)
   3. Latency analysis is getting no class error when called from Alisa
      (`#1693 <https://github.com/osate/osate2/issues/1693>`__)
   4. Method registry reports unresolved reference error when Resolute
      is not installed
      (`#1700 <https://github.com/osate/osate2/issues/1700>`__)
   5. CyberPhysical Properties and Data Types as Contributions
      (`#1703 <https://github.com/osate/osate2/issues/1703>`__)
   6. NoClassDefFoundError exception when Resolute is not installed
      (`#1714 <https://github.com/osate/osate2/issues/1714>`__)
   7. Resolute detection and invocation has multiple issues
      (`#1724 <https://github.com/osate/osate2/issues/1724>`__)

Version 2.3.7
~~~~~~~~~~~~~

.. _release-13:

Release
^^^^^^^

-  **GIT tag**: 2.3.7-RELEASE
-  **Release date**: January 31, 2019
-  **Eclipse base version**: Oxygen.3a
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.7/products

.. _sha256-hashes-for-the-downloads-13:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   01864123ad681d805d3677a92fe699a93e159ab1aaed9d5d6ddb8ca590bda0d9  osate2-2.3.7-vfinal-linux.gtk.x86_64.tar.gz
   dadad40b7aacfb64a703411444525de51c8d5b6dce6431aabb87a268ae0e3c6f  osate2-2.3.7-vfinal-macosx.cocoa.x86_64.tar.gz
   e716eb0a7b2625eb827f623a557f45d0d24430126cb5b21e27d26ad6512ea284  osate2-2.3.7-vfinal-win32.win32.x86_64.zip
   10138025c453ccf7dd6a7c5e23faed8320c1ee39d4ae1341db3e3529dc9099f4  osate2-2.3.7-vfinal-win32.win32.x86.zip

.. _notable-changes-13:

Notable changes
^^^^^^^^^^^^^^^

-  Added AADL search functionality.
-  This is the last release based on Eclipse Oxygen, the next release
   will be based on Eclipse 2018-12.
-  This is the last release that includes a 32bit version for Windows
   because Oracle has dropped 32bit support for Java.
-  This is the last release that includes Resolute and AGREE in the
   default download. In future versions of OSATE Resolute and AGREE can
   be be installed as additional components.

.. _fixed-issues-13:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1. Remove deprecated classes
      (`#1672 <https://github.com/osate/osate2/issues/1672>`__)
   2. OSATE nightly build failing since 12/19/18
      (`#1667 <https://github.com/osate/osate2/issues/1667>`__)
   3. AADL Properties View no longer works for instance models
      (`#1658 <https://github.com/osate/osate2/issues/1658>`__)
   4. Provide AADL Search that includes Plugin Contributions
      (`#1028 <https://github.com/osate/osate2/issues/1028>`__)
   5. OSATE does not include Code Generation Annex property set
      (`#1220 <https://github.com/osate/osate2/issues/1220>`__)
   6. Instance Model Creation Crashes on Modal Properties on Threads
      included in a Thread Group
      (`#1616 <https://github.com/osate/osate2/issues/1616>`__)

-  Error Model and Analysis Plugins

   1. Probability computation for fault trees has rounding error due to
      use of Double
      (`#1649 <https://github.com/osate/osate2/issues/1649>`__)
   2. Erroneous sum of branch probabilities error
      (`#1643 <https://github.com/osate/osate2/issues/1643>`__)
   3. Fault tree root should be any component instance not just system
      instance (`#1641 <https://github.com/osate/osate2/issues/1641>`__)

-  Graphical Editor

   1. Improve graphical editor documentation
      (`#1175 <https://github.com/osate/osate2/issues/1175>`__)
   2. Basic graphical editor EMV2 support
      (`#1170 <https://github.com/osate/osate2/issues/1170>`__)
   3. Review graphical editor developer guide
      (`#1645 <https://github.com/osate/osate2/issues/1645>`__)
   4. Improve AADL property editing support in graphical editor
      (`#1169 <https://github.com/osate/osate2/issues/1169>`__)

-  ALISA

   1. Execution of Java based verification throws class not found
      exception
      (`#1638 <https://github.com/osate/osate2/issues/1638>`__)
   2. Value predicate for properties on model element does not retrieve
      value (`#1635 <https://github.com/osate/osate2/issues/1635>`__)

-  Behavior Annex

   1. In behavior annex plugin: add a prototype binding resolver for
      data component references
      (`#1631 <https://github.com/osate/osate2/issues/1631>`__)
   2. In behavior annex plugin: unit is not set for timed actions
      (`#1632 <https://github.com/osate/osate2/issues/1632>`__)

Version 2.3.6
~~~~~~~~~~~~~

.. _release-14:

Release
^^^^^^^

-  **GIT tag**: 2.3.6-RELEASE
-  **Release date**: November 15, 2018
-  **Eclipse base version**: Oxygen.3a
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.6/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.6/products

.. _sha256-hashes-for-the-downloads-14:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   ded61fcdde1056b1a303ee117aa3c5fd31cfdbe93deb7ebc3db3410aa6eb7e9b  osate2-2.3.6-vfinal-linux.gtk.x86_64.tar.gz
   79dfa684244250a2774d944dbe2bc24deb5e15b54533b9247f3fb72eb3548cba  osate2-2.3.6-vfinal-macosx.cocoa.x86_64.tar.gz
   2e99cb854746b1be4d414782b5dd5f8b6c7d5d7baf77a5103ee74d0347c391ff  osate2-2.3.6-vfinal-win32.win32.x86_64.zip
   d90ac3a54b8a9d6a670d56919f9380d4dbde926099239762da7539b31ef992c4  osate2-2.3.6-vfinal-win32.win32.x86.zip

.. _notable-changes-14:

Notable changes
^^^^^^^^^^^^^^^

1. The graphical editor now supports annotations on diagrams and can
   visualize flows and modes for instance models.
2. Added support for Python scripting to OSATE. This uses Eclipse EASE
   with Py4J. See, for example, `this
   presentation <https://www.eclipsecon.org/france2016/sites/default/files/slides/EASE-ily%20Python.pdf>`__
   for an introduction. Python can also be used to write ALISA
   verification methods (see help text).

.. _fixed-issues-14:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Project references are not set in the new AADL project wizard
       (`#1602 <https://github.com/osate/osate2/issues/1602>`__)
   2.  Don’t use cached project references in New Package Wizard
       (`#1595 <https://github.com/osate/osate2/issues/1595>`__)
   3.  AADL Navigator: Double-click on instance model content doesn’t
       open editor
       (`#1572 <https://github.com/osate/osate2/issues/1572>`__)
   4.  In modes clause attached to connection is missing when saving an
       AADL model
       (`#1551 <https://github.com/osate/osate2/issues/1551>`__)
   5.  Add import/export of working sets
       (`#1539 <https://github.com/osate/osate2/issues/1539>`__)
   6.  AnalysisResult records parameters, Result with status, no more
       recursive Diagnostic
       (`#1521 <https://github.com/osate/osate2/issues/1521>`__)
   7.  Plugin contributions node is added to all projects
       (`#1510 <https://github.com/osate/osate2/issues/1510>`__)
   8.  Setting a modal path to in-mode does not reflect change
       (`#1493 <https://github.com/osate/osate2/issues/1493>`__)
   9.  Registration of Guice injectors should be removed
       (`#1467 <https://github.com/osate/osate2/issues/1467>`__)
   10. AADL Navigator: Add node that shows project dependencies
       (`#1463 <https://github.com/osate/osate2/issues/1463>`__)
   11. AADL Navigator should show annexes
       (`#1451 <https://github.com/osate/osate2/issues/1451>`__)
   12. AADL Navigator: No status bar text for expanded file content and
       contributed AADL
       (`#1435 <https://github.com/osate/osate2/issues/1435>`__)
   13. AADL Navigator: Double click on expanded file content doesn’t
       open text editor
       (`#1432 <https://github.com/osate/osate2/issues/1432>`__)
   14. AADL Navigator: No error/warning decorations on expanded file
       content (`#1431 <https://github.com/osate/osate2/issues/1431>`__)
   15. Frequent Guice configuration errors
       (`#1321 <https://github.com/osate/osate2/issues/1321>`__)
   16. Add UI tests for the package creation wizard
       (`#1229 <https://github.com/osate/osate2/issues/1229>`__)
   17. Unused classes in core
       (`#1218 <https://github.com/osate/osate2/issues/1218>`__)
   18. Delete EMFIndexRetrieval
       (`#1036 <https://github.com/osate/osate2/issues/1036>`__)
   19. Compile OSATE without smaccm sources
       (`#1584 <https://github.com/osate/osate2/issues/1584>`__)
   20. Integrate python scripting
       (`#1480 <https://github.com/osate/osate2/issues/1480>`__)
   21. The build should be modularized
       (`#1225 <https://github.com/osate/osate2/issues/1225>`__)

-  Error Model and Analysis Plugins

   1. Add documentation for FaultTree representation
      (`#1588 <https://github.com/osate/osate2/issues/1588>`__)
   2. FaultTree is currently stored with shared subtrees replicated
      (`#1586 <https://github.com/osate/osate2/issues/1586>`__)
   3. Compile OSATE without smaccm sources
      (`#1584 <https://github.com/osate/osate2/issues/1584>`__)
   4. FTA dialog shows initial state as first requiring user to
      typically select another state
      (`#1506 <https://github.com/osate/osate2/issues/1506>`__)
   5. Quantitative FTA does not interpret occurrence probability on
      error paths
      (`#1503 <https://github.com/osate/osate2/issues/1503>`__)
   6. Probability is calculated incorrectly for OR and 1 of (XOR)
      (`#1501 <https://github.com/osate/osate2/issues/1501>`__)
   7. Transition branch probability is not always taken into account
      (`#1498 <https://github.com/osate/osate2/issues/1498>`__)
   8. Outline view for EMV2 annex should be improved
      (`#1084 <https://github.com/osate/osate2/issues/1084>`__)

-  Graphical Editor

   1. ConcurrentModificationException in saved diagram index
      (`#1612 <https://github.com/osate/osate2/issues/1612>`__)
   2. Subcomponent palette entries are missing
      (`#1567 <https://github.com/osate/osate2/issues/1567>`__)
   3. Visualize mode and flows for instance model
      (`#1177 <https://github.com/osate/osate2/issues/1177>`__)
   4. Support Annotations/Comments on Diagrams
      (`#1173 <https://github.com/osate/osate2/issues/1173>`__)

-  ALISA

   1.  Marker based plugin analyses do not work when instance model and
       analysis results are not saved
       (`#1596 <https://github.com/osate/osate2/issues/1596>`__)
   2.  Assure provides wrong message when Java verification method does
       not exist
       (`#1591 <https://github.com/osate/osate2/issues/1591>`__)
   3.  ALISA tests require Resolute
       (`#1589 <https://github.com/osate/osate2/issues/1589>`__)
   4.  Compile OSATE without smaccm sources
       (`#1584 <https://github.com/osate/osate2/issues/1584>`__)
   5.  Assurance View should not show TBD on sub-Result objects
       (`#1583 <https://github.com/osate/osate2/issues/1583>`__)
   6.  Null pointer Exception in ALISA Assure View
       (`#1579 <https://github.com/osate/osate2/issues/1579>`__)
   7.  Verify validator depends on Resolute
       (`#1577 <https://github.com/osate/osate2/issues/1577>`__)
   8.  Serialization issue when verification runs same analysis multiple
       times (`#1569 <https://github.com/osate/osate2/issues/1569>`__)
   9.  Unsupported Operation exception in AssureProcessor
       (`#1523 <https://github.com/osate/osate2/issues/1523>`__)
   10. AILSA Description does not handle references to instance objects
       (`#1517 <https://github.com/osate/osate2/issues/1517>`__)
   11. Verify does not validate instance object reference parameters
       correctly
       (`#1516 <https://github.com/osate/osate2/issues/1516>`__)
   12. Evaluation of Instance object parameters fails for Resolute
       (`#1512 <https://github.com/osate/osate2/issues/1512>`__)
   13. Verify does not resolve model element references
       (`#1509 <https://github.com/osate/osate2/issues/1509>`__)
   14. Integrate python scripting
       (`#1480 <https://github.com/osate/osate2/issues/1480>`__)
   15. The ALISA plugin verification methods should call on methods
       returning AnalysisResult objects
       (`#1474 <https://github.com/osate/osate2/issues/1474>`__)
   16. Add extension point registering Java classes whose methods can be
       invoked as verification methods
       (`#1468 <https://github.com/osate/osate2/issues/1468>`__)
   17. Assure should be stored as XML files
       (`#1289 <https://github.com/osate/osate2/issues/1289>`__)
   18. Assure uses nested Diagnostic objects which is deprecated
       (`#1288 <https://github.com/osate/osate2/issues/1288>`__)
   19. No validation that verification activity assigns compute
       variables needed for value predicate
       (`#1284 <https://github.com/osate/osate2/issues/1284>`__)
   20. Remove broken assure integration with AGREE
       (`#1106 <https://github.com/osate/osate2/issues/1106>`__)
   21. Filtering on assurance case does not show subset any more
       (`#1102 <https://github.com/osate/osate2/issues/1102>`__)

-  Resolute

   1. Null pointer exception using instance()
      (`#167 <https://github.com/smaccm/smaccm/issues/167>`__)

-  AGREE

   1. Equation variables in subcomponents do not resolve
      (`#163 <https://github.com/smaccm/smaccm/issues/163>`__)
   2. Generation of type predicates clutters results with trivial
      obligations
      (`#159 <https://github.com/smaccm/smaccm/issues/159>`__)

Version 2.3.5
~~~~~~~~~~~~~

.. _release-15:

Release
^^^^^^^

-  **GIT tag**: 2.3.5-RELEASE
-  **Release date**: August 31, 2018
-  **Eclipse base version**: Oxygen.3a
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.5/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.5/products

.. _sha256-hashes-for-the-downloads-15:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   0f6794c2671b4b52455ade7665f15684165010d9b4cc819cfab1f36e774dbb6f  osate2-2.3.5-vfinal-linux.gtk.x86_64.tar.gz
   b34ba1818aa3ab7492e59b06b8ae5cfa768b43d1d3b88f62386fdc95dbdb694d  osate2-2.3.5-vfinal-macosx.cocoa.x86_64.tar.gz
   88ebbad352fd4919bdc767950f993a0d72ac6da670aa7096630223e3dfe69ed6  osate2-2.3.5-vfinal-win32.win32.x86_64.zip
   e37d4fdae443c46a68382211264cfc544fd3f7b229f56e740d8f218aed3a3cca  osate2-2.3.5-vfinal-win32.win32.x86.zip

.. _notable-changes-15:

Notable changes
^^^^^^^^^^^^^^^

1. The AADL Navigator now supports working sets. Note that Plugin
   Contributions are now displayed in each project.
2. It is now possible to copy and paste elements in the graphical
   editor.

.. _fixed-issues-15:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  PropertyDoesNotApplyToHolderException in checkConstantProperty
       (`#1465 <https://github.com/osate/osate2/issues/1465>`__)
   2.  AADL Navigator should not sort file content
       (`#1459 <https://github.com/osate/osate2/issues/1459>`__)
   3.  Renaming a Mode throws ClassCastException
       (`#1449 <https://github.com/osate/osate2/issues/1449>`__)
   4.  Missing icon and label text for feature groups in text editor
       outline view
       (`#1434 <https://github.com/osate/osate2/issues/1434>`__)
   5.  AADL Navigator: Contributed AADL files cannot be expanded
       (`#1433 <https://github.com/osate/osate2/issues/1433>`__)
   6.  AADL Navigator: “Link with Editor” doesn’t work for component
       implementations
       (`#1430 <https://github.com/osate/osate2/issues/1430>`__)
   7.  AADL Navigator: Expanded AADL file content collapses on save
       (`#1429 <https://github.com/osate/osate2/issues/1429>`__)
   8.  Exception when formatting code which context annex which doesn’t
       support IFormatter2
       (`#1401 <https://github.com/osate/osate2/issues/1401>`__)
   9.  Help contains content for removed components
       (`#1391 <https://github.com/osate/osate2/issues/1391>`__)
   10. Missing entries in help table of contents
       (`#1390 <https://github.com/osate/osate2/issues/1390>`__)
   11. Exception in type check validation
       (`#1366 <https://github.com/osate/osate2/issues/1366>`__)
   12. Double clicking a project in AADL explorer should open it
       (`#1296 <https://github.com/osate/osate2/issues/1296>`__)
   13. Potential AnnexParseUtil Thread Safety
       (`#1146 <https://github.com/osate/osate2/issues/1146>`__)
   14. AADL Navigator Re-orders itself
       (`#1120 <https://github.com/osate/osate2/issues/1120>`__)
   15. AADL Navigator Does not Properly Support Working Sets
       (`#1056 <https://github.com/osate/osate2/issues/1056>`__)
   16. No errors for constant property associations
       (`#935 <https://github.com/osate/osate2/issues/935>`__)

-  Error Model and Analysis Plugins

   1.  FTA does not pick up new property values
       (`#1487 <https://github.com/osate/osate2/issues/1487>`__)
   2.  Safety analysis should better explain the use of
       OccurrenceDistribution
       (`#1482 <https://github.com/osate/osate2/issues/1482>`__)
   3.  Fault Tree tests use UI dependent test harness
       (`#1457 <https://github.com/osate/osate2/issues/1457>`__)
   4.  Stack Overflow in fault tree generation
       (`#1424 <https://github.com/osate/osate2/issues/1424>`__)
   5.  Serialized reference to ErrorTypes incorrectly qualified
       (`#1399 <https://github.com/osate/osate2/issues/1399>`__)
   6.  Stack overflow for cyclic error library extension
       (`#1392 <https://github.com/osate/osate2/issues/1392>`__)
   7.  transition branch probability is not taken into account in fault
       tree (`#1380 <https://github.com/osate/osate2/issues/1380>`__)
   8.  Migrate EMV2 tests to new framework
       (`#1372 <https://github.com/osate/osate2/issues/1372>`__)
   9.  Fault tree analysis always saves the resulting tree
       (`#1361 <https://github.com/osate/osate2/issues/1361>`__)
   10. Unreachable code in FlowLatencyAnalysisSwitch
       (`#1427 <https://github.com/osate/osate2/issues/1427>`__)
   11. Flow latency analysis runs with synchronous setting when the
       preference is asynchonous and vice versa
       (`#1394 <https://github.com/osate/osate2/issues/1394>`__)
   12. Update Weight Analysis to use AnalysisResult
       (`#1381 <https://github.com/osate/osate2/issues/1381>`__)
   13. Virtual processor without properties is not included in flow
       latency report
       (`#1311 <https://github.com/osate/osate2/issues/1311>`__)

-  Graphical Editor

   1. Outline color does not work for processor and memory shapes
      (`#1485 <https://github.com/osate/osate2/issues/1485>`__)
   2. Prevent tooltip contributors from being called with null business
      object (`#1419 <https://github.com/osate/osate2/issues/1419>`__)
   3. Rename DiagamElementUtil to DiagramElementUtil
      (`#1417 <https://github.com/osate/osate2/issues/1417>`__)
   4. Setting extended classifier to same classifier in graphical editor
      causes error.
      (`#1413 <https://github.com/osate/osate2/issues/1413>`__)
   5. Memory leak when graphical editor fails to load diagram
      (`#1389 <https://github.com/osate/osate2/issues/1389>`__)
   6. Prompt for Unlock When Editing Diagrams in Subversion Repository
      (`#1217 <https://github.com/osate/osate2/issues/1217>`__)
   7. Alignment Tools
      (`#1178 <https://github.com/osate/osate2/issues/1178>`__)
   8. Copy/paste of model elements in graphical editor
      (`#1167 <https://github.com/osate/osate2/issues/1167>`__)

-  ALISA

   1. AssureProcessor always saves assure and instance model files
      (`#1473 <https://github.com/osate/osate2/issues/1473>`__)
   2. Enable test of Resolute library with units
      (`#1469 <https://github.com/osate/osate2/issues/1469>`__)
   3. Reference finder does not work except in one method in ALISA
      (`#1453 <https://github.com/osate/osate2/issues/1453>`__)
   4. Documentation mentions ReqIF import
      (`#1440 <https://github.com/osate/osate2/issues/1440>`__)
   5. ReqSpec does not resolve measurement units
      (`#1421 <https://github.com/osate/osate2/issues/1421>`__)
   6. ALISA does not handle AnalysisResult returned from a Java
      verification method
      (`#1262 <https://github.com/osate/osate2/issues/1262>`__)
   7. There are no automated tests for ALSIA
      (`#1161 <https://github.com/osate/osate2/issues/1161>`__)

-  Resolute

   1. minor bug fixes

-  AGREE

   1. minor bug fixes

Version 2.3.4
~~~~~~~~~~~~~

.. _release-16:

Release
^^^^^^^

-  **GIT tag**: 2.3.4-RELEASE
-  **Release date**: July 17, 2018
-  **Eclipse base version**: Oxygen.3a
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.4/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.4/products

.. _sha256-hashes-for-the-downloads-16:

SHA256 Hashes for the downloads
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

::

   456d82b33103f2e93d83a226f34084658f1981ab3d944ee661bfacdc0233cda3  osate2-2.3.4-vfinal-linux.gtk.x86_64.tar.gz
   891ce022cb01a9fb0ec578fe9859ca55711d37805c3d7ae7eecbf027bd13e532  osate2-2.3.4-vfinal-macosx.cocoa.x86_64.tar.gz
   11d5fd0eb4dcf31ce3929dd0dcf5e0014333c8ef600822390120326a801782f2  osate2-2.3.4-vfinal-win32.win32.x86_64.zip
   895e93d6bfb877ad5d84145a6634be895c7ecfebc7170d46236be160d00e45cd  osate2-2.3.4-vfinal-win32.win32.x86.zip

.. _notable-changes-16:

Notable changes
^^^^^^^^^^^^^^^

1. Running OSATE under Java 9 or Java 10 is now supported.
2. Improvements to automated tests (speedup of >10x)

.. _fixed-issues-16:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  PropertiesLinkingDiagnosticMessageProvider is in the wrong place
       (`#1316 <https://github.com/osate/osate2/issues/1316>`__)
   2.  Aadl2GlobalScopeProvider should be generalized
       (`#1309 <https://github.com/osate/osate2/issues/1309>`__)
   3.  Need instantiation method that does not create a file and returns
       issues (`#1297 <https://github.com/osate/osate2/issues/1297>`__)
   4.  Update core and analysis tests to new pattern
       (`#1291 <https://github.com/osate/osate2/issues/1291>`__)
   5.  Error message for duplicate property sets prints internal
       representation
       (`#1280 <https://github.com/osate/osate2/issues/1280>`__)
   6.  Aadl2 standlone plugin should not use Eclipse workbench classes
       (`#1273 <https://github.com/osate/osate2/issues/1273>`__)
   7.  ResultUtil is missing some support methods
       (`#1260 <https://github.com/osate/osate2/issues/1260>`__)
   8.  Annex processing assumes that it runs inside Eclipse
       (`#1257 <https://github.com/osate/osate2/issues/1257>`__)
   9.  Instantiation always creates error markers
       (`#1255 <https://github.com/osate/osate2/issues/1255>`__)
   10. Tests should not use a workspace build
       (`#1254 <https://github.com/osate/osate2/issues/1254>`__)
   11. Multiple problems have occurred pop-up
       (`#1243 <https://github.com/osate/osate2/issues/1243>`__)
   12. Incorrect error text for feature group inverse error
       (`#1234 <https://github.com/osate/osate2/issues/1234>`__)
   13. Incorrect error about feature directions in inverse feature group
       (`#1233 <https://github.com/osate/osate2/issues/1233>`__)
   14. Check Unhandled Faults should be grouped with safety analyses
       (`#1231 <https://github.com/osate/osate2/issues/1231>`__)
   15. AADL Navigator should have New -> AADL Project in context menu
       (`#1228 <https://github.com/osate/osate2/issues/1228>`__)
   16. AADL resources which reference contributed properties are rebuilt
       needlessly
       (`#1145 <https://github.com/osate/osate2/issues/1145>`__)
   17. IGlobalScopeProvider enhancement
       (`#1089 <https://github.com/osate/osate2/issues/1089>`__)
   18. Remove unmaintained Lattix import plugin
       (`#1373 <https://github.com/osate/osate2/issues/1373>`__)
   19. Update flow latency plugin for usability / consistency
       (`#1322 <https://github.com/osate/osate2/issues/1322>`__)
   20. Resolute and Agree plugin dependencies are not optional
       (`#1293 <https://github.com/osate/osate2/issues/1293>`__)
   21. Update core and analysis tests to new pattern
       (`#1291 <https://github.com/osate/osate2/issues/1291>`__)
   22. Latency analysis result contains unnecessary data and description
       is not a section under Latency Analysis
       (`#1261 <https://github.com/osate/osate2/issues/1261>`__)
   23. Latency analysis parameters are not passed in explicitly but via
       Preference settings
       (`#1250 <https://github.com/osate/osate2/issues/1250>`__)

-  Error Model and Analysis Plugins

   1. Exception when serializing EMV2
      (`#1327 <https://github.com/osate/osate2/issues/1327>`__)
   2. EMV2 uses a string to identify a Resolute function instead of a
      reference
      (`#1302 <https://github.com/osate/osate2/issues/1302>`__)
   3. Annex parser and linker should not be in a UI plugin
      (`#1268 <https://github.com/osate/osate2/issues/1268>`__)
   4. Old FTA code is still present in the EMV2 feature
      (`#1157 <https://github.com/osate/osate2/issues/1157>`__)
   5. Fault Tree Viewer without Modeling Nature
      (`#1101 <https://github.com/osate/osate2/issues/1101>`__)
   6. Support conditional Error Flows and Events
      (`#1094 <https://github.com/osate/osate2/issues/1094>`__)
   7. Create a formatter for EMV2 annex libraries and subclauses
      (`#1085 <https://github.com/osate/osate2/issues/1085>`__)

-  Graphical Editor

   1. Reworked Undo/Redo Support.
      (`#1182 <https://github.com/osate/osate2/issues/1182>`__)
   2. Added menu option for removing bendpoints from selected
      connections.
      (`#1210 <https://github.com/osate/osate2/issues/1210>`__)
   3. Added menu option for selecting all connections.
      (`#1210 <https://github.com/osate/osate2/issues/1210>`__)
   4. Added option to set extended classifier to none.
      (`#1336 <https://github.com/osate/osate2/issues/1336>`__)
   5. Fixed erroneous unsaved diagram change indicator.
      (`#1246 <https://github.com/osate/osate2/issues/1246>`__)
   6. Fixed creation of unnecessary with statements.
      (`#1342 <https://github.com/osate/osate2/issues/1342>`__)
   7. Fixed memory management issues.
      (`#1307 <https://github.com/osate/osate2/issues/1307>`__)
   8. Added API for Exporting Diagrams.
      (`#1176 <https://github.com/osate/osate2/issues/1176>`__)

-  ALISA

   1.  null pointer exception when editing
       (`#1332 <https://github.com/osate/osate2/issues/1332>`__)
   2.  Assurance View in ALISA does not always update itself
       (`#1331 <https://github.com/osate/osate2/issues/1331>`__)
   3.  Resolute compute function result is not included in assure
       structure
       (`#1329 <https://github.com/osate/osate2/issues/1329>`__)
   4.  Icons for Failure and Error are confusing
       (`#1324 <https://github.com/osate/osate2/issues/1324>`__)
   5.  global requirements on connection, flow do not have target in
       assure instance
       (`#1323 <https://github.com/osate/osate2/issues/1323>`__)
   6.  Verify method registry uses identifier to refer to Resolute
       function rather than qualified name
       (`#1301 <https://github.com/osate/osate2/issues/1301>`__)
   7.  Alisa interface to Resolute has extra diagnostics
       (`#1300 <https://github.com/osate/osate2/issues/1300>`__)
   8.  Resolute and Agree plugin dependencies are not optional
       (`#1293 <https://github.com/osate/osate2/issues/1293>`__)
   9.  Incorrect result status when requirement target has no results
       from plugin analysis
       (`#1279 <https://github.com/osate/osate2/issues/1279>`__)
   10. ALISA should examine both Failure and Error issues to determine
       verification success
       (`#1276 <https://github.com/osate/osate2/issues/1276>`__)
   11. Return value from a Java verification method is not assigned to a
       compute variable and evaluated by the predicate
       (`#1275 <https://github.com/osate/osate2/issues/1275>`__)
   12. Execution of latency analysis from ALISA does not hold on to
       AnalysisResult for successive result lookup
       (`#1272 <https://github.com/osate/osate2/issues/1272>`__)
   13. Requirement predicate has execution error when compute variables
       have no values
       (`#1267 <https://github.com/osate/osate2/issues/1267>`__)
   14. ALISA does not handle ResoluteFailExceptions
       (`#1266 <https://github.com/osate/osate2/issues/1266>`__)
   15. global requirements on features and flows are not handled
       (`#1265 <https://github.com/osate/osate2/issues/1265>`__)
   16. Update ALISA documentation on global requirements and guidance in
       writing verification methods
       (`#1259 <https://github.com/osate/osate2/issues/1259>`__)
   17. Verification activity with method and requirement for feature
       incorrectly marked with error
       (`#1240 <https://github.com/osate/osate2/issues/1240>`__)
   18. ALISA does not report negative latency results any more
       (`#1223 <https://github.com/osate/osate2/issues/1223>`__)
   19. Incorrect inconsistency reported between requirement target and
       verification method target
       (`#1160 <https://github.com/osate/osate2/issues/1160>`__)
   20. ALISA does not handle assurance cases on subsystems
       (`#1159 <https://github.com/osate/osate2/issues/1159>`__)

-  Resolute

   1. Resolute debug built-in method writes to System.out which does not
      show in OSATE
      (`#143 <https://github.com/smaccm/smaccm/issues/143>`__)
   2. Resolute can retrive property value but not values of property
      constants (`#144 <https://github.com/smaccm/smaccm/issues/144>`__)
   3. Mixing claim functions and compute functions in binary operations
      in the Resolute Prover
      (`#127 <https://github.com/smaccm/smaccm/issues/127>`__)
   4. Incorrect comparison of instances in Resolute Evaluator
      (`#129 <https://github.com/smaccm/smaccm/issues/129>`__)
   5. Does connections function return {connection} or [connection]
      (`#136 <https://github.com/smaccm/smaccm/issues/136>`__)
   6. Resolute fail expression and built-in function type shortcomings
      (`#137 <https://github.com/smaccm/smaccm/issues/137>`__)
   7. Resolute documentation is out of date
      (`#139 <https://github.com/smaccm/smaccm/issues/139>`__)

-  AGREE

   1. Added support for editing AGREE models via the OSATE graphical
      editor
   2. Generation of type predicates clutters results with trivial
      obligations
      (`#159 <https://github.com/smaccm/smaccm/issues/159>`__)

Version 2.3.3
~~~~~~~~~~~~~

.. _release-17:

Release
^^^^^^^

-  **GIT tag**: 2.3.3-RELEASE
-  **Release date**: May 4, 2018
-  **Eclipse base version**: Oxygen.3a
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.3/updates
-  **Download URL**:
   http://osate-build.sei.cmu.edu/download/osate/stable/2.3.3/products

.. _notable-changes-17:

Notable changes
^^^^^^^^^^^^^^^

1. There is a new diagrams view.
2. Improved code coverage for weight, resource budget, and flow latency
   analysis tests uncovered several bugs, which were fixed.
3. There is now a single command to run an FHA, the FHA variant is
   selected via a preference.

.. _fixed-issues-17:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Fixed a class cast exception when generating fault tree
       (`#1163 <https://github.com/osate/osate2-core/issues/1163>`__)
   2.  Fixed error “representations.aird resource has been externally
       changed, should we reload it?” when opening a fault tree
       (`#1162 <https://github.com/osate/osate2-core/issues/1162>`__)
   3.  OSATE has been updated to Oxygen.3
       (`#1155 <https://github.com/osate/osate2-core/issues/1155>`__)
   4.  Property set wizard now checks for name conflicts
       (`#1154 <https://github.com/osate/osate2-core/issues/1154>`__)
   5.  Fixed missing queuing latency on data ports and extra sampling
       latency on queuing ports
       (`#1152 <https://github.com/osate/osate2-core/issues/1152>`__)
   6.  Use correct Sirius version
       (`#1149 <https://github.com/osate/osate2-core/issues/1149>`__)
   7.  Added missing per byte computation when only wrapper data size
       given
       (`#1144 <https://github.com/osate/osate2-core/issues/1144>`__)
   8.  Include virtual bus latency contribution if requires VB
       (`#1143 <https://github.com/osate/osate2-core/issues/1143>`__)
   9.  Queuing latency now calculated correctly for sporadic or periodic
       threads
       (`#1142 <https://github.com/osate/osate2-core/issues/1142>`__)
   10. On connections from outside a partition both major frame and
       offset latency were added for a given partition
       (`#1141 <https://github.com/osate/osate2-core/issues/1141>`__)
   11. Use specified connection latency when binding target has no
       latency
       (`#1140 <https://github.com/osate/osate2-core/issues/1140>`__)
   12. Latency contribution by virtual bus and sampling latency by buses
       and virtual buses are now included
       (`#1139 <https://github.com/osate/osate2-core/issues/1139>`__)
   13. Global requirements added in assurance plans and system
       requirements were sometimes ignored
       (`#1137 <https://github.com/osate/osate2-core/issues/1137>`__)
   14. Added hover support for verification activities
       (`#1136 <https://github.com/osate/osate2-core/issues/1136>`__)
   15. Support **when** condition on requirements
       (`#1133 <https://github.com/osate/osate2-core/issues/1133>`__)
   16. Flow latency analysis used wrong property in some cases
       (`#1127 <https://github.com/osate/osate2-core/issues/1127>`__)
   17. Fixed a NullPointerException in Flow Latency Analysis
       (`#1126 <https://github.com/osate/osate2-core/issues/1126>`__)
   18. Verification of global requirements on instance root only
       (`#1123 <https://github.com/osate/osate2-core/issues/1123>`__)
   19. Fix handling of global requirements on connections in assure
       generation
       (`#1122 <https://github.com/osate/osate2-core/issues/1122>`__)
   20. Updated Sirius to version 5.1.0
       (`#1118 <https://github.com/osate/osate2-core/issues/1118>`__)
   21. Added SWTBot GEF to Setup File
       (`#1116 <https://github.com/osate/osate2-core/issues/1116>`__)
   22. Fixed typo in wizard title
       (`#1114 <https://github.com/osate/osate2-core/issues/1114>`__)
   23. Updated documentation for the new AADL package wizard
       (`#1109 <https://github.com/osate/osate2-core/issues/1109>`__)
   24. Removed dependency on D-Cace
       (`#1095 <https://github.com/osate/osate2-core/issues/1095>`__)
   25. Cleaned up Assure execution engine - use of Issue and stand alone
       call of Resolute Claim Functions
       (`#1093 <https://github.com/osate/osate2-core/issues/1093>`__)
   26. Instantiation failed when referencing a required mode in a
       property association.
       (`#1092 <https://github.com/osate/osate2-core/issues/1092>`__)
   27. Fixed a gate logic optimization problem in fault tree generation
       (`#1088 <https://github.com/osate/osate2-core/issues/1088>`__)
   28. **All** in error flows was not handled correctly in fault tree
       generation
       (`#1087 <https://github.com/osate/osate2-core/issues/1087>`__)
   29. Improved test coverage for fault tree and cut set generation
       (`#1086 <https://github.com/osate/osate2-core/issues/1086>`__)
   30. Added preference to select FHA version
       (`#1083 <https://github.com/osate/osate2-core/issues/1083>`__)
   31. Fixed an XtextReconcilerJob error while editing text
       (`#1082 <https://github.com/osate/osate2-core/issues/1082>`__)
   32. Asymmetric SOM handling
       (`#1079 <https://github.com/osate/osate2-core/issues/1079>`__)
   33. Better separation of flow latency analysis from handler
       (`#1078 <https://github.com/osate/osate2-core/issues/1078>`__)
   34. Fixed NPE in bound resource allocations analysis
       (`#1075 <https://github.com/osate/osate2-core/issues/1075>`__)
   35. Weight analysis considered too many connections
       (`#1071 <https://github.com/osate/osate2-core/issues/1071>`__)
   36. Connection bindings are now handled by fault tree generator
       (`#1062 <https://github.com/osate/osate2-core/issues/1062>`__)
   37. Restructured preference settings
       (`#1061 <https://github.com/osate/osate2-core/issues/1061>`__)
   38. Simplified analysis result data structure
       (`#1055 <https://github.com/osate/osate2-core/issues/1055>`__)
   39. Safety Analysis documentation is now properly included in online
       help
       (`#1049 <https://github.com/osate/osate2-core/issues/1049>`__)
   40. Latency Analysis documentation is now properly included online
       help
       (`#1048 <https://github.com/osate/osate2-core/issues/1048>`__)
   41. AADL package wizard now checks for name conflicts
       (`#1044 <https://github.com/osate/osate2-core/issues/1044>`__)
   42. Moved Resolute help to smaccm repo
       (`#1015 <https://github.com/osate/osate2-core/issues/1015>`__)
   43. Integrated help text markdown to HTML conversion into build
       (`#1013 <https://github.com/osate/osate2-core/issues/1013>`__)
   44. Updated splash screen
       (`#1010 <https://github.com/osate/osate2-core/issues/1010>`__)
   45. ALISA dependency on Resolute/AGREE is now optional
       (`#926 <https://github.com/osate/osate2-core/issues/926>`__)
   46. Fixed instantiation error with extended inverse feature group
       type (`#818 <https://github.com/osate/osate2-core/issues/818>`__)

-  Graphical Editor

   1. Added Diagrams View.
      (`#214 <https://github.com/osate/osate-ge/issues/214>`__)
   2. Added ability to show diagram element as image.
      (`#154 <https://github.com/osate/osate-ge/issues/154>`__)
   3. Improved performance with diagrams which a large number of
      connections.
      (`#290 <https://github.com/osate/osate-ge/issues/290>`__)
   4. Improved automatic layout by allowing layout algorithm to
      optionally ignore feature direction when positioning port.
      (`#325 <https://github.com/osate/osate-ge/issues/325>`__)
   5. Added support for diagrams which are not associated with a
      particular model element. Such diagrams allow displaying multiple
      packages in a single diagram.
      (`#213 <https://github.com/osate/osate-ge/issues/213>`__)
   6. Added AADL Diagram wizard.
      (`#213 <https://github.com/osate/osate-ge/issues/213>`__)

-  Resolute

   1. Resolute collection semantics
      (`#91 <https://github.com/smaccm/smaccm/issues/91>`__)
   2. Restore non-short-circuit behavior for logical operator evaluation
      in claims (`#122 <https://github.com/smaccm/smaccm/issues/122>`__)
   3. Fix exception computing return type of list/set function
      (`#121 <https://github.com/smaccm/smaccm/issues/121>`__)
   4. Fix stack overflow in Resolute validation
      (`#117 <https://github.com/smaccm/smaccm/issues/117>`__)
   5. Fix connected function to correctly handle connection instances
      (`#100 <https://github.com/smaccm/smaccm/issues/100>`__)
   6. Remove remnants of D-Case export
      (`#93 <https://github.com/smaccm/smaccm/issues/93>`__)

-  AGREE

   1.  Analysis of AGREE models with unspecified AADL properties
       (`#98 <https://github.com/smaccm/smaccm/issues/98>`__)
   2.  Support analysis on pure event ports
       (`#57 <https://github.com/smaccm/smaccm/issues/57>`__)
   3.  Support AADL data subranges in AGREE
       (`#76 <https://github.com/smaccm/smaccm/issues/76>`__)
   4.  Add ability for AGREE to access AADL property constants
       (`#77 <https://github.com/smaccm/smaccm/issues/77>`__)
   5.  Update model checker to Jkind v4.0.1
       (`#83 <https://github.com/smaccm/smaccm/issues/83>`__)
   6.  Add case handling type evaluation of enumerations as data
       subcomponent types
       (`#124 <https://github.com/smaccm/smaccm/issues/124>`__)
   7.  Refactor AgreeScopeProvider to fix scoping omissions
       (`#110 <https://github.com/smaccm/smaccm/issues/110>`__,
       `#12 <https://github.com/smaccm/smaccm/issues/12>`__)
   8.  Fix erroneous typing of properties
       (`#74 <https://github.com/smaccm/smaccm/issues/74>`__)
   9.  Fix problem scoping NodeDef from other packages
       (`#78 <https://github.com/smaccm/smaccm/issues/78>`__)
   10. Fix spurious validation errors from re-used ids in linearization
       and record definitions
       (`#102 <https://github.com/smaccm/smaccm/issues/102>`__)
   11. Disallow property statements in annex libraries
       (`#103 <https://github.com/smaccm/smaccm/issues/103>`__)
   12. Allow executing AGREE analysis and TCG from graphical editor
       (`#105 <https://github.com/smaccm/smaccm/issues/105>`__)
   13. Subrange type predicates should be obligations, not assertions
       (`#96 <https://github.com/smaccm/smaccm/issues/96>`__)
   14. Fix incorrect references to figures in AGREE documentation
       (`#88 <https://github.com/smaccm/smaccm/issues/88>`__)
   15. Fix missing variables in counter example views
       (`#75 <https://github.com/smaccm/smaccm/issues/75>`__)
   16. Serialization fixes
       (`#84 <https://github.com/smaccm/smaccm/issues/84>`__)
   17. Fix scoping of enumerators
       (`#81 <https://github.com/smaccm/smaccm/issues/81>`__)
   18. Fix ‘Check Realizability’ analysis causes Xtext exception (and
       possible crash)
       (`#79 <https://github.com/smaccm/smaccm/issues/79>`__)

.. _known-issues-12:

Known Issues
^^^^^^^^^^^^

1. Running OSATE under Java 9 or Java 10 is not supported.
2. Using the AADL Property View to edit property values results in bad
   formatting.

Version 2.3.2
~~~~~~~~~~~~~

.. _release-18:

Release
^^^^^^^

-  **GIT tag**: 2.3.2-RELEASE
-  **Release date**: March 5, 2018
-  **Eclipse base version**: Oxygen.2
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.3.2/updates
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.3.2/products

.. _notable-changes-18:

Notable changes
^^^^^^^^^^^^^^^

1. Diagrams created with this version of OSATE will not work properly
   with older versions of OSATE. A warning will be displayed when
   opening such diagrams in an older versions of OSATE.
2. The graphical editor’s diagram configuration options have been
   redesigned and predefined diagram types have been added. Existing
   diagrams associated with AADL packages will be converted to *Package*
   diagrams. Existing diagrams associated with AADL classifiers will be
   converted to *Structure* diagrams. See the user guide for additional
   details.
3. The context menu for the graphical editor has been redesigned. Model
   editing functionality which was previously in the context menu has
   been moved to the eclipse *Properties* view. This view can be
   accessed by double-clicking a diagram element.

.. _fixed-issues-18:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  AND gates were getting lost in fault tree generation from
       composite state logic.
       (`#988 <https://github.com/osate/osate2-core/issues/988>`__)
   2.  Added AADL project wizard to navigator context menu.
       (`#989 <https://github.com/osate/osate2-core/issues/989>`__)
   3.  Fixed exception when creating abstract feature in graphical
       editor.
       (`#990 <https://github.com/osate/osate2-core/issues/990>`__)
   4.  EMV2: composite parts fault tree based on error states only.
       (`#992 <https://github.com/osate/osate2-core/issues/992>`__)
   5.  EMV2: propagation path cannot point to propagation point without
       subcomponent.
       (`#993 <https://github.com/osate/osate2-core/issues/993>`__)
   6.  Fixed bug with flow through call in call sequence.
       (`#994 <https://github.com/osate/osate2-core/issues/994>`__)
   7.  Process user defined error propagation paths.
       (`#995 <https://github.com/osate/osate2-core/issues/995>`__)
   8.  Reinstantiate command is now properly enabled on instance models.
       (`#997 <https://github.com/osate/osate2-core/issues/997>`__)
   9.  OSATE no longer requires ‘with EMV2’ for models containing error
       modeling annex elements.
       (`#1002 <https://github.com/osate/osate2-core/issues/1002>`__)
   10. EMV2: presentation improvements and better handling of state
       types and optional type constraints.
       (`#1005 <https://github.com/osate/osate2-core/issues/1005>`__)
   11. Improved fault tree integration tests to check content
       structurally.
       (`#1006 <https://github.com/osate/osate2-core/issues/1006>`__)
   12. Fixed a name resolution issues.
       (`#1009 <https://github.com/osate/osate2-core/issues/1009>`__)
   13. Updated the OSATE user guide.
       (`#1012 <https://github.com/osate/osate2-core/issues/1012>`__)
   14. Fixed exception when renaming a subprogram call.
       (`#1021 <https://github.com/osate/osate2-core/issues/1021>`__)
   15. Fixed deadlock when instantiating models with errors.
       (`#1024 <https://github.com/osate/osate2-core/issues/1024>`__)
   16. Inverse feature group were badly formatted when modifying them in
       the graphical editor.
       (`#1026 <https://github.com/osate/osate2-core/issues/1026>`__)
   17. Provide single wizard for new AADL package (textual or
       graphical).
       (`#1029 <https://github.com/osate/osate2-core/issues/1029>`__)
   18. Fault impact analysis included error events as starting points
       incorrectly.
       (`#1037 <https://github.com/osate/osate2-core/issues/1037>`__)
   19. Fault impact and fault tree analysis now interpret “all” in error
       flows.
       (`#1038 <https://github.com/osate/osate2-core/issues/1038>`__)
   20. Changes in the graphical editor no longer insert extra newlines
       in text.
       (`#1043 <https://github.com/osate/osate2-core/issues/1043>`__)
   21. Latency report now spells out preference settings.
       (`#1050 <https://github.com/osate/osate2-core/issues/1050>`__)
   22. User defined propagation paths to features are now supported.
       (`#1053 <https://github.com/osate/osate2-core/issues/1053>`__)
   23. Fixed a fault tree generation issue with type set and multi state
       transitions.
       (`#1057 <https://github.com/osate/osate2-core/issues/1057>`__)
   24. Handle inherited actual processor bindings when computing error
       propagation paths.
       (`#1058 <https://github.com/osate/osate2-core/issues/1058>`__)
   25. Process mix of error flows and outgoing propagation conditions to
       compute error propagation paths.
       (`#1059 <https://github.com/osate/osate2-core/issues/1059>`__)
   26. Fixed exception when using the graphical editor without text
       editor open.
       (`#1063 <https://github.com/osate/osate2-core/issues/1063>`__)
   27. Updated latency and safety analysis documentation.
       (`#1065 <https://github.com/osate/osate2-core/issues/1065>`__)
   28. Fixed icons and added missing icons to outline view.
       (`#1069 <https://github.com/osate/osate2-core/issues/1069>`__)
   29. Don’t add additional spaces to annex subclauses when using the
       graphical editor without a text editor open.
       (`#1074 <https://github.com/osate/osate2-core/issues/1074>`__)
   30. Removed duplicate entries in fault tree.
       (`#1081 <https://github.com/osate/osate2-core/issues/1081>`__)

-  Graphical Editor

   1. Fixed appearance properties settings only working on Windows.
      (`#282 <https://github.com/osate/osate-ge/issues/282>`__)
   2. Fixed change indicators appearing when a change had not been made
      to the diagram.
      (`#270 <https://github.com/osate/osate-ge/issues/270>`__)
   3. Reworked context menu.

      -  Replaced menu items related to modifying the AADL model with
         additions to the eclipse *Properties* view. Double-clicking a
         diagram element will open the *Properties* view.
         (`#212 <https://github.com/osate/osate-ge/issues/212>`__)
      -  Menu items for adjusting diagram contents has been reworked.
         (`#211 <https://github.com/osate/osate-ge/issues/211>`__)
      -  Reorganized context menu items.

   4. Reworked content filtering and added document types.
      (`#211 <https://github.com/osate/osate-ge/issues/211>`__)
   5. Loosened editing rules. Classifiers can be edited by modifying a
      graphical subcomponent or feature group. Can create a component
      implementation without manually creating a component
      type.(`#193 <https://github.com/osate/osate-ge/issues/193>`__)
   6. Fixed cases in which diagram layout failed to execute.

-  Resolute/AGREE

   1. Added AGREE documentation.
   2. A couple of bug fixes.

.. _known-issues-13:

Known Issues
^^^^^^^^^^^^

1. Using the AADL Property View to edit property values results in bad
   formatting.

Version 2.3.1
~~~~~~~~~~~~~

.. _release-19:

Release
^^^^^^^

-  **GIT tag**: 2.3.1-RELEASE
-  **Release date**: January 3, 2018
-  **Eclipse base version**: Oxygen.1A
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.3.1/updates
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.3.1/products

.. _notable-changes-19:

Notable changes
^^^^^^^^^^^^^^^

1. Complete redesign of the menu structure and the toolbar. In the
   process some unmaintained or defective commands and analyses were
   removed (Generate Marker Report, Report Generator Settings, Clear
   Eclipse History, Remove Problem Markers, Save as XMI, Model
   Statistics, Import Scade Model, Graphically view instances and
   implementations, Common Mode Assessment, Reliability Block Diagram,
   ImplementationCompliance, Spotlight).
2. Added new wizards for all file types supported by OSATE.
3. The underlying Eclipse is updated to Oxygen.1A.
4. Implemented new automatic layout capability to the graphical editor.
   A preference to control the incremental layout mode is located at
   OSATE Preferences/Diagrams. See OSATE Graphical Editor User Guide for
   additional details.
5. Reworked instance model diagram referencing system. When opening such
   diagrams, the user will be prompted to relink instance model diagrams
   with the appropriate instance model. Relinked diagrams will not be
   compatible with older versions of OSATE.

.. _fixed-issues-19:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1.  Support flows through subprogram calls.
       (`#929 <https://github.com/osate/osate2-core/issues/929>`__)
   2.  Fixed bug in validation of flow implementations.
       (`#931 <https://github.com/osate/osate2-core/issues/931>`__)
   3.  Support error model properties on untyped feature groups.
       (`#963 <https://github.com/osate/osate2-core/issues/963>`__)
   4.  New command to install additional OSATE components under Help
       menu.
       (`#933 <https://github.com/osate/osate2-core/issues/933>`__)
   5.  Remove obsolete .aadlsettings directory in AADL projects.
       (`#729 <https://github.com/osate/osate2-core/issues/729>`__,
       `#974 <https://github.com/osate/osate2-core/issues/974>`__)
   6.  AADL project icons are again decorated with ‘A’ instead of ‘X’.
       (`#437 <https://github.com/osate/osate2-core/issues/437>`__)
   7.  Provide complete set of file creation wizards for AADL and ALSIA
       languages.
       (`#946 <https://github.com/osate/osate2-core/issues/946>`__)
   8.  Added code coverage tool (jacoco) to tycho build.
       (`#934 <https://github.com/osate/osate2-core/issues/934>`__)
   9.  Support properties on connection error source.
       (`#954 <https://github.com/osate/osate2-core/issues/954>`__)
   10. Added binding paths to propagation analysis.
       (`#962 <https://github.com/osate/osate2-core/issues/962>`__)
   11. Updated MILSTD882 and ARP4761 property sets.
       (`#956 <https://github.com/osate/osate2-core/issues/956>`__,
       `#967 <https://github.com/osate/osate2-core/issues/967>`__)
   12. Fixed a text editor crash.
       (`#957 <https://github.com/osate/osate2-core/issues/957>`__)
   13. New icons for several analyses.
       (`#938 <https://github.com/osate/osate2-core/issues/938>`__)
   14. Disable instantiation for component types.
       (`#943 <https://github.com/osate/osate2-core/issues/943>`__)
   15. Fixed a null pointer exception.
       (`#953 <https://github.com/osate/osate2-core/issues/953>`__)
   16. Bug fixes for latency analysis.
       (`#942 <https://github.com/osate/osate2-core/issues/942>`__,
       `#955 <https://github.com/osate/osate2-core/issues/955>`__,
       `#944 <https://github.com/osate/osate2-core/issues/944>`__,
       `#939 <https://github.com/osate/osate2-core/issues/939>`__)
   17. Updated tests for FTA.
       (`#930 <https://github.com/osate/osate2-core/issues/930>`__)
   18. Cleaned up menus and toolbar.
       (`#928 <https://github.com/osate/osate2-core/issues928>`__)

-  Graphical Editor

   1. Added ability to show Mode Transition Triggers as labels.
      (`#244 <https://github.com/osate/osate-ge/issues/244>`__)
   2. Reworked flow and mode highlighting.
      (`#133 <https://github.com/osate/osate-ge/issues/133>`__)
   3. Reworked automatic layout support by integrating the Eclipse
      Layout Kernel(ELK).
      (`#158 <https://github.com/osate/osate-ge/issues/158>`__)
   4. Added capability to correct broken reference to the AADL model.
      (`#136 <https://github.com/osate/osate-ge/issues/136>`__)
   5. Prevented showing both Implements and Extends relationships for
      the same component implementation.
      (`#254 <https://github.com/osate/osate-ge/issues/254>`__)
   6. Fixed Arrays having invalid names when renaming.
      (`#254 <https://github.com/osate/osate-ge/issues/262>`__)
   7. Added support for show bindings in instance Model
      (`#196 <https://github.com/osate/osate-ge/issues/196>`__)

-  Resolute/AGREE

   1. Bug fixes

.. _known-issues-14:

Known Issues
^^^^^^^^^^^^

1. Using the AADL Property View to edit property values results in bad
   formatting.
2. End points for connections representing mode transitions triggers and
   property values which reference connections are incorrect if the mode
   transition or referenced connection does not contain a bendpoint.

Version 2.3.0
~~~~~~~~~~~~~

.. _release-20:

Release
^^^^^^^

-  **GIT tag**: 2.3.0-RELEASE
-  **Release date**: November 9, 2017
-  **Eclipse base version**: Oxygen.1
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.3.0/updates
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.3.0/products

.. _notable-changes-20:

Notable changes
^^^^^^^^^^^^^^^

1. The underlying Eclipse is updated to Oxygen1.
2. Property sets and packages contributed by plugins are no longer
   copied as files into each workspace. Existing workspaces will be
   migrated automatically.
3. The FTA and minimal cut set calculation have been rewritten. The
   fault tree uses a new graphical representation.

.. _fixed-issues-20:

Fixed issues
^^^^^^^^^^^^

-  OSATE Core and Analysis Plugins

   1. Created an EMF based generic analysis result format
      (`#898 <https://github.com/osate/osate2-core/issues/898>`__)
   2. Latency analysis updated to use new result format
      (`#902 <https://github.com/osate/osate2-core/issues/902>`__)
   3. Plugin contributed resources are shown in the navigator but lo
      longer copied into the workspace
      (`#527 <https://github.com/osate/osate2-core/issues/527>`__)
   4. Abstract features were serialized with keyword ``prototype``
      (`#883 <https://github.com/osate/osate2-core/issues/883>`__)
   5. Behavior annex errors are now processed correctly
      (`#891 <https://github.com/osate/osate2-core/issues/891>`__)
   6. Created new representation for fault propagation graphs and fault
      trees (`#901 <https://github.com/osate/osate2-core/issues/901>`__)

-  Graphical Editor

   1. Added basic formatting support. This includes adjusting the
      outline color, fill color, text color, line size, and
      font-size.(`#151 <https://github.com/osate/osate-ge/issues/151>`__)
   2. Added options to toggle connection label visibility on a
      per-diagram or per connection basis.
      (`#239 <https://github.com/osate/osate-ge/issues/239>`__)
   3. Port graphic and connection point adjustments.
      (`#228 <https://github.com/osate/osate-ge/issues/228>`__)(`#229 <https://github.com/osate/osate-ge/issues/229>`__)
   4. Mode transitions now use free-form connections.
      (`#236 <https://github.com/osate/osate-ge/issues/236>`__)
   5. Mode assignments is now performed using the Properties view. Modes
      can be assigned to multiple elements simultaneously.
      (`#200 <https://github.com/osate/osate-ge/issues/200>`__)
   6. Double-clicking a model element now opens the Properties view. The
      properties view allows the modification of diagram element
      formatting and model element properties. Additional properties
      will be added in subsequent releases.

-  Resolute/AGREE

   1. Bug fixes

.. _known-issues-15:

Known Issues
^^^^^^^^^^^^

1. Using the AADL Property View to edit property values results in bad
   formatting.

Version 2.2.3 update 01
~~~~~~~~~~~~~~~~~~~~~~~

.. _release-21:

Release
^^^^^^^

-  **GIT tag**: 2.2.3-UPDATE01
-  **Release date**: September 6, 2017
-  **Eclipse base version**: Mars.2
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.2.3/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.2.3/products

This is a maintenance release that contains bug fixes for the graphical
editor.

.. _notable-changes-21:

Notable changes
^^^^^^^^^^^^^^^

1. Adjusted the data types of several fields in the diagram meta-model.
   Unfortunately, the this breaks forward compatibility. The original
   2.2.3 release will not be able to correctly parse diagrams saved with
   newer versions. However the change is backward compatible. The
   updated version will work with diagrams created with the original
   2.2.3 release.

.. _fixed-issues-21:

Fixed issues
^^^^^^^^^^^^

-  Graphical Editor

   1. Fixes elements being assigned duplicate id’s. As a result, AADL
      properties were not represented accurately.
   2. Fixed case where a rename refactoring caused a NPE.
   3. Fixes flow implementations not appearing the drop-down list to be
      highlighted.
   4. Fixes multiple errors and race conditions with diagram indexing.
   5. Fixes exception when opening empty AADL file
      (`#218 <https://github.com/osate/osate-ge/issues/218>`__)
   6. Fixes exception when attempting to delete a realization. Deletion
      of realizations is not supported.
   7. Fixed typo in the user guide

.. _known-issues-16:

Known Issues
^^^^^^^^^^^^

1. Using the AADL Property View to edit property values results in bad
   formatting.

Version 2.2.3
~~~~~~~~~~~~~

.. _release-22:

Release
^^^^^^^

-  **GIT tag**: 2.2.3-RELEASE-20170811
-  **Release date**: August 21, 2017
-  **Eclipse base version**: Mars.2
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.2.3/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.2.3/products

This is the last release based on Eclipse Mars.

.. _notable-changes-22:

Notable changes
^^^^^^^^^^^^^^^

1. New analysis checks if bindings (Actual_*_Binding) adhere to
   constraints (Allowed_*_Binding, Allowed_*_Binding_Class, Required
    Provided_Connection_Quality_of_Service, Required
    Provided_Virtual_Bus_Class)
   (`#775 <https://github.com/osate/osate2-core/issues/775>`__)
2. Significant improvements in the graphical editor. See below for
   details.
3. Added an AGREE simulator. A user guide is included in the help
   content.

.. _fixed-issues-22:

Fixed issues
^^^^^^^^^^^^

-  OSATE core

   1.  Resolve property constants in record fields
       (`#835 <https://github.com/osate/osate2-core/issues/835>`__)
   2.  Fixed bogus error when validating property consistency along
       connections during instantiation
       (`#819 <https://github.com/osate/osate2-core/issues/819>`__)
   3.  An empty annex library or subclause no longer causes an exception
       (`#816 <https://github.com/osate/osate2-core/issues/816>`__)
   4.  Fixed corner case in connection validation with inverse feature
       groups
       (`#815 <https://github.com/osate/osate2-core/issues/815>`__)
   5.  OSATE now contains a plugin that supports diagram export
       (`#707 <https://github.com/osate/osate2-core/issues/707>`__)
   6.  End to end flows can now be expanded to show the flow segments in
       the instance model editor
       (`#859 <https://github.com/osate/osate2-core/issues/859>`__)
   7.  Use short names for system operation modes
       (`#743 <https://github.com/osate/osate2-core/issues/743>`__)
   8.  System operation modes can now be expanded to show the
       participating modes in the instance model editor
       (`#867 <https://github.com/osate/osate2-core/issues/867>`__)
   9.  Instantiation now limits the number of system operation modes to
       1000 (`#666 <https://github.com/osate/osate2-core/issues/666>`__)
   10. Cleaned up labels in instance model editor
       (`#865 <https://github.com/osate/osate2-core/issues/865>`__)
   11. No duplicate value error for binding specifig property
       association
       (`#833 <https://github.com/osate/osate2-core/issues/833>`__)

-  Analysis Plugins

   1. Fixed wrong data in FHA reports
      (`#848 <https://github.com/osate/osate2-core/issues/848>`__)
   2. Flow latency analysis now uses fixed transmission overhead when a
      port is missing a data type
      (`#852 <https://github.com/osate/osate2-core/issues/852>`__)

-  Graphical Editor

   -  Diagrams

      -  The file format used by previous versions of the Graphical
         Editor has been deprecated. Support for opening such diagrams
         will be removed in a subsequent release. When opening a legacy
         diagram, the user will be prompted to convert the file. The new
         file format is more compact and contains more reliable linkages
         with the AADL model.
      -  It is recommended to convert all legacy diagrams to the new
         format by opening them.
      -  Diagrams no longer use UUIDs are part of file names. Legacy
         diagrams will be renamed as part of the conversion process.
      -  Added support for multiple diagrams representing the same model
         element.
      -  Added a “Configure Diagram…” option to the diagram’s context
         menu which is used for configuring which model elements are
         displayed in the diagram.
      -  Removed diagram-wide nesting level option. The nesting level of
         diagram elements can now be controlled individually.
      -  Added Show Contents, Hide Contents, and Show Type Contents to
         the diagram element context menu.
      -  Added an asterisk indicator after labels which indicates
         whether all of the contents for an element are shown.

   -  Refactoring

      -  Renaming elements from the diagram editor will refactor the
         AADL model.
      -  Renaming elements from the diagram editor will update related
         diagrams.
      -  References in legacy diagrams are not updated.
      -  Renaming a model elment using the “Rename Element” menu option
         updates linkages in diagrams.

   -  AADL Property Support

      -  Reworked AADL property support. Individual AADL properties can
         be enabled on a per-diagram basis using the “Configure
         Diagram…” context menu.
      -  AADL reference property values between descendants which are
         not shown are displayed as a binding between the closest
         ancestors which are included in the diagram.
      -  AADL reference property values for the same AADL property,
         source, and destination are grouped together into a single
         connection.
      -  Added tooltip for grouped AADL property reference values which
         contains details about the property values.
      -  Bindings along with other reference properties now support
         bendpoints.

   -  AADL Features

      -  Features may be docked to any side. Previously only the left
         and right were supported.
      -  Feature group types use the same symbol regardless of the type
         of diagram. Previously, feature group types used a rectangle on
         classifier diagrams.

         -  Feature groups can be resized.

   -  Formatting

      -  Labels of classifiers on package diagrams are now located at
         the top and centered.
      -  Added labels for classifiers in classifier diagrams.
      -  Elements are now colored differently to indicate that they are
         not owned by the container.
      -  Added toolbar commands for positioning shapes in a radial or
         grid pattern.

   -  Miscellaneous

      -  Changed behavior of unique identifier generation to include the
         containing classifier’s name. This is to avoid naming conflicts
         with classifiers that extend the classifier being edited.
      -  Relaxed validation in the flow implementation tool. It is
         intended that the validation will be improved in a future
         release. The tool should allow creation of all valid flow
         implementations but will also allow selection of invalid
         elements in some circumstances.
      -  Modified filtering when selecting model elements. Now matches
         any part of name.
      -  Fixed cases where setting a subcomponent classifier was not
         working properly.
      -  Added support for connections whose features are not included
         in the diagram. Such connections are formatted differently from
         normal connections.
      -  Added command to navigate to component type diagram for
         subcomponents.

-  Resolute/AGREE

   1. Various bug fixes

-  ALISA Incremental Assurance

   1. Minor bug fixes
      (`#17 <https://github.com/osate/osate2-core/issues/17>`__,
      `#23 <https://github.com/osate/osate2-core/issues/23>`__,
      `#24 <https://github.com/osate/osate2-core/issues/24>`__)

.. _known-issues-17:

Known Issues
^^^^^^^^^^^^

1. Using the AADL Property View to edit property values results in bad
   formatting
2. AADL 2.2 support: Partial end to end flows are not yet supported
3. ALISA still has error markers on some references even though they are
   correctly resolved

Version 2.2.2
~~~~~~~~~~~~~

.. _release-23:

Release
^^^^^^^

-  **GIT tag**: 2.2.2-RELEASE-20170515
-  **Release date**: May 15, 2017
-  **Eclipse base version**: Mars.2
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.2.2/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.2.2/products

This release adds support for features new in AADL 2.2.

Note that the underlying AADL meta-model has changed. This makes it
necessary to do a clean build of existing projects and to recreate all
instance models. Otherwise errors may occur when running analyses.

.. _notable-changes-23:

Notable changes
^^^^^^^^^^^^^^^

1. Allow connection ends that reach down into feature groups
   (`#500 <https://github.com/osate/osate2-core/issues/500>`__)
2. Removed ``Type_Extension`` from property ``Classifier_Matching_Rule``
   (`#740 <https://github.com/osate/osate2-core/issues/740>`__)
3. Support property types ``classifier`` and ``reference`` with empty
   list of classifiers
   (`#718 <https://github.com/osate/osate2-core/issues/718>`__)
4. Flow implementations may reference a feature in a feature group even
   if the flow specification references the geature group
   (`#794 <https://github.com/osate/osate2-core/issues/794>`__)
5. Added a checker that can be run before code generation
6. Added outline support to the graphical editor
7. Updated Xtext to version 2.11
   (`#697 <https://github.com/osate/osate2-core/issues/697>`__,
   `#800 <https://github.com/osate/osate2-core/issues/800>`__)
8. ReqSpec now allows requirement and val declarations to be
   interspersed (`#13 <https://github.com/osate/alisa/issues/13>`__)
9. Alisa now supports automated verification when verification plans are
   not complete, i.e., activities are missing for some requirements
   (`#14 <https://github.com/osate/alisa/issues/14>`__)

.. raw:: html

   <!---
   1. Added AADL and ALISA file types to Eclipse logical model
      - Dependent files are added to git commits
      - **NOTE** Comparing two AADL or ALISA text files starts the structural compare view. There textual comparison must be selected manually.
   -->

.. _fixed-issues-23:

Fixed issues
^^^^^^^^^^^^

-  OSATE core

   1.  Improved end to end flow validation
       (`#763 <https://github.com/osate/osate2-core/issues/763>`__)
   2.  Component instances reference their declarative classifier
       (`#746 <https://github.com/osate/osate2-core/issues/746>`__)
   3.  Correct serialization of flow implementations
       (`#750 <https://github.com/osate/osate2-core/issues/750>`__)
   4.  Fixes in connection instantiation
       (`#766 <https://github.com/osate/osate2-core/issues/766>`__,
       `#780 <https://github.com/osate/osate2-core/issues/780>`__)
   5.  Correct checking of property applicability
       (`#635 <https://github.com/osate/osate2-core/issues/635>`__)
   6.  Warn about empty flow implementations
       (`#781 <https://github.com/osate/osate2-core/issues/781>`__)
   7.  Fix in end to end flow instantiation
       (`#789 <https://github.com/osate/osate2-core/issues/789>`__)
   8.  Generate sensible names for end to end flow instances
       (`#742 <https://github.com/osate/osate2-core/issues/742>`__)
   9.  Correct validation of classifier substitution rule
       ``Classifier_Match``
       (`#795 <https://github.com/osate/osate2-core/issues/795>`__)
   10. Detect cycles in property references during instantiation
       (`#699 <https://github.com/osate/osate2-core/issues/699>`__)
   11. Detect cycles in feature group containment during instantiation
       (`#761 <https://github.com/osate/osate2-core/issues/761>`__)
   12. Added utility methods for internal features
       (`#683 <https://github.com/osate/osate2-core/issues/683>`__)
   13. OSATE warns about usage of aggregate data ports which are not
       handled in model instantiation
       (`#744 <https://github.com/osate/osate2-core/issues/744>`__)
   14. Fixed bugs related to inverses of feature groups
       (`#277 <https://github.com/osate/osate2-core/issues/277>`__,
       `#810 <https://github.com/osate/osate2-core/issues/810>`__,
       `#277 <https://github.com/osate/osate2-core/issues/277>`__)

-  Analysis Plugins

   1. Fixed flow latency calculation when end to end flow includes other
      end to end flows
      (`#792 <https://github.com/osate/osate2-core/issues/792>`__)
   2. Separate menu entries for ARP4761 and MIL-STD-882 FHA
      (`#827 <https://github.com/osate/osate2-core/issues/827>`__)
   3. Various bug fixes in FHA report
      (`#821 <https://github.com/osate/osate2-core/issues/821>`__,
      `#822 <https://github.com/osate/osate2-core/issues/822>`__,
      `#823 <https://github.com/osate/osate2-core/issues/823>`__,
      `#824 <https://github.com/osate/osate2-core/issues/824>`__,
      `#825 <https://github.com/osate/osate2-core/issues/825>`__,
      `#826 <https://github.com/osate/osate2-core/issues/826>`__)

-  Graphical Editor

   1. Subprogram calls now display the flow specifications of the
      contained subprogram type
      (`#186 <https://github.com/osate/osate-ge/issues/186>`__)
   2. Fixed an exception which occured when a Component Instance did not
      have a classifier
      (`#183 <https://github.com/osate/osate-ge/issues/183>`__)
   3. Allow bendpoints for generalizations
      (`#786 <https://github.com/osate/osate2-core/issues/786>`__)
   4. Fixed an exception which could occur when working with models
      which include annex subclauses

-  Resolute/AGREE

   1. This release contains numerous bug fixes for Resolute.
   2. It also includes the addition of “Real-time Patterns” and
      “Linearization” to AGREE. These new features are documented in the
      `User’s
      Guide <https://github.com/smaccm/smaccm/raw/master/documentation/agree/AGREE%20Users%20Guide.pdf>`__

-  ALISA Incremental Assurance

   1. Alisa Assurance View: Color bars replaced by colored count entries
      (`#21 <https://github.com/osate/osate2-core/issues/21>`__)
   2. Removed Assurance Progress View. Progress indication is already
      available in Assurance View
      (`#20 <https://github.com/osate/alisa/issues/20>`__)
   3. Assurance Requirement Coverage now has its own filter selection
      (`#22 <https://github.com/osate/alisa/issues/22>`__)
   4. Several bug fixes related to predicate evaluation and error marker
      on references that actually have been resolved

.. _known-issues-18:

Known Issues
^^^^^^^^^^^^

1. Using the AADL Property View to edit property values results in bad
   formatting
2. AADL 2.2 support: Partial end to end flows are not yet supported
3. ALISA still has error markers on some references even though they are
   correctly resolved

Version 2.2.1 update 03
~~~~~~~~~~~~~~~~~~~~~~~

.. _release-24:

Release
^^^^^^^

-  **GIT tag**: 2.2.1-UPDATE03
-  **Release date**: January 20, 2017
-  **Eclipse base version**: Mars.2
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.2.1/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.2.1/products

This is a maintenance release that contains bug fixes and improvements.

.. _notable-changes-24:

Notable changes
^^^^^^^^^^^^^^^

1. Allow ``Code_Size`` property on virtual bus components
2. Allow ``Data_Size`` property on bus and virtual bus components
3. Improvements to flow latency analysis

   -  Use ``Reference_Time`` property to determine synchronous
      vs. asynchronous
   -  Improved help text for flow latency analysis

4. Reworked ALISA views
5. Improved layout and generation of requirement traceability reports
6. Added simple requirements report
7. Added help text for reporting

.. _fixed-issues-24:

Fixed issues
^^^^^^^^^^^^

-  OSATE core

   1. Repaired ARP4761 example
      (`#738 <https://github.com/osate/osate2-core/issues/738>`__)
   2. Fixed regression in instantiation of feature group connections
      (`#752 <https://github.com/osate/osate2-core/issues/752>`__)
   3. Instantiate connections from input features to data subcomponents
      (`#753 <https://github.com/osate/osate2-core/issues/753>`__)
   4. Additional validation of feature directions for feature group
      connections

-  Analysis Plugins

   1. Fixes in flow latency analysis:

      -  Use deadline as default latency
         (`#62 <https://github.com/osate/osate2-plugins/issues/62>`__,
         `#63 <https://github.com/osate/osate2-plugins/issues/63>`__)
      -  Don’t skip components without flow path
         (`#60 <https://github.com/osate/osate2-plugins/issues/60>`__)

-  Graphical Editor

   1. Don’t assume that component instances have a classifier
      (`#183 <https://github.com/osate/osate-ge/issues/183>`__)
   2. Fix issue with disappearing connection references
      (`#181 <https://github.com/osate/osate-ge/issues/181>`__)
   3. Show flows from called subprogram types
      (`#186 <https://github.com/osate/osate-ge/issues/186>`__)

-  Error Model Annex

   1. Fixed error model name resolution to conform to standard
      (`#103 <https://github.com/osate/ErrorModelV2/issues/103>`__,
      `#114 <https://github.com/osate/ErrorModelV2/issues/114>`__)
   2. Additional validation rule
      (`#117 <https://github.com/osate/ErrorModelV2/issues/117>`__)
   3. Fixed containment check for type sets
      (`#118 <https://github.com/osate/ErrorModelV2/issues/118>`__,
      `#120 <https://github.com/osate/ErrorModelV2/issues/120>`__)
   4. Fixed name resolution issue for error types
      (`#119 <https://github.com/osate/ErrorModelV2/issues/119>`__)

.. _known-issues-19:

Known Issues
^^^^^^^^^^^^

1. Using the AADL Property View to edit property values results in bad
   formatting.

Version 2.2.1 update 02
~~~~~~~~~~~~~~~~~~~~~~~

.. _release-25:

Release
^^^^^^^

-  **GIT tag**: 2.2.1-UPDATE02
-  **Release date**: Oct 14, 2016
-  **Eclipse base version**: Mars.2
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.2.1/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.2.1/products

This is a maintenance release that contains bug fixes and improvements
to the ReqSpec language. It also includes a beta version the Verify and
Alisa languages for requirements verification.

.. _notable-changes-25:

Notable Changes
^^^^^^^^^^^^^^^

1. Added missing ``Array_Size_Range`` property type
2. Updated help text for flow latency analysis
3. Many small improvements to the graphical editor
4. Various improvements for fault tree generation

.. _fixed-issues-25:

Fixed Issues
^^^^^^^^^^^^

-  OSATE core and analyses

   1. Flow sink implementations are now property serialized (#617)
   2. Fixed a crash when creating an instance model that has errors
      (#712)
   3. Fixed a deadlock during instantiation (#726)
   4. Connections that go through a component (from in port directly to
      out port) are now flagged as errors (#727, #728)
   5. Validation of feature group connections now flags mismatched
      feature group types as an error (#709)
   6. Fixed validation to allow references to elements of
      multi-dimensional arrays in property values (#694)
   7. Fixed a bug that caused missing connections in instance model
      (#734)
   8. Instance model analyses now take selected system operation mode
      into account (#736)
   9. Fixed a deadlock during flow latency analysis (#737)

-  Graphical Editor

   1. Default port direction is set according to the side of the
      component (#150)
   2. Fixed bug that prevented adding subcomponent flow to end-to-end
      flow or flow implementation (#166)
   3. It is now possible to select a component when it is covered by
      labels (context menu: select container) (#171)
   4. Prevent negative y-coordinates for feature groups (#172)

-  Error Model Annex

   1. FHA report was missing hazards (#113)

.. _known-issues-20:

Known Issues
^^^^^^^^^^^^

1. Using the AADL Property View to edit property values results in bad
   formatting.

Version 2.2.1 update 01
~~~~~~~~~~~~~~~~~~~~~~~

.. _release-26:

Release
^^^^^^^

-  **GIT tag**: 2.2.1-UPDATE01
-  **Release date**: May 24, 2016
-  **Eclipse base version**: Mars.2
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.2.1/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.2.1/products

This is a maintenance release that contains bug fixes and improvements
to the ReqSpec language.

.. _notable-changes-26:

Notable Changes
^^^^^^^^^^^^^^^

1. Property ``Classifier_Matching_Rule => Subset`` is now supported for
   instantiation.
2. Creating a text file for an instance model works now.
3. Added documentation for using the AADL Property Values view under
   OSATE Core Documentation -> Getting started -> Viewing and editing
   property values.
4. Added a Usage Guide to the Resolute documentation.
5. Added more types and type checking to the ReqSpec language. The help
   text has been updated to reflect these changes.

.. _known-issues-21:

Known Issues
^^^^^^^^^^^^

1. Using the AADL Property View to edit property values results in bad
   formatting.

.. _fixed-issues-26:

Fixed Issues
^^^^^^^^^^^^

The full lists of closed issues for this release are available at

https://github.com/osate/osate2-core/issues?q=is%3Aissue+updated%3A2016-04-19..2016-05-22+is%3Aclosed

https://github.com/osate/osate2-plugins/issues?q=is%3Aissue+updated%3A2016-04-19..2016-05-22+is%3Aclosed

https://github.com/osate/ErrorModelV2/issues?q=is%3Aissue+updated%3A2016-04-19..2016-05-22+is%3Aclosed

Version 2.2.1
~~~~~~~~~~~~~

.. _release-27:

Release
^^^^^^^

-  **GIT tag**: 2.2.1-RELEASE-20160418
-  **Release date**: April 18, 2016
-  **Eclipse base version**: Mars.2
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.2.1/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.2.1/products

.. _notable-changes-27:

Notable Changes
^^^^^^^^^^^^^^^

1. We have included the EMFTA tool for fault tree analysis (see Help
   text). The existing export to OpenFTA has been removed
2. OSATE now includes requirements specification language (ReqSpec) from
   our ALISA project (see Help text)
3. Implemented approved language errata:

   1. Abstract features are allowed as mode transition triggers
   2. Added property Reference_Time

      3. Abstract features can reference classifiers in addition to
         prototypes:

         prototypes fp: feature; dt: data; features – feature is the
         prototype actual f1: prototype fp; – abstract feature
         referencing a data classifier f2: feature SomeDataType; –
         abstract feature referencing a data prototype f3: feature dt;

4. Added textual representation of instance models. Convert AADL
   instance model file to text via action “Generate Textual Instance” in
   AADL Navigator context menu
5. Added BIRT for report generation. An example report for requirements
   traceability is included: Action “Requirements Tracing” in context
   menu in the AADL Navigatior view, active for AADL packages, instance
   models, system requirements and system goals. The report sources are
   in plugin org.osate.reqtrace
6. Unnecessary plugins were removed to reduce download size
7. Updated Agree to version 2.1.3
8. The underlying Eclipse version has been updated to Mars.2

.. _known-issues-22:

Known Issues
^^^^^^^^^^^^

1. Using the AADL Property View to edit property values results in bad
   formatting

.. _fixed-issues-27:

Fixed Issues
^^^^^^^^^^^^

The full lists of closed issues for this release are available at

https://github.com/osate/osate2-core/issues?q=is%3Aissue+updated%3A2015-12-24..2016-04-18+is%3Aclosed

https://github.com/osate/osate2-plugins/issues?q=is%3Aissue+updated%3A2015-12-24..2016-04-18+is%3Aclosed

https://github.com/osate/osate-ge/issues?q=is%3Aissue+updated%3A2015-12-24..2016-04-18+is%3Aclosed

https://github.com/osate/ErrorModelV2/issues?q=is%3Aissue+updated%3A2015-12-24..2016-04-18+is%3Aclosed

Version 2.2.0
~~~~~~~~~~~~~

.. _release-28:

Release
^^^^^^^

-  **GIT tag**: 2.2.0-RELEASE-20151223
-  **Release date**: January 5, 2016
-  **Eclipse base version**: Mars.1
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.2.0/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.2.0/products

.. _notable-changes-28:

Notable changes
^^^^^^^^^^^^^^^

1. OSATE is now based on Eclipse Mars which requires a new full
   installation
2. Implemented approved errata for properties:

   1. Process_Swap_Execution_time now applies to virtual processor.
   2. Add processor, virtual processor in applies to of
      Activate_Entry_Point. They are included in the other entry_point
      properties.
   3. Code_Size, Heap_Size, Data_Size, and Stack_Size now apply to
      virtual processors.
   4. Mark Byte_Count as deprecated.
   5. Add Source_xx_Size back in and mark as deprecated. These are used
      in the standard, the book, and in the course. Backward
      compatibility.
   6. Memory_Binding properties now apply to system and processor. Also
      to virtual processor to model partitions with memory budgets.
   7. Property values are no longer allowed as array index value.

3. Performance improvements in graphical editor
4. Outline view can now handle annexes

.. _known-issues-23:

Known Issues
^^^^^^^^^^^^

1. Using the AADL Property View to edit property values results in bad
   formatting

.. _fixed-issues-28:

Fixed Issues
^^^^^^^^^^^^

The full lists of closed issues for this release are available at

https://github.com/osate/osate2-core/issues?q=is%3Aissue+updated%3A2015-09-05..2015-12-22+is%3Aclosed

https://github.com/osate/osate2-plugins/issues?q=is%3Aissue+updated%3A2015-09-05..2015-12-22+is%3Aclosed

https://github.com/osate/osate-ge/issues?q=is%3Aissue+updated%3A2015-09-05..2015-12-22+is%3Aclosed

https://github.com/osate/ErrorModelV2/issues?q=is%3Aissue+updated%3A2015-09-05..2015-12-22+is%3Aclosed

Version 2.1.2
~~~~~~~~~~~~~

.. _release-29:

Release
^^^^^^^

-  **GIT tag**: 2.1.2-RELEASE-20150904
-  **Release date**: September 14, 2015
-  **Eclipse base version**: Luna SR2
-  **Java version**: Java 8
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.1.2/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.1.2/products

Major changes
^^^^^^^^^^^^^

1. Flows can now be created in the graphical editor by clicking on
   components and connections
2. The AADL Properties view can be used with the instance model
3. The text editor automatically un-indents section keywords (features,
   subcomponents, etc.), see preference Window -> Preferences -> OSATE
   Preferences -> Aadl2 Text Editor to control this behavior

.. _known-issues-24:

Known Issues
^^^^^^^^^^^^

1. Using the AADL Property View to edit property values results in bad
   formatting

.. _fixed-issues-29:

Fixed Issues
^^^^^^^^^^^^

The full lists of closed issues for this release are available at

https://github.com/osate/osate2-core/issues?q=is%3Aissue+updated%3A2015-07-06..2015-09-04+is%3Aclosed

https://github.com/osate/osate2-plugins/issues?q=is%3Aissue+updated%3A2015-07-06..2015-09-04+is%3Aclosed

https://github.com/osate/osate-ge/issues?q=is%3Aissue+updated%3A2015-07-06..2015-09-04+is%3Aclosed

https://github.com/osate/ErrorModelV2/issues?q=is%3Aissue+updated%3A2015-07-06..2015-09-04+is%3Aclosed

Version 2.1.1
~~~~~~~~~~~~~

.. _release-30:

Release
^^^^^^^

-  **GIT tag**: 2.1.1-RELEASE-20150702
-  **Release date**: July 6, 2015
-  **Eclipse base version**: Luna SR2
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.1.1/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.1.1/products

.. _major-changes-1:

Major changes
^^^^^^^^^^^^^

1.  OSATE now requires Java 8
2.  Automatically add “end” when typing in the text editor, see
    preference Window -> Preferences -> OSATE Preferences -> Aadl2 Text
    Editor to control this behavior
3.  New text editor command to organize with clauses
4.  The Plugin_Resources project has subdirectories to organize property
    sets - existing workspaces should be updated automatically (If there
    is a problem, try to re-create the project using the context menu in
    the AADL Navigator: “Reset/create all Predeclared and Annex
    Properties”)
5.  The AADL Property View supports editing of property associations
    declared in the classifier’s properties section if the applies to
    contains a single name (“local contained”)
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

.. _known-issues-25:

Known Issues
^^^^^^^^^^^^

1. Using the AADL Property View to edit property values results in bad
   formatting

.. _fixed-issues-30:

Fixed Issues
^^^^^^^^^^^^

The full lists of closed issues for this release are available at

https://github.com/osate/osate2-core/issues?q=is%3Aissue+updated%3A2015-05-01..2015-07-05+is%3Aclosed

https://github.com/osate/osate2-plugins/issues?q=is%3Aissue+updated%3A2015-05-01..2015-07-05+is%3Aclosed

https://github.com/osate/osate-ge/issues?q=is%3Aissue+updated%3A2015-05-01..2015-07-05+is%3Aclosed

https://github.com/osate/ErrorModelV2/issues?q=is%3Aissue+updated%3A2015-05-01..2015-07-05+is%3Aclosed

Version 2.1.0
~~~~~~~~~~~~~

.. _release-31:

Release
^^^^^^^

-  **GIT tag**: 2.1.0-RELEASE-20150501
-  **Release date**: May 2, 2015
-  **Eclipse base version**: Luna SR2
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.1.0/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.1.0/products

.. _major-changes-2:

Major changes
^^^^^^^^^^^^^

1. Additional validations for textual AADL models
2. Added quick fixes in the AADL text editor
3. Added Resolute language reference
4. Performance improvements in the graphical editor
5. Flow latency analysis handles periodic buses
6. Various bug fixes related to connection and flow instantiation

.. _known-issues-26:

Known Issues
^^^^^^^^^^^^

1. Running Agree requires Java 8

.. _fixed-issues-31:

Fixed Issues
^^^^^^^^^^^^

The full lists of closed issues for this release are available at

https://github.com/osate/osate2-core/issues?q=is%3Aissue+updated%3A2015-02-26..2015-05-01+is%3Aclosed

https://github.com/osate/osate2-plugins/issues?q=is%3Aissue+updated%3A2015-02-26..2015-05-01+is%3Aclosed

https://github.com/osate/osate-ge/issues?q=is%3Aissue+updated%3A2015-02-26..2015-05-01+is%3Aclosed

https://github.com/osate/ErrorModelV2/issues?q=is%3Aissue+updated%3A2015-02-26..2015-05-01+is%3Aclosed

Version 2.0.9
~~~~~~~~~~~~~

.. _release-32:

Release
^^^^^^^

-  **GIT tag**: 2.0.9-RELEASE-20150301
-  **Release date**: March 2, 2015
-  **Eclipse base version**: Luna
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.0.9/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.0.9/products

.. _major-changes-3:

Major changes
^^^^^^^^^^^^^

1. The AADL Property View has been rewritten to support expansion of
   list and record values. In addition, property values can be edited
   directly in the view.
2. Instance models can be created from any component **Note:** The
   SystemInstance object now references a ComponentImplementation
   instead of a SystemImplementation. Plugins may need to be adapted.
3. We have integrated the Resolute and Agree plugins created at Rockwell
   Collins (see https://github.com/smaccm/smaccm). **Note:** Agree
   depends on an program (JKind 2.1) which requires Java 8 to run.
4. We have integrated the Ocarina plugin for OSATE 2 (see
   https://github.com/OpenAADL/osate2-ocarina).

.. _known-issues-27:

Known Issues
^^^^^^^^^^^^

.. _fixed-issues-32:

Fixed Issues
^^^^^^^^^^^^

The full list of closed issues for this release are available at

https://github.com/osate/osate2-core/issues?q=is%3Aissue+updated%3A2014-10-01..2015-02-25+is%3Aclosed

https://github.com/osate/osate2-plugins/issues?q=is%3Aissue+updated%3A2014-10-01..2015-02-25+is%3Aclosed

https://github.com/osate/osate-ge/issues?q=is%3Aissue+updated%3A2014-10-01..2015-02-25+is%3Aclosed

https://github.com/osate/ErrorModelV2/issues?q=is%3Aissue+updated%3A2014-10-01..2015-02-25+is%3Aclosed

Version 2.0.8
~~~~~~~~~~~~~

A special page is dedicated to the `release notes of OSATE2
2.0.8 <release_notes_of_OSATE2_2.0.8>`__

.. _release-33:

Release
^^^^^^^

-  **GIT tag**: 2.0.8-RELEASE
-  **Release date**: September, 5 2014
-  **Eclipse base version**: Luna
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.0.8/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.0.8/products

.. _major-changes-4:

Major changes
^^^^^^^^^^^^^

1. Switched to Eclipse Luna
2. Refactored many analysis plugins
3. Excel report for latency analysis
4. Examples built-in in OSATE

.. _known-issues-28:

Known Issues
^^^^^^^^^^^^

1. After the first start with a new workspace the project
   **Plugin_Resources** may shown three times in the AADL navigator.
   Restarting OSATE fixes the issue.

Version 2.0.7
~~~~~~~~~~~~~

This release was published after the 2014 July AADL meeting hold in
Orlando, Florida, USA.

.. _release-34:

Release
^^^^^^^

-  **GIT tag**: 2.0.7-RELEASE
-  **Release date**: July, 14 2014
-  **Eclipse base version**: Kepler
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.0.7/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.0.7/products

.. _major-changes-5:

Major changes
^^^^^^^^^^^^^

1. Automatically compute reliability values from sub-components in the
   Reliability Block Diagram plugin
2. Graphical tool now works with Java 6
3. Update of EMV2 annex, compliant with the document under ballot
4. Update of ARINC653 properties, compliant with the version being under
   ballot for the coming September meeting.

Version 2.0.6
~~~~~~~~~~~~~

This release was published after the 2014 April AADL meeting hold in
Santa Barbara, USA.

.. _release-35:

Release
^^^^^^^

-  **GIT tag**: 2.0.6-RELEASE
-  **Release date**: Apr, 28 2014
-  **Eclipse base version**: Kepler
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.0.6/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.0.6/products

.. _known-issues-29:

Known issues
^^^^^^^^^^^^

1. Using the update site, under Windows7 you may have a file protection
   issue for your installation. Eclipse update is just silently failing
   to update rather than reporting “permission denied.” Please check the
   date of the installed OSATE feature (Open Source AADL Tool
   Environment) under Help->About and then Installation Details. If it
   did not get updated to the most recent date, please change your
   permissions.
2. Using the update site, when you are in OSATE (Eclipse) and just
   checked an update site for updates, Eclipse caches that information.
   If someone tells you about a new release on the update site, please
   exit and reenter OSATE so it will actually find the new release.

.. _major-changes-6:

Major changes
^^^^^^^^^^^^^

1. Integration of the Graphical Editor
2. New safety analysis tools

Version 2.0.5
~~~~~~~~~~~~~

This release was published after the 2014 February AADL meeting hold in
Toulouse, France.

.. _release-36:

Release
^^^^^^^

-  **GIT tag**: 2.0.5-RELEASE-201402040847
-  **Release date**: February 4, 2014.
-  **Eclipse base version**: Kepler
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.0.5/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.0.5/products

.. _known-issues-30:

Known issues
^^^^^^^^^^^^

1. Using the update site, under Windows7 you may have a file protection
   issue for your installation. Eclipse update is just silently failing
   to update rather than reporting “permission denied.” Please check the
   date of the installed OSATE feature (Open Source AADL Tool
   Environment) under Help->About and then Installation Details. If it
   did not get updated to the most recent date, please change your
   permissions.
2. Using the update site, when you are in OSATE (Eclipse) and just
   checked an update site for updates, Eclipse caches that information.
   If someone tells you about a new release on the update site, please
   exit and reenter OSATE so it will actually find the new release.

Changes and new features
^^^^^^^^^^^^^^^^^^^^^^^^

1.  ResolvePrototypeUtil - FeatureGroupPrototypeActual support -
    https://github.com/osate/osate2-core/issues/285
2.  Constant property declaration using user-defined property set is not
    working - https://github.com/osate/osate2-core/issues/286
3.  Data_Volume property not defined in AADL_Project.aadl -
    https://github.com/osate/osate2-core/issues/287
4.  standard properties are no longer parsed -
    https://github.com/osate/osate2-core/issues/302
5.  Instantiated subcomponent has a component type only" error message -
    https://github.com/osate/osate2-core/issues/301
6.  Concrete Syntax Validation Error -
    https://github.com/osate/osate2-core/issues/299
7.  Connections are not required to have names -
    https://github.com/osate/osate2-core/issues/298
8.  getLocationReference() always returns null -
    https://github.com/osate/osate2-core/issues/295
9.  newFormal must be an instance of ComponentPrototype -
    https://github.com/osate/osate2-core/issues/293
10. Connection Refinement Issue -
    https://github.com/osate/osate2-core/issues/291
11. EMV2.aadl being included with OSATE -
    https://github.com/osate/osate2-core/issues/290
12. Mode Transition Trigger Port Reference Issue -
    https://github.com/osate/osate2-core/issues/289
13. Cannot resolve units type in constant declaration -
    https://github.com/osate/osate2-core/issues/288
14. Connection id is now mandatory -
    https://github.com/osate/osate2-core/issues/304
15. add nullity test to “upfgt” in Aadl2InstanceUtil.isSame -
    https://github.com/osate/osate2-core/issues/305
16. Issue with Xtext Grammar/Meta Model -
    https://github.com/osate/osate2-core/issues/306
17. System subcomponents become Abstract when instantiated -
    https://github.com/osate/osate2-core/issues/307
18. Typo in Metamodel - https://github.com/osate/osate2-core/issues/308
19. Hybrid and Timed literals do not exist in AadlProject -
    https://github.com/osate/osate2-core/issues/309
20. OSATE allows subprograms to provide data access -
    https://github.com/osate/osate2-core/issues/310
21. getSubcomponentType does not invoke eIsProxy if subcomponentType is
    null… - https://github.com/osate/osate2-core/issues/311
22. Question on connecting ‘out data port’ to ‘requires data access’ -
    https://github.com/osate/osate2-core/issues/312
23. Extra natures added to the Plugin_Resources project are always
    removed at startup. -
    https://github.com/osate/osate2-core/issues/319
24. The name of a subcomponent should be set to null whenever its
    refined subcomponent is set to a non null value. -
    https://github.com/osate/osate2-core/issues/320
25. AADL package section elements have a null qualified name. -
    https://github.com/osate/osate2-core/issues/321
26. AADL navigator content provider throws null pointer exception for
    the Plugin_Resources project. -
    https://github.com/osate/osate2-core/issues/322
27. AnnexParserAgent.java -
    https://github.com/osate/osate2-core/pull/284
28. Error when defining bus binding -
    https://github.com/osate/ErrorModelV2/issues/39
29. FHA cannot be generated when using error type -
    https://github.com/osate/ErrorModelV2/issues/38

Version 2.0.4
~~~~~~~~~~~~~

This release was published after the 2013 Fall AADL meeting hold in
Montreal, Canada.

.. _release-37:

Release
^^^^^^^

-  **GIT tag**: 2.0.4-RELEASE-201309240847
-  **Release date**: September, 24 2013
-  **Eclipse base version**: Kepler
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.0.4/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.0.4/products

.. _known-issues-31:

Known issues
^^^^^^^^^^^^

1. Using the update site, under Windows7 you may have a file protection
   issue for your installation. Eclipse update is just silently failing
   to update rather than reporting “permission denied.” Please check the
   date of the installed OSATE feature (Open Source AADL Tool
   Environment) under Help->About and then Installation Details. If it
   did not get updated to the most recent date, please change your
   permissions.
2. Using the update site, when you are in OSATE (Eclipse) and just
   checked an update site for updates, Eclipse caches that information.
   If someone tells you about a new release on the update site, please
   exit and reenter OSATE so it will actually find the new release.
3. If you updated an old Juno installation, you should also add the
   Kepler update site so that the Kepler dependencies can be updated as
   well.

.. _changes-and-new-features-1:

Changes and new features
^^^^^^^^^^^^^^^^^^^^^^^^

-  EMV2.aadl being included with OSATE -
   https://github.com/osate/osate2-core/issues/290
-  Cannot resolve units type in constant declaration -
   https://github.com/osate/osate2-core/issues/288
-  Data_Volume property not defined in AADL_Project.aadl -
   https://github.com/osate/osate2-core/issues/287
-  Constant property declaration using user-defined property set is not
   working - https://github.com/osate/osate2-core/issues/286
-  ResolvePrototypeUtil - FeatureGroupPrototypeActual support -
   https://github.com/osate/osate2-core/issues/285
-  ResolvePrototypeUtil.resolveFeaturePrototype always returns null -
   https://github.com/osate/osate2-core/issues/281
-  Adding a property fails -
   https://github.com/osate/osate2-core/issues/279
-  property edition: unit are not recognized -
   https://github.com/osate/osate2-core/issues/278
-  Feature Group Connections. Invalid inverse connection is allowed. -
   https://github.com/osate/osate2-core/issues/276
-  NullPointerException at
   org.osate.aadl2.properties.PropertyAcc.addLocalContained(PropertyAcc.java:107)

   -  https://github.com/osate/osate2-core/issues/275

-  GetProperties::getDelayedUnitLiteral always returns null. -
   https://github.com/osate/osate2-core/issues/273
-  org.eclipse.sphinx.emf needed and not found -
   https://github.com/osate/osate2-core/issues/271
-  Unable to Instantiate System/Qualified names are not unique -
   https://github.com/osate/osate2-core/issues/270
-  Defining a property delete other components -
   https://github.com/osate/osate2-core/issues/268
-  Refreshing property values -
   https://github.com/osate/osate2-core/issues/267
-  Adding a property on a component fails and triggers an exception -
   https://github.com/osate/osate2-core/issues/266
-  Most-Recent Develop Build Omits Plug-In Launch(es) -
   https://github.com/osate/osate2-core/issues/265
-  Instantiation Warning Not Helpful: Instantiated subcomponent has a
   component type only - https://github.com/osate/osate2-core/issues/264
-  Update to Kepler - https://github.com/osate/osate2-core/issues/263
-  Properties already defined are not shown -
   https://github.com/osate/osate2-core/issues/261
-  Cannot add a property value -
   https://github.com/osate/osate2-core/issues/260
-  error when building osate -
   https://github.com/osate/osate2-core/issues/258
-  Instance Model Viewer: Keep User Position Changes When Inserting
   Subcomponents - https://github.com/osate/osate2-core/issues/257
-  Types that are allows in global index are too restrictive. -
   https://github.com/osate/osate2-core/issues/256
-  AADL Properties View Issues -
   https://github.com/osate/osate2-core/issues/254
-  Setting the type of component implementations and the extended
   component for types and implementations throws unsupported operation
   exception. - https://github.com/osate/osate2-core/issues/253
-  Checking properties for connection instances -
   https://github.com/osate/osate2-core/issues/252
-  FHA cannot be generated when using error type -
   https://github.com/osate/ErrorModelV2/issues/38
-  add severity and likelhood in the hazard record -
   https://github.com/osate/ErrorModelV2/issues/36
-  Fail to parse the annex content when not using types -
   https://github.com/osate/ErrorModelV2/issues/26
-  Cannot specify the type associated to a state in the composite model

   -  https://github.com/osate/ErrorModelV2/issues/27

-  Property not being inherited -
   https://github.com/osate/ErrorModelV2/issues/34
-  Properties for refined components -
   https://github.com/osate/ErrorModelV2/issues/35

Version 2.0.3
~~~~~~~~~~~~~

This release was published after the 2013 Summer AADL meeting hold in
Pittsburgh, USA.

.. _release-38:

Release
^^^^^^^

-  **GIT tag**: 2.0.3-RELEASE-201307220847
-  **Release date**: July, 22 2013
-  **Eclipse base version**: Juno - 4.2
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.0.3/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.0.3/products
-  **Number of commits since the last stable**: 383

.. _known-issues-32:

Known issues
^^^^^^^^^^^^

1. Using the update site, under Windows7 you may have a file protection
   issue for your installation. Eclipse update is just silently failing
   to update rather than reporting “permission denied.” Please check the
   date of the installed OSATE feature (Open Source AADL Tool
   Environment) under Help->About and then Installation Details. If it
   did not get updated to the most recent date, please change your
   permissions.
2. Using the update site, when you are in OSATE (Eclipse) and just
   checked an update site for updates, Eclipse caches that information.
   If someone tells you about a new release on the update site, please
   exit and reenter OSATE so it will actually find the new release.

.. _changes-and-new-features-2:

Changes and new features
^^^^^^^^^^^^^^^^^^^^^^^^

-  PRISM export now supports error propagation
-  Updated Error Model Support
-  Property editor updated and refined
-  Integration of Sphinx, contribution from Geensyde

Issues closed
^^^^^^^^^^^^^

-  Connection instances not created for feature group connection -
   https://github.com/osate/osate2-core/issues/228
-  annex subclauses are not parsed in feature group type -
   https://github.com/osate/osate2-core/issues/227
-  Subprogram Problem - https://github.com/osate/osate2-core/issues/226
-  Error when connecting array of subcomponents -
   https://github.com/osate/osate2-core/issues/225
-  Connection instances not created for feature group connection -
   https://github.com/osate/osate2-core/issues/228
-  ModelLoadingAdapter returns null instead of a model -
   https://github.com/osate/osate2-core/issues/229
-  Update ModelLoadingAdapter.java -
   https://github.com/osate/osate2-core/issues/230
-  property parsing error -
   https://github.com/osate/osate2-core/issues/231
-  ConnectionReferences in ConnectionInstance is incorrect for arrays -
   https://github.com/osate/osate2-core/issues/232
-  Properties Viewer throws null pointer exception -
   https://github.com/osate/osate2-core/issues/233
-  when feature group is defined via prototype the connection instances
   connect as if all_to_all -
   https://github.com/osate/osate2-core/issues/235
-  AnalysisModel does not take bindings information into account -
   https://github.com/osate/osate2-core/issues/238
-  Add Preference to turn off \*all\* Xtext background operations until
   file save - https://github.com/osate/osate2-core/issues/239
-  Call to getType on AbstractImplementation classifier causes a stack
   trace overflow. - https://github.com/osate/osate2-core/issues/240
-  Error when defining a property that applies to package -
   https://github.com/osate/osate2-core/issues/241
-  Request - API to retrieve NamedElement by qualified name -
   https://github.com/osate/osate2-core/issues/242
-  index order in Connection_Set issue -
   https://github.com/osate/osate2-core/issues/243
-  Calling methods EMFIndexRetrieval too early can cause exception. -
   https://github.com/osate/osate2-core/issues/244
-  ConnectionReference holds incorrect values when arrays are involved

   -  https://github.com/osate/osate2-core/issues/245

-  References to AADL model elements from models of other meta-models
   are shifted when elements are deleted / added in the AADL declarative
   model. - https://github.com/osate/osate2-core/issues/247
-  Class cast exception thrown when resolving some derived references of
   the meta-model. - https://github.com/osate/osate2-core/issues/248
-  Setting the name of a package section throws an unsuported operation
   exception and causes problems for model merge.. -
   https://github.com/osate/osate2-core/issues/249
-  EcoreUtil.equals does not work on Generalizations -
   https://github.com/osate/osate2-core/issues/250
-  connection between data and a subcomponent inside an other data -
   https://github.com/osate/osate2-core/issues/251
-  Instance Model Viewer: Keep User Position Changes When Inserting
   Subcomponents - https://github.com/osate/osate2-core/issues/257
-  bindings information in AnalysisModel -
   https://github.com/osate/ErrorModelV2/issues/22
-  Check of duplicate flow identifiers -
   https://github.com/osate/ErrorModelV2/issues/23
-  EM2TypeSetUtil.contains improvement -
   https://github.com/osate/ErrorModelV2/issues/24
-  Fail to parse the annex content when not using types -
   https://github.com/osate/ErrorModelV2/issues/26
-  Cannot specify the type associated to a state in the composite model

   -  https://github.com/osate/ErrorModelV2/issues/27

Version 2.0.2
~~~~~~~~~~~~~

This release is published after the 2013 Spring AADL meeting hold in
Jacksonville, USA. Please note that this release changed also the
structure of our download area. The testing update site is now available
on http://www.aadl.info/aadl/osate/testing/

.. _release-39:

Release
^^^^^^^

-  **GIT tag**: 2.0.2-RELEASE-201304300847
-  **Release date**: April, 30 1013
-  **Eclipse base version**: Juno version **4.2.2**
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.0.2/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.0.2/products
-  Number of commits since the last stable: 283 (194 on the core) and 89
   on the plugins.

.. _known-issues-33:

Known issues
^^^^^^^^^^^^

1. Using the update site, under Windows7 you may have a file protection
   issue for your installation. Eclipse update is just silently failing
   to update rather than reporting “permission denied.” Please check the
   date of the installed OSATE feature (Open Source AADL Tool
   Environment) under Help->About and then Installation Details. If it
   did not get updated to the most recent date, please change your
   permissions.
2. Using the update site, when you are in OSATE (Eclipse) and just
   checked an update site for updates, Eclipse caches that information.
   If someone tells you about a new release on the update site, please
   exit and reenter OSATE so it will actually find the new release.

.. _changes-and-new-features-3:

Changes and new features
^^^^^^^^^^^^^^^^^^^^^^^^

-  Integration of the Property View
-  Integration of the IMV viewer with error-model annex
-  Add the Markov-Chain export for the Error-Model
-  Add the Reliability Block Diagram analysis tool for the Error-Model
-  Add the Fault-Tree Analysis tool for the Error-Model
-  Improvements of the Fault Hazard Assessment
-  Clean up the AADL perspective, analysis function being available only
   when using AADL view

.. _issues-closed-1:

Issues closed
^^^^^^^^^^^^^

1.  Using Xtext to create annex-
    https://github.com/osate/osate2-core/issues/224
2.  Instanciation exception when using connection datasubcomponent ->
    call.dataaccess - https://github.com/osate/osate2-core/issues/222
3.  inconsistent kind between flow spec and implementation not detected

    -  https://github.com/osate/osate2-core/issues/221

4.  Instanciation exception when using connection datasubcomponent ->
    call.parameter - https://github.com/osate/osate2-core/issues/220
5.  ConnectionKind in AADL2 Meta model -
    https://github.com/osate/osate2-core/issues/215
6.  mode specific property values in instance model -
    https://github.com/osate/osate2-core/issues/214
7.  AADL BA wizard examples -
    https://github.com/osate/osate2-core/issues/212
8.  conflicting handlers when invoking Content Assist -
    https://github.com/osate/osate2-core/issues/211
9.  clock_period and clock_period_range should apply to device -
    https://github.com/osate/osate2-core/issues/210
10. Instence creation with prototype binding does not work -
    https://github.com/osate/osate2-core/issues/209
11. flow latency calculation not correct for components without flow
    spec - https://github.com/osate/osate2-core/issues/207
12. flow implementation without connections accepted without warning or
    error - https://github.com/osate/osate2-core/issues/206
13. property association not created in instance model -
    https://github.com/osate/osate2-core/issues/205
14. Missing connection instances -
    https://github.com/osate/osate2-core/issues/204
15. User Interface Improvements -
    https://github.com/osate/osate2-core/issues/203
16. ProeprtyView icon not found -
    https://github.com/osate/osate2-core/issues/202
17. Resolution of Device_Driver property -
    https://github.com/osate/osate2-core/issues/200
18. patch proposal - https://github.com/osate/osate2-core/issues/199
19. Features direction for subprogram ports and thread ports -
    https://github.com/osate/osate2-core/issues/198
20. (Modified) Plugin_Resources not updated upon ‘Create/update
    Predeclared and Annex Properties’’ -
    https://github.com/osate/osate2-core/issues/197
21. flow path reports incrrectly that the port direction is wrong -
    https://github.com/osate/osate2-core/issues/196
22. The AADL meta-models are not declared in the EMF package registry
    for the development time version. -
    https://github.com/osate/osate2-core/issues/195
23. Last Connection Reference of a Connection Instance generated from a
    bidirectional feature group bug -
    https://github.com/osate/osate2-core/issues/194
24. Aadl Property Viewer does not show values on virtual processor in
    instance model - https://github.com/osate/osate2-core/issues/193
25. Some new operations in the meta-model are not implemented in the
    Java classes. - https://github.com/osate/osate2-core/issues/192
26. null pointer error on OSATE startup when AADL Properties view is
    open - https://github.com/osate/osate2-core/issues/191
27. requires subprogram access causes parsing error -
    https://github.com/osate/osate2-core/issues/189
28. osate2-core now has dependency to ErrorModelV2 -
    https://github.com/osate/osate2-core/issues/188
29. Problems with classifier matching rules on refined subcomponents. -
    https://github.com/osate/osate2-core/issues/182
30. for bidirectional feature group connections false warning about no
    ingoing connection - https://github.com/osate/osate2-core/issues/184
31. Can wrap illegal features inside legal feature groups -
    https://github.com/osate/osate2-core/issues/185
32. class cast exception in validator -
    https://github.com/osate/osate2-core/issues/186
33. FlowSpecificationInstance no longer has Source and Destination
    assigned - https://github.com/osate/osate2-core/issues/187

Version 2.0.1
~~~~~~~~~~~~~

This release is published after the Winter AADL meeting hold on
Valencia, Spain. We thank again our host for hosting this event.

.. _release-40:

Release
^^^^^^^

-  **GIT tag**: 2.0.1-RELEASE-201302141024
-  **Release date**: 2013, Feb 14
-  **Eclipse base version**: Juno version **4.2.1**
-  **Eclipse Update-Site**:
   http://www.aadl.info/aadl/osate/stable/2.0.1/update-site
-  **Download URL**:
   http://www.aadl.info/aadl/osate/stable/2.0.1/products

.. _known-issues-34:

Known issues
^^^^^^^^^^^^

1. Using the update site, under Windows7 you may have a file protection
   issue for your installation. Eclipse update is just silently failing
   to update rather than reporting “permission denied.” Please check the
   date of the installed OSATE feature (Open Source AADL Tool
   Environment) under Help->About and then Installation Details. If it
   did not get updated to the most recent date, please change your
   permissions.
2. Using the update site, when you are in OSATE (Eclipse) and just
   checked an update site for updates, Eclipse caches that information.
   If someone tells you about a new release on the update site, please
   exit and reenter OSATE so it will actually find the new release.

.. _changes-and-new-features-4:

Changes and new features
^^^^^^^^^^^^^^^^^^^^^^^^

-  LUTE integration in AADL plug-ins
-  Instance Model Viewer Integration
-  Error Model Annex v1
-  Error Model Annex v2
-  Integration of Ocarina specific property sets
-  Migration to Eclipse/Juno
-  ARINC653 validation functions
-  Support for ARINC653 annex
-  Update of help content within Eclipse (with Java API, plugins
   description, etc.)
-  User feedback when model instantiation fails
-  System Instance can be validated using EMF
-  Property viewer integration
-  Reference Manual integration

Bugfixes
''''''''

1.  Subprogram implementations in call sequences
    (https://github.com/osate/osate2-core/issues/181)
2.  Flows through feature groups (cf.
    https://github.com/osate/osate2-core/issues/179)
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
13. AADL connection instance property. “applies to” does not work.
    (https://github.com/osate/osate2-core/issues/174)
14. DATA_VOLUME_UNITS is now defined in AADL_Project
15. AADL_Project.java file need update for Data_Volume_Units
    (https://github.com/osate/osate2-core/issues/173)
16. Invalid ConnectionInstance property value
    (https://github.com/osate/osate2-core/issues/171)
17. Property Association Missing in instantiation -
    https://github.com/osate/osate2-core/issues/168
18. Access features are missing the super class of the specific category
    in the Meta model - https://github.com/osate/osate2-core/issues/167
19. Instantiation error (regression); trace suggests it comes from the
    process component - https://github.com/osate/osate2-core/issues/172
20. Naming resolution error: subprogram call context not found -
    https://github.com/osate/osate2-core/issues/170
21. Incorrect error reporting: “Value for property.. is inconsistent
    along connection” - https://github.com/osate/osate2-core/issues/158
22. Menu item failures from 2013-01-30 Development Branch. -
    https://github.com/osate/osate2-core/issues/165
23. Support of Juno - https://github.com/osate/osate2-core/issues/139
24. Cyclic reference error when typing in an alias (renames) -
    https://github.com/osate/osate2-core/issues/163
25. Exception when Instantiating System with Warning -
    https://github.com/osate/osate2-core/issues/162
26. Type mis-match warning on correct connection -
    https://github.com/osate/osate2-core/issues/155
27. Error when instantiating the model -
    https://github.com/osate/osate2-core/issues/156
28. Incorrect message for feature direction in flow implementation -
    https://github.com/osate/osate2-core/issues/161
29. Incorrect error message on flow between elements of feature groups -
    https://github.com/osate/osate2-core/issues/160
30. Error in org.osate.imv.propertydecorations.threads -
    https://github.com/osate/osate2-core/issues/159
31. Support for subprogram implementation -
    https://github.com/osate/osate2-core/issues/153
32. Visibility differs in subcomponent declaration versus properties
    section - https://github.com/osate/osate2-core/issues/152
33. Illegal refinement of category type allowed -
    https://github.com/osate/osate2-core/issues/150
34. Instance model error -
    https://github.com/osate/osate2-core/issues/151
35. Package visible without being withed -
    https://github.com/osate/osate2-core/issues/149
36. Property association classifier type -
    https://github.com/osate/osate2-core/issues/148
37. setPropertyValue method in NamedElementImpl -
    https://github.com/osate/osate2-core/issues/59
38. Formatting (via I or format command seems to loose the text in
    annexes. - https://github.com/osate/osate2-core/issues/145
39. Subset matching for feature group is not supported yet -
    https://github.com/osate/osate2-core/issues/107
40. renames causes cyclic lazy resolution -
    https://github.com/osate/osate2-core/issues/143
41. Checking type of reference value and classifier value -
    https://github.com/osate/osate2-core/issues/68
42. Property constant as value in range -
    https://github.com/osate/osate2-core/issues/129
43. Bus classifier not recognized in bus access connection for refined
    features. - https://github.com/osate/osate2-core/issues/121
44. Local path in target definition -
    https://github.com/osate/osate2-core/issues/7
45. Instance model corrupted when error occurs -
    https://github.com/osate/osate2-core/issues/135
46. Verification of duplicate elements -
    https://github.com/osate/osate2-core/issues/141
47. Instanciation error with Compute_Execution_Time property -
    https://github.com/osate/osate2-core/issues/140
48. Check for duplicate packages too restrictive -
    https://github.com/osate/osate2-core/issues/91
49. Default port “Complete” is not working -
    https://github.com/osate/osate2-core/issues/114
50. Property association omitted at instantiation of virtual processors

    -  https://github.com/osate/osate2-core/issues/126

51. Inconsistent literals for properties -
    https://github.com/osate/osate2-core/issues/45
52. Property sets for AADL annexes -
    https://github.com/osate/osate2-core/issues/64
53. Subprogam call name resolution -
    https://github.com/osate/osate2-core/issues/127
54. Record values surrounded with () vs. [] is inconsistent -
    https://github.com/osate/osate2-core/issues/137
55. Non-existent qualified name for a property -
    https://github.com/osate/osate2-core/issues/138
56. Enumeration literal not recognized -
    https://github.com/osate/osate2-core/issues/133
57. EValidator error when property constant is used as value -
    https://github.com/osate/osate2-core/issues/134
58. Incorrect error msg: “Connection between two components that inherit
    features is not supported” -
    https://github.com/osate/osate2-core/issues/136
59. Error with OSATE views -
    https://github.com/osate/osate2-core/issues/128
60. Bug with creating the connection instance with abstract component -
    https://github.com/osate/osate2-core/issues/118
61. About dialog is outdated -
    https://github.com/osate/osate2-core/issues/123
62. Method “acceptsProperty” in ComponentInstanceImpl always return true
    whatever the property is. -
    https://github.com/osate/osate2-core/issues/122
63. Property applicability clause to classifiers not recognized. -
    https://github.com/osate/osate2-core/issues/120
64. Discrepancy between ModeTransition ecore class and Java class -
    https://github.com/osate/osate2-core/issues/124
65. OsateResourceUtil bug? -
    https://github.com/osate/osate2-core/issues/42
66. Propertyset projects have been replaced by properties projects, this
    has… - https://github.com/osate/osate2-core/pull/125
67. Exception at ConnectionInstanceImpl.java (Line 843) -
    https://github.com/osate/osate2-core/issues/112
68. null pointer exception on hashcode of PropertyImpl -
    https://github.com/osate/osate2-core/issues/130
69. Duplicate Element ‘mils_example’ in PublicPackageSection
    ‘Test_Package’ example.aadl -
    https://github.com/osate/osate2-core/issues/132
70. Handling of instantiating a System when the model has errors. -
    https://github.com/osate/osate2-core/issues/77
71. Array size via property value -
    https://github.com/osate/osate2-core/issues/89
72. Workspace synchronization when instanciate several systems -
    https://github.com/osate/osate2-core/issues/119
73. Meta model support for contaiment path in core AADL with annex
    specific segments - https://github.com/osate/osate2-core/issues/146

This page uses the `Cayman
theme <https://github.com/jasonlong/cayman-theme>`__ by `Jason
Long <https://twitter.com/jasonlong>`__.
