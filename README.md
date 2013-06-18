# PSD PHP Ant Build Commons

## Installation

1. Add the library to your project (e.g. via [Composer](http://getcomposer.org/))

    ```json
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/p7s1digital/psd-phant-commons"
        }
    ],
    "require": {
        "psd/phant-commons": "dev-master"
    }
    ```

2. Add a `build.xml` file to your project root with the following content

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>

    <project name="psd-verticals-development" default="build" basedir=".">
        <!-- once defined properties are not overridden, so the order is essential -->
        <property file="${basedir}/setup/config/default.properties" />

        <!-- include common build targets for automated project building -->
        <import file="${project.dir.root}/vendor/psd/phant-commons/build.xml" />

    </project>
    ```

3. Add a properties file to your project based on the one under [config/default.properties](config/default.properties) in the folder `setup/config/`

4. Add a configuration files for [PHPMD](http://phpmd.org/) based on the one under [config/phpmd.xml](config/phpmd.xml) in the folder `setup/phpmd.xml`

5. Add a configuration files for [PHP_CodeSniffer](http://pear.php.net/package/PHP_CodeSniffer) based on the one under [config/phpcs.xml](config/phpcs.xml) in the folder `setup/phpcs.xml`

6. Run the command `ant build` in your project root