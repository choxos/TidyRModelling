# R Code Review

Comprehensive code review for R scripts and packages. This command uses the **r-code-reviewer** agent (Opus) to perform thorough quality assessment.

## Review Scope

### Style Review
- Tidyverse style guide compliance
- Naming conventions (snake_case, meaningful names)
- Code formatting and indentation
- Pipe usage and readability

### Quality Review
- Function design (single responsibility, pure functions)
- Error handling patterns
- Documentation completeness
- DRY principle adherence

### Performance Review
- Vectorization opportunities
- Memory efficiency
- Computational bottlenecks
- Parallel processing opportunities

### Security Review
- Input validation
- Credential handling
- SQL injection prevention
- Safe file operations

### Testing Review
- Test coverage assessment
- Test quality and patterns
- Edge case coverage
- Mocking practices

## Usage

```
/r-code-review [path] [review_type]
```

### Parameters
- `path`: Path to R file, directory, or package (default: current directory)
- `review_type`: One of `full`, `style`, `performance`, `security`, `tests` (default: full)

## Output Location

Review report will be written to:
```
output/
└── reports/
    └── code_review_[timestamp].md
```

## Review Report Structure

1. **Executive Summary**
   - Overall assessment
   - Key findings count by severity
   - Recommended priority actions

2. **Detailed Findings**
   - Each issue with:
     - Severity (Critical, Major, Minor, Suggestion)
     - Location (file:line)
     - Description
     - Recommendation
     - Code example (before/after)

3. **Metrics**
   - Lines of code
   - Function count and complexity
   - Test coverage (if available)
   - Documentation coverage

4. **Positive Observations**
   - Well-written code patterns
   - Good practices observed

## Example

```
/r-code-review R/ full
```

This will perform a comprehensive review of all R files in the R/ directory.

## Integration with CI/CD

The review output can be integrated into GitHub Actions or other CI pipelines:

```yaml
- name: R Code Review
  run: |
    # Generate review report
    # Parse for critical issues
    # Fail if critical issues found
```

## Notes

- Review is read-only - no code modifications are made
- All suggestions are written to the output folder
- Large codebases may be reviewed in sections
