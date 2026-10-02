# HanMove Automation Archive

A historical Django/Celery project for scheduling HanMove service requests. It includes a web interface, asynchronous jobs, and administrator-managed periodic tasks.

Original Chinese documentation: [README.zh-CN.md](README.zh-CN.md).

## Requirements

A historical Python environment compatible with Django 1.11.16 and Celery 3.1.25, the pinned packages in `requirments.txt` (original spelling), and RabbitMQ. These versions are unsupported.

## Getting started

Review the archived Chinese setup guide and task code before running. For isolated research, install the pinned environment and configure a local broker/database. Do not point scheduled jobs at a real account without explicit authorization.

## Project structure

| Path | Purpose |
| --- | --- |
| `manage.py` | Django management entry point |
| `fuckhanmu_web` | Django project and Celery setup |
| `autorun` | Views and background tasks |
| `templates` | Web interface |
| `requirments.txt` | Historical dependency pins |

## Configuration and limitations

The original workflow uses Django migrations plus separate web, Celery worker, beat, and Flower processes. Its periodic-task setup assumes a pre-existing crontab record ID. The name is historical; `hanmove-automation-archive` would describe the content more clearly.

## Development and validation

No reproducible current-runtime setup or automated integration tests are supplied. Review broker connectivity and task behavior against an authorized test service before enabling scheduling.

## Related projects and attribution

Original attribution includes [zyc199847](https://github.com/zyc199847), [goolhanrry](https://github.com/goolhanrry), and [S-Ex1t](https://github.com/S-Ex1t).

## License

No root-level license file is included. Check source-specific notices and obtain permission before redistribution or reuse.
