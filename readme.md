# Engine Test Data

> [!NOTE]
> Test case files may contain descriptions in JSON5-compliant comments. Test implementations should be ready to parse JSON5.

E2E tests for all Flagsmith Engine implementations.

## Engine Evaluation Tests

Test cases ported from v1 are named in the pattern of `test_case/test_{context_value}__{matching_segments}.json`, where:
 - `{context_value}` is the main context value matched in the case — usually, `$.identity.identifier`.
 - `{matching_segments}` is a dunder-delimited matched segments list, e.g. `segment_two__segment_three`. In case no segments match, `default` is used.

Single test case contents are described with [schema.json](./schema.json) JSONSchema.

## Mapper Tests

> [!WARNING]
> Mapper tests exist only to support safe deprecation of the environment document. These tests validate the conversion layer between the legacy environment document format and the evaluation context.

Mapper test cases validate the conversion from environment documents to evaluation contexts. Test files are located in `mapper_test_cases/` and follow the naming pattern `test_mapper__{description}.jsonc`.

Each mapper test case contains:
- `environment_document`: The input environment document
- `expected_evaluation_context`: The expected output evaluation context
