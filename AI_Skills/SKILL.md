---
name: digital-systems-benchmark
description: |
  >Digital_tool_pratice
  
---
# Digital Systems & IC Logic Exam Benchmark Synthesizer

## Purpose & Scope
This skill bridges the gap between limited local past exam papers and world-class digital hardware benchmarks. It analyzes slides, past midterms/finals, and tutorial sheets from the HCMUT Talented Bachelor's Program (Digital Systems/Microchip Design track), extracts core hardware abstractions, and synthesizes parallel (isomorphic) exam problems calibrated against MIT, Berkeley, and Stanford standards.

## Target Course Modules & Mapping
- **Boolean & Combinational Logic**: Hazard analysis, optimal SOP/POS, Multi-level logic synthesis, Propagation ($t_{pd}$) vs. Contamination ($t_{cd}$) delays. (Cross-mapped to: MIT 6.004 L1-L4).
- **Arithmetic Modules**: Carry-Lookahead, Carry-Skip, Wallace Tree / Booth Multipliers, ALU control flags. (Cross-mapped to: Berkeley EECS 151 Lab/Midterm).
- **Sequential Timing Analysis**: Setup time ($t_{su}$), Hold time ($t_h$), Clock-to-Q ($t_{cq}$), Clock Skew ($\delta$), Metastability, Maximum operating frequency ($f_{max}$). (Cross-mapped to: Berkeley EECS 151, Stanford EE108).
- **FSM Engineering**: Mealy vs. Moore structural transformations, State reduction (Implication charts), Glitch-free outputs, Sequence detectors with overlapping/non-overlapping constraints.

## Generation Pipeline

### Step 1: Input Deconstruction
When the user uploads a problem, slide, or past exam snippet:
1. Identify the core hardware primitive (e.g., Timing path with clock skew, Carry Lookahead block, Non-ideal latch behavior).
2. Identify the parameter constraints (e.g., $t_{pd,mux} = 2\text{ ns}$, $t_{setup} = 0.5\text{ ns}$, Skew $\pm 0.2\text{ ns}$).
3. Pinpoint common student traps (e.g., ignoring contamination delay when calculating hold violation, false paths in combinational logic).

### Step 2: Global Benchmark Cross-Query
Retrieve equivalent problem architectures from:
- **MIT 6.004 Past Quizzes**: Focus on elegant, conceptual, modular reasoning.
- **UC Berkeley EECS 151 / 251A Midterms**: Focus on realistic physical constraints, critical paths, and area-delay-power trade-offs.
- **Stanford EE108 / EE180 Assignments**: Focus on robust synchronous system design and edge-case handling.

### Step 3: Synthesizing Isomorphic Problem Sets
Generate 3 distinct tiers of practice:
- **Tier 1 (HCMUT Baseline Match)**: Same complexity and format as the provided sample; ideal for cementing fundamental concepts.
- **Tier 2 (Top-Tier University Equivalence - Berkeley/MIT Level)**: Same core mathematical/hardware theory, but adds non-ideal parameters (e.g., wire delay, setup/hold variations under clock skew, multi-cycle paths).
- **Tier 3 (Honor Challenge / Edge-Case Trap)**: Questions that test boundary conditions (e.g., dynamic race hazards, asynchronous reset deassertion hazards, metastability resolution).

### Step 4: Step-by-Step Derivation & Grading Rubric
For every generated problem, include:
1. **Governing Equation**: Clearly state formulas (e.g., $T_{clk} \ge t_{cq} + t_{pd,comb} + t_{setup} - t_{skew}$).
2. **Analytical Derivation**: Full intermediate substitution steps with physical units ($\text{ns}$, $\text{MHz}$, gate equivalents).
3. **Common Trap Warning**: Explicitly highlight where students typically lose points in exams.
4. **Grading Rubric**: Points distribution matching an official university marking scheme.

## Output Constraints
- Render all circuit equations, timing inequalities, and logic states using LaTeX ($...$ and $$...$$).
- Provide ASCII circuit diagrams, timing waveforms, or state transition tables whenever visual architecture is involved.
- Maintain rigorous engineering terminology used in standard IEEE digital design curricula.
