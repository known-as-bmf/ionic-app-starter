JDK 1.8+
Update Android SDK (API 25)

{
  "common": {
    // Base Angular app constants.
    "constants": {}
  },
  "builds": {
    "dev": {
      // Allows to exclude some cordova plugins per build.
      "excludePlugins": [],
      // Per build Angular constants.
      "constants": {}
    },
    "test": {
      "excludePlugins": [],
      "constants": {}
    },
    "preprod": {
      "excludePlugins": [],
      "constants": {}
    },
    "qa": {
      "excludePlugins": [],
      "constants": {}
    },
    "prod": {
      "excludePlugins": [
        // The Cordova console plugin should be
        // excluded in the production build.
        "cordova-plugin-console"
      ],
      "constants": {}
    }
  },
  "apps": {
    "default": {
      // App name in config.xml, optionnal as it can be specified per build.
      "name": "App",
      // App id in config.xml, optionnal is it can be specified per build.
      // Can either be a string or an object. If an object then a "ios" key
      // must be present (default) and an "android" key can be present so
      // that one can use a different id for iOS and Android. iOS allows
      // dashes and disallows underscores in the id, Android does the
      // opposite. For this reason you should not use both of them and
      // specify the id as a string.
      "id": {
        "ios": "",
        "android": ""
      },
      // Per app Angular constants.
      // You should always use UNDERSCORE_SNAKE names by convention.
      "constants": {
        // Mandatory
        "I18N": {
          // Mandatory, you must provide at least one locale for your app.
          // Use bcp47 locale identifiers.
          "locales": ["en-US"],
          // Optionnal: first locale in locales array if not specified.
          "default": "en-US"
        }
      },
      // Per app builds configuration.
      "builds": {
        "dev": {
          // Optionnal if a global app name is specified. If so, the
          // build key will be appended to the app name to allow for
          // quick apps differenciation on the device springboard.
          // If specified, the overrides the global app name.
          "name": "App dev",
          // Same as global app id except this will override
          // it if specified. If not specified, a global one must
          // exist and the build key will be appended to it to allow
          // for installing multiple builds on the same device.
          "id": {
            "ios": "",
            "android": ""
          },
          // Per app build Angular constants.
          "constants": {
            "API_SERVER_URL": ""
          }
        },
        "test": {
          "name": "App test",
          "id": {
            "ios": "",
            "android": ""
          },
          "constants": {
            "API_SERVER_URL": ""
          }
        },
        "preprod": {
          "name": "App preprod",
          "id": {
            "ios": "",
            "android": ""
          },
          "constants": {
            "API_SERVER_URL": ""
          }
        },
        "qa": {
          "name": "App qa",
          "id": {
            "ios": "",
            "android": ""
          },
          "constants": {
            "API_SERVER_URL": ""
          }
        },
        "prod": {
          // The build key will not be appended to the app name for prod.
          "name": "App",
          "id": {
            "ios": "",
            "android": ""
          },
          "constants": {
            "API_SERVER_URL": ""
          }
        }
      },
      "targets": {
        "smartphone": {
          "constants": {}
        },
        "tablet": {
          "constants": {}
        }
      }
    }
  }
}
