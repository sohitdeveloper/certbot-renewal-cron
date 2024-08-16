# Certbot Renewal Cron Job

This repository contains a cron job configuration for automatic renewal of SSL/TLS certificates using Certbot.

## Overview

The cron job is set to run every 12 hours and performs the following tasks:
- Checks if the Certbot executable exists.
- Ensures that the system is not using `systemd`.
- Introduces a random delay to distribute load.
- Runs the Certbot renewal command to renew certificates quietly.
