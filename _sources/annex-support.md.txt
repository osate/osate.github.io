# Annexes Supported in OSATE

## EMV2 Language Support

OSATE strives to supports all of EMV2 as specified in the annex standard. However,
the syntax used to apply a property to an EMV2 annex element in a subcomponent
cannot be implemented in our LL(k) parser because it requires infinite look-ahead
to distinguish applies to paths that contain an '@' from those that do not.

We use the following modified rule (note the added ^)

```
emv2_containment_path ::=
     [ ^ aadl2_core_path @ ] emv2_annex_specific_path
```

The EMV2 implementation in OSATE contains the following extensions that are
proposed as errata (see [here](https:github.com/saeaadl/emv2/))

* Repair events require a `when` keyword
  ([#3](https://github.com/saeaadl/emv2/issues/3))
* Allow single trigger as argument for operators `ormore`, `orless`, ...
  ([#4](https://github.com/saeaadl/emv2/issues/4))
* Support for operators `all` and `all (...) but`
  ([#7](https://github.com/saeaadl/emv2/issues/7))
* Allow out propagation of a subcomponent in out propagation condition
  ([#11](https://github.com/saeaadl/emv2/issues/11))
* Allow references to out propagations of deeply nested subcomponents
  ([#26](https://github.com/saeaadl/emv2/issues/26))
