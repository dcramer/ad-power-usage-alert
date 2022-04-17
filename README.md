Notify when your dryer finishes running:

```yaml
power_usage_dryer:
  module: power_usage_alert
  class: PowerUsageAlert
  dependencies: sentry
  entity_id: sensor.dryer_energy_power
  deactivation_delay: 3
  namespace: hive
  telegram:
    - !secret telegram_group_id_home
  done_message: "The dryer has finished"
```

Notify when the espresso machine has warmed up:

```yaml
espresso_machine:
  module: power_usage_alert
  class: PowerUsageAlert
  dependencies: sentry
  entity_id: sensor.espresso_machine_power
  activation_delay: 600
  namespace: hive
  telegram:
    - !secret telegram_group_id_home
  message: "The espresso machine is ready"
```
