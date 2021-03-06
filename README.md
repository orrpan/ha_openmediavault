# homeassistant openmediavault component
A home assistant component that exposes openmediavault as a sensor.

### Installation

Copy this folder into your config directory. You should end up with a file path similar to the following: `<config_dir>/custom_components/openmediavault/`.

Add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
sensor:
  platform: openmediavault
  host: http://openmediavault
  username: admin
  password: !secret openmediavault_password
  monitored_conditions:
    -  hostname
    -  version
    -  processor
    -  kernel
    -  system_time
    -  uptime
    -  load_average
    -  cpu_usage
    -  memory_usage
```

### Configuration

**name** 
    (string) (Optional)

    Name to give the OMV sensor.

Default value:
openmediavault

**host**
    (string) (Required)
    
    Hostname of the openmediavault server

**username**
    (string) (Optional)

    Username used for logging in to openmediavault.

Default value:
admin

**password**
    (string) (Required)
    
    The password used to login to openmediavault