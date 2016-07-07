Config
========

Config is a simple library to make loading configuration json structs from file and environment consistent and easy. It
exposes two functions, `LoadConfigurationFromFile` and `LoadConfigurationFromEnvironmentVariables`.

Structs that can be loaded from these functions should have public members be marked with `json:"fieldname"` tags to specify custom
json names to load from. Environment variables should be marked with `env:"ENV_VARIABLE"` tags. By default, if there is no json tag,
the name of the member is used. If there is no env tag, then the member will not be affected by LoadConfigurationFromEnvironmentVariables.