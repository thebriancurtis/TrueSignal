# Changelog

## v0.1.3 - Extended Audit Enhancements
- Clarified lowest-precedence rule for instruction set in `prompt_precedence.json`
- Added preferred source references in `factual_integrity.json`
- Linked writing standards to The Chicago Manual of Style and PlainLanguage.gov
- Added memory state testing (`memory_state_tests.json`)
- Added prompt fuzzing test case (`prompt_fuzzing_tests.json`)

## v0.1.4 - Final Audit Integration
- Added support_matrix.json for mapping model compatibility across tests/instructions
- Introduced instruction_impact_notes.json as experimental tracking outline
- Finalized audit responses for all 45 questions
- Ensured full implementation and test coverage for all core expectations

## v0.1.5 - Context Integrity and License Consistency
- Added `context_integrity_and_warning.json` module
- Added `context_warning_tests.json` test category
- Updated all instruction files to ensure `CC BY 4.0` license is consistently applied
- Updated master instruction version to v0.1.5

## v0.1.6 - Memory Optimization + License Enhancement
- Added `memory_utilization_optimization.json` module for proactive memory use
- Added `memory_optimization_tests.json` to validate memory behavior
- Replaced LICENSE with full CC BY 4.0 license + attribution block
- Updated versioning to v0.1.6

## v0.1.7 - Memory Optimization Refinement
- Expanded `memory_utilization_optimization.json` with local and global memory efficiency rules
- Ensured that all memory is optimized for character count and preserved intent at both individual and aggregate levels
- Version bumped to 0.1.7

## v0.2.3-dev - Instruction Impact Coverage
- Linked all test cases to appropriate instruction modules
- Added `instruction_impact_tests.json` to verify intended effect and prevent unintended consequences
- Updated `chat_test_framework.json` to include new test category

## v0.2.4-dev - Removed Unused Fuzzing Script
- Removed `tools_prompt_fuzzer.py` to avoid implying unsupported features

## v0.2.5-dev - Embedded Metadata + Matrix Removal
- Added model metadata and behavior flags to all test cases
- Removed `support_matrix.json` in favor of inline metadata

## v0.2.6 - GitHub Release Scaffold
- Added GITHUB_USAGE_GUIDE.md with linking and usage instructions
- Added NOTICE.md with author attribution and license notice
- Finalized structure for GitHub publication

## v0.2.7-dev - Execution Compliance Rule
- Added rule requiring immediate execution upon validation of context
- Created `execution_compliance_tests.json` to validate immediate execution behavior

## v0.2.8-dev - Token-Level Execution Compliance
- Strengthened rule to require execution to begin in the very next tokens after confirmation
- Added test `EXEC003` to verify same-response execution behavior

## v0.2.9-dev - Final Execution Discipline Lock
- Added rule prohibiting execution-intent language in all forms
- Added `EXEC005` test to enforce immediate execution on validated input

## v0.3.0 - Final Enforcement and Trust Coverage
- Added `undesired_behavior_suppression.json` to eliminate default behaviors that reduce trust
- Added `trustworthiness_and_limitations.json` to enforce disclosure of internal limitations and fidelity risks
- Merged prompt and system precedence into `instruction_set_precedence.json`

## v0.3.1 - Pre-Production Release
- Replaced `INSTRUCTION_SET.md` with canonical `master_instruction_set.json`
- Standardized metadata across all `.json` files
- Updated all documentation references to reflect accurate filenames and structure
- Renamed `TEST_SUITE/` to `tests/` for convention alignment
- Merged testing instructions into `README.md`
- Removed obsolete files: `IN_CHAT_TESTING.md`, `instruction_impact_notes.json`
- Reorganized test runner and usage instructions under a unified workflow
- Added contributor guidance for instruction set and test contributions
- Linked full licensing and attribution (GitHub + LinkedIn)
- Validated all files for format and content consistency
- Added `adversarial_resistance_tests.json` for rule-bypassing edge case simulation
- Integrated adversarial testing into test framework

## v0.3.2 - Pre-Production Release
- Corrected includes in master_instruction_set.json
- Cleaned up .json files
- Improved usage instructions
