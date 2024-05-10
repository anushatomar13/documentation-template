# Upgrading


## Upgrading Hyperledger Caliper

Caliper follows semantic versioning (major.minor.patch) for releases. Upgrading to a newer minor or patch version should be backward compatible, while a major version upgrade may include breaking changes.

### Upgrading to a Newer Minor or Patch Version

1. **Backup your existing installation**
    - Make a backup copy of your current Caliper directory in case you need to revert.

2. **Update the codebase**
    - Change to the Caliper directory:
      ```
      cd /path/to/caliper
      ```
    - Fetch the latest code:
      ```
      git pull
      ```

3. **Install new dependencies**
    - Install any new dependencies introduced in the newer version:
      ```
      npm install
      ```

4. **Review release notes**
    - Check the release notes for the new version you are upgrading to.
    - Take note of any configuration changes, deprecated features, or other breaking changes that may impact your setup.

5. **Update configurations**
    - If the release notes mention any changes to configuration file formats or parameters, update your test configurations accordingly.

6. **Verify installation**
    - Run some simple tests to verify that the upgrade was successful:
      ```
      npm run caliper launch -- <simple_test_options>
      ```

### Upgrading to a New Major Version

For major version upgrades, in addition to the steps above, you may need to take additional actions:

1. **Review breaking changes**
    - Carefully review the release notes and documentation for the new major version.
    - Take note of any breaking changes to APIs, configurations, or other core components.

2. **Update code and tests**
    - If you have custom code integrations or test cases, you may need to update them to work with the new APIs and formats introduced in the new major version.

3. **Consider compatibility**
    - Ensure the blockchain system versions you plan to test are compatible with the new Caliper version. You may need to upgrade your blockchain systems first.

4. **Start fresh (optional)**
    - For significant upgrades with many breaking changes, you may want to start with a fresh Caliper installation rather than upgrading in-place.
