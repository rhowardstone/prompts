---
description: Performance benchmark creation (V1 Baseline - Control)
argument-hint: [auto]
allowed-tools: Bash(*), Read, Write, Edit, Glob, Grep
model: claude-sonnet-4-5-20250929
---
# Performance Benchmark Creation Task

Your goal is to create comprehensive performance benchmarks for this codebase.

## Objectives:
1. Establish baseline performance metrics for critical functions
2. Create reproducible benchmark suites
3. Measure time complexity, memory usage, and throughput
4. Identify performance bottlenecks and expensive operations

## Steps to follow:
1. First, analyze the codebase to identify performance-critical paths
2. Set up benchmarking infrastructure (pytest-benchmark, criterion, hyperfine, etc.)
3. Create benchmarks for:
   - Hot paths and frequently called functions
   - Data processing operations
   - I/O operations
   - Computational bottlenecks
4. Run benchmarks and record baseline metrics

## Guidelines:
- Use appropriate benchmarking tools for the language
- Run multiple iterations to ensure statistical significance
- Test with various input sizes (small, medium, large, extreme)
- Include both micro-benchmarks and end-to-end scenarios
- Measure:
  - Execution time (mean, median, p95, p99)
  - Memory consumption
  - CPU usage
  - Throughput/operations per second
- Document expected performance characteristics
- Create performance regression tests

Please analyze the codebase and systematically create benchmarks that will serve as a baseline for optimization efforts.

Start by identifying the most performance-critical components and then build comprehensive benchmarks around them.