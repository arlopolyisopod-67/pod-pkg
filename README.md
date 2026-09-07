# `pod` Package manager

## How to use

1. Run `pod new` to create required folders and files (`pod_packages`, `pod_packages/packages.json`, `main.py`)
2. Run `pod install name@version` to install a new package (if `pod_packages` is not found, it will fail) (you can also go `pod install -F/--file deps.json` to install from a dependency file) (e.g. `pod install foo@1.2.3`)
3. Run `pod remove name@version` to uninstall a package (if no version is provided, it will remove all installed versions from the current `pod_packages` folder) (e.g. `pod remove foo@1.2.3` or `pod remove foo`)
4. Run `pod list` to list installed packages (e.g. `pod list` -> `foo versions 1.2.3, 1.0.0`)
5. Run `pod freeze` to create `deps.json` containing package metadata to be used in `pod install`
6. Run `pod check` to check currently installed packages against the `-F/--file` argument (defaults to `deps.json`)
