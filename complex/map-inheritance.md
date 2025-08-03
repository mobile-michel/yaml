---
title: Map inheritance
date: 2025-08-01
---
# {title}

```
# 1. Define a base configuration template using an anchor (&base_config)
base_config: &base_config
  api_version: v1
  timeout: 5000
  retries: 3
  monitoring:
    enabled: true

# 2. Create a 'development' configuration that inherits from the base
development_service:
  <<: *base_config  # Use alias (*) to inherit all keys from &base_config
  # Override a key from the base
  timeout: 1000
  # Add a new key specific to development
  debug_mode: true

# 3. Create a 'production' configuration that also inherits from the base
production_service:
  <<: *base_config  # Inherit from the same base config
  # Override keys for production needs
  retries: 5
  # Add a new key
  replicas: 10
```

## Development Service

- api_version: {development_service.api_version}
- timeout: {development_service.timeout}
- retries: {development_service.retries}
- monitoring enabled: {development_service.monitoring.enabled}
- debug_mode: {development_service.debug_mode}

## Production Service

- api_version: {production_service.api_version}
- timeout: {production_service.timeout}
- retries: {production_service.retries}
- monitoring enabled: {production_service.monitoring.enabled}
- replicas: {production_service.replicas}