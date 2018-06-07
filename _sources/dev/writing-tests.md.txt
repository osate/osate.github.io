# Writing Tests

We use a stylized way of writing tests based on the xtext testing framework. The
test class declaration must extends XtextTest and be annotated as follows:

```
@RunWith(XtextRunner)
@InjectWith(Aadl2InjectorProvider)
class ModeTransitionsTest extends XtextTest {
```

It is important to use the `Aadl2Injectorprovider` and not the UI injector provider
as the UI injector requires the presence of files in an Eclipse workspace.

## Provided Helper Classes

### Class TestHelper

This class provides access to the parser, linker, validator, etc. and can process
AADL strings and AADL files. It must be injected into the test class:

```
@Inject
TestHelper<AadlPackage> testHelper
```

### Class TestResourceSetHelper

This class provides a singleton resource set that can be reused across tests. The
resource set is initialized on creation with all contributed AADL property sets and 
packages. It is mainly there for use in `TestHelper`. Note that each call to 
`getResourceSet()` returns the same resource set but removes all resources loaded
since the previous call.

### Class AssertHelper

This class provides a couple of extension methods for working with the `FluentIssueCollection`
and to test scoping.

## Examples

There are a couple of examples that show how tests can be written:

- in `org.osate.core.tests`
   - [Issue277Test.xtend](https://github.com/osate/osate2/blob/develop/core/org.osate.core.tests/src/org/osate/core/tests/issues/Issue277Test.xtend)
     This shows how to parse a string that contains AADL text and work with the resulting
     AADL Package.
   - [Issue361Test.xtend](https://github.com/osate/osate2/blob/develop/core/org.osate.core.tests/src/org/osate/core/tests/issues/Issue361Test.xtend)
     This test shows how to instantiate a component implementation and work with the
     resulting instance model. Note that the instance model must be created in the same
     resource set as the declarative AADL model.
   - [Issue1092Test.xtend](https://github.com/osate/osate2/blob/develop/core/org.osate.core.tests/src/org/osate/core/tests/issues/Issue1092Test.xtend)
     This test shows how to analyze issues reported during instantiation, see method
     `testUnmappedModes()`.
   - [ModeTransitionsTest.xtend]
     This test shows how to get a fluent issue collection from an AADL string and how
     to work with it. 

## Running tests

Tests can be run in the development environment using `Run as...` -> `JUnit Plug-in Test`.
Running a plain JUnit tests does not work because the test envoronment needs the eclipse
plugin mechanism to load contributed AADL property sets and packages.

In the tycho build, test plugins must run with the UI enabled because tests load plugins
that depend on UI plugins even if they don't use the UI during the test.
