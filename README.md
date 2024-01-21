# Development repo for _Anoesis Audio_ Eurorack modules

## Repo Structure

This repo, _ano_modules_prv_, includes folders for modules with this structure:

> __<module name>__ - contains the name.c file & those it runs
  > __bootloader__ - bootloader unique to this module
  > __data__ - binaries included in what is stored on the module
  > __drivers__ - drivers unique to this module
  > __hardware_design__ - KiCad files, etc.
  > __python__ - scripts used to do pre-build things for this module
  > __tests__ - test scripts

This repo relies on _ano_lib_prv_, which is included as a submodule at the same level as the module folders.

```zsh
# cd ano_modules_prv
git submodule add -b main https://github.com/MyPublicGitHubAcct/ano_lib_prv.git
```

Update all submodules in the repo like:

```zsh
# cd ano_modules_prv
git submodule init
git submodule update
```


## Examples

- _secondblink_ shows a simple blink program with the drivers outside of the folder structure (i.e., as part of _ano_lib_dev_). Additionally, the "Core" folder is removed in favor of "Inc" and "Src" being direct children of the main project folder.
