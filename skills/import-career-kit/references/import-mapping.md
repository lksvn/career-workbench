# Career Kit import mapping

## Source precedence

Follow the source repository's own instructions. When it identifies `PROFILE.md` as canonical, use it for facts and treat resumes, forms, and cover letters as derived evidence. A derived artifact may reveal a conflict but must not silently override the canonical profile.

## Destination mapping

| Source concept | Destination |
| --- | --- |
| Name, contact details, location, links | `profile.yaml` → `person` |
| Headline, summary, target roles, preferences, languages | `profile.yaml` → `positioning` |
| Employment and contract roles | `experience.yaml` |
| Personal, study, open-source, volunteer, or named professional projects | `projects.yaml` |
| Degrees, courses, certifications | `education.yaml` |
| Technologies and practices with explicit context | `skills.yaml` |
| Files read, supported claims, ambiguities, disagreements | `evidence.yaml` |

## Classification rules

- A technology named only in learning, roadmap, or project material is not professional experience.
- A responsibility is not an achievement unless a supported result is stated.
- Preserve the available date precision; do not manufacture months or days.
- Store unsupported metrics as pending or rejected claims, never canonical facts.
- Exclude application logs, recruiter data, reference contact details, and unrelated private material unless explicitly requested.

## Import report

List counts and record IDs rather than repeating sensitive content unnecessarily. Identify each conflict with the source references needed to resolve it.
