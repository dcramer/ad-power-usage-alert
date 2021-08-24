## App configuration

```yaml
power_usage_washer:
  module: power_usage_alert
  class: PowerUsageAlert
  dependencies: sentry
  entity_id: sensor.washer_power
  delay: 3
  input_boolean: input_boolean.washer
  telegram:
    - !secret telegram_group_id_home
  done_message: "The wash machine has finished"
```
