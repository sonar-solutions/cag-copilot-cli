# Sonar Context Augmentation directives

## Before generating or modifying code

- Call `get_guidelines` to retrieve project-specific coding standards and quality rules. Apply these guidelines to all generated code.
- Call `get_current_architecture` to understand the project's module structure and component relationships before making structural changes.
- Use `search_by_signature_patterns` or `search_by_body_patterns` to locate existing implementations before creating new classes or methods. Follow established patterns.

## Before structural changes

- Call `get_intended_architecture` to check for user-defined architectural constraints.
- Use `get_upstream_call_flow` and `get_downstream_call_flow` to trace the impact of changes through the call graph.
- Call `get_references` to identify all inbound and outbound dependencies for any class or module being modified.
- Call `get_type_hierarchy` to understand inheritance relationships before adding new subclasses or implementations.

## Before adding or updating dependencies

- Call `check_dependency` with the Package URL (purl) to verify the dependency is free of known vulnerabilities, malware, and license issues.

## After modifying code

- Use `show_rule` to look up details for any SonarQube rule violations flagged during analysis.
