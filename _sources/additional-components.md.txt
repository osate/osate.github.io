# Additional OSATE Components

The following additional OSATE components are not port of the base installation. They can be installed 
into OSATE via the dialog `Help` -> `Install Additional OSATE Components...`. For detailed instructions
click [here](http://osate.org/download-and-install.html#installing-additional-osate-components).

## OSATE Components by the Software Engineering Institute

### FACE Data Model to AADL Translator

The FACE Data Model to AADL Translator converts a FACE 3.0 “.face” file into an AADL 2.2 model. It
translates the Data Model, UoP Model, and Integration Model. The translator produces data classifiers
for the Data Model, thread groups for the UoP Model, and a system component for the Integration Model.
The system contains subcomponents for the UoPs and Transport Nodes and connections between these
subcomponents.

The purpose of the translator is to enable developers of FACE components to use the analytical
capabilities of AADL. The architectural information included in the FACE model is captured and expressed
in the resulting AADL model. This model can then be extended by the user to add various properties and
then analyzed. The existence of the FACE Data Model to AADL Translator allows for changes in the FACE
model to be quickly realized in the AADL model and then analyzed.

The FACE Data Model to AADL Translator is a set of plugins to OSATE. The translator integrates with the
OSATE modeling environment and is invoked from within OSATE.

## OSATE Components by Third Parties

### BLESS Plugin

The Behavior Language for Embedded Systems with Software (BLESS) is an annex sublanguage of AADL to 
express behavior of components with state-transition machines.

The plugin is provided by Multitude Corporation. See [their web site](http://www.multitude.net) 
for more information.

### Cheddar Plugin

Cheddar is a real-time scheduling analysis tool composed of a scheduling simulator and a set of 
schedulability tests. The plugin allows to generate Cheddar models to verify schedulability of 
uniprocessor and multiprocessor real-time systems.

The plugin is provided by the Universit&#xe9; de Bretagne Occidentale. See 
[their web site](http://beru.univ-brest.fr/cheddar/) for more information.

### RAMSES Plugin

RAMSES (Refinement of AADL Models for Synthesis of Embedded Systems) compiles AADL models into code
for ARINC653, POSIX, and OSEK compliant operating systems.

RAMSES is provided by TELECOM Paris. See [their web site](https://mem4csd.telecom-paristech.fr)
for more information.
