# Example 01 — False Overlap Correction

## Before
Overlap tags applied, but no true simultaneity.

## Issue
Sequential speech incorrectly marked as overlapping.

## Decision
Remove overlap tags.

## Reasoning
- Main clause intact  
- No simultaneous speech  
- Improves readability and structure  

## Key Insight
Overlap must represent simultaneity, not segmentation error.

## Decision Trace
- Structure: intact  
- Simultaneity: false  
- Information value: preserved without overlap  
→ Action: remove overlap  

## After
Sequential structure restored.
