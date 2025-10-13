---
description: Performance improvement agent (V1 Baseline - Control)
argument-hint: [auto]
allowed-tools: Bash(*), Read, Write, Edit, Glob, Grep
model: claude-sonnet-4-5-20250929
---
# Performance Improvement Task

Your goal is to systematically optimize this codebase for better performance while maintaining correctness.

## Objectives:
1. Improve performance metrics by at least 20% from baseline
2. Maintain 100% test suite pass rate
3. Preserve all existing functionality
4. Apply proven optimization techniques

## Steps to follow:
1. Review the baseline benchmark results to identify bottlenecks
2. Run the existing test suite to establish correctness baseline
3. Identify optimization opportunities (use profiling if needed)
4. Apply optimizations incrementally, one at a time
5. After each change:
   - Run full test suite (must pass 100%)
   - Run benchmarks to measure improvement
   - Document the change and impact
6. Iterate until performance targets are met

## Optimization strategies to consider:
- **Algorithmic improvements**: Better time/space complexity
- **Data structure optimization**: Choose more efficient structures
- **Caching/memoization**: Reduce redundant computations
- **Lazy evaluation**: Defer expensive operations
- **Vectorization**: Batch operations where possible
- **I/O optimization**: Reduce disk/network calls
- **Memory management**: Reduce allocations, reuse objects
- **Parallelization**: Leverage multiple cores where applicable
- **Database optimization**: Index usage, query efficiency
- **Loop optimization**: Reduce iterations, hoist invariants

## Critical rules:
- **NEVER break existing tests** - if tests fail, revert the change
- **Measure, don't guess** - always benchmark before/after
- **One change at a time** - isolate the impact of each optimization
- **Document trade-offs** - note any complexity or maintainability impacts
- **Validate correctness first** - performance means nothing if the code is wrong

## Output format:
For each optimization iteration, document:
```
Optimization #N: [Brief description]
Target: [Function/module being optimized]
Technique: [What optimization was applied]
Baseline: [Original benchmark results]
Improved: [New benchmark results]
Speedup: [X% improvement or Nx faster]
Tests: [PASS/FAIL]
Notes: [Any important considerations]
```

Please analyze the codebase, benchmarks, and tests, then systematically apply performance optimizations.

Start by profiling to identify the biggest bottlenecks, then tackle them in order of impact.