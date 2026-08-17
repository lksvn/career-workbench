# Vacancy analysis

## Requirement map

Classify vacancy statements as:

- `mandatory`: explicitly required or central to the role.
- `preferred`: described as desirable, beneficial, or optional.
- `responsibility`: work the hired person is expected to perform.
- `constraint`: location, language, schedule, contract, compensation, authorization, travel, or education condition.
- `context`: industry, product type, team shape, customer type, or development environment.

Separate technologies into languages, frameworks, databases, infrastructure, testing, and workflow. Preserve exact versions only when the vacancy makes them material.

## Evidence states

For each material requirement assign one state:

- `professional`: supported by employment or paid professional-project evidence.
- `project`: supported by a personal, open-source, or volunteer project.
- `study`: supported only by learning or a study project.
- `historical`: supported professionally but explicitly stale or not currently assessed.
- `unsupported`: no confirmed workspace evidence.

Do not collapse `project`, `study`, or `historical` into `professional`.

## Selection signals

Prefer evidence that matches the vacancy's responsibility, not merely its keyword. For example, REST API maintenance may support an integration responsibility even when the target framework differs. Report the framework gap rather than claiming equivalence.

Treat required years as a screening condition, not permission to alter the person's actual career duration. Treat adjacent experience as partial support only when the relationship is clear and factual.
