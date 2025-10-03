# Engine Test Data

E2E tests for all Flagsmith Engine implementations.

Test cases ported from v1 are named in the pattern of `test_case/test_{context_value}__{matching_segments}.json`, where:
 - `{context_value}` is the main context value matched in the case — usually, `$.identity.identifier`.
 - `{matching_segments}` is a dunder-delimited matched segments list, e.g. `segment_two__segment_three`. In case no segments match, `default` is used.

Single test case contents are described with [schema.json](./schema.json) JSONSchema.

A test case file may contain a test description in the form of a JSONC comment in the beginning of the file. Test implementations should be ready to parse JSONC.
