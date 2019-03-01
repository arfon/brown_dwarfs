# Arfon's Fantastic List of Brown Dwarfs

This is a test repository for the MAST Lists service. This repository contains a `List` definition, `list.yaml` which defines the properties of the List, together with the available properties for `Things` in the `List`:

```YAML
name: "Arfon's Fantastic List of Brown Dwarfs"
description: "Arfon's list of brown dwarfs. Hand-picked just for you."
properties:
  - name: "Short Name"
    kind: "String"
    units: ""
    required: "true"
    group: "Default"
    key: "default_short_name"
```

`List` items (known as `Things`) are in the `things` folder and follow a format of one `Thing` per YAML file. `Thing` definition files can follow any naming convention. The filename for a `Thing` is not special but in this case we're using the filename to make it more straightforward to identify the brown dwarf we're describing (e.g. `1658+1820.yaml`)

`Thing` YAML definitions may only contain properties that are already defined on the parent `List` in `list.yaml`:

```YAML
default_short_name:
  value: "1658+1820"
  origin: ""
default_alternate_designation:
  value: "SDSS J16585026+1820006"
  origin: "https://arxiv.org/abs/1408.3089"
default_distance:
  value: ""
  origin: ""
default_ra:
  value: "254.709737"
  origin: ""
default_dec:
  value: "18.333275"
  origin: ""
```

## Data Validation

[![Build Status](https://travis-ci.org/arfon/brown_dwarfs.svg?branch=master)](https://travis-ci.org/arfon/brown_dwarfs)

This List repository knows how to validate itself by running the tests in `list_test.rb`. Any modifications to the `Thing` YAML files or the `List` definition in `list.yaml` will be tested by Travis-CI.
