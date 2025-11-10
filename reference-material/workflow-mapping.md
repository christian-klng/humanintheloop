# Workflow Mapping Techniques

Guide for documenting and visualizing observed workflows to identify pain points, inefficiencies, and improvement opportunities.

## Why Map Workflows

Workflow maps help you:
- Visualize actual vs. intended process
- Identify friction points and bottlenecks
- Quantify time costs at each step
- Communicate findings to others
- Compare variations across users
- Spot patterns across observations

## Basic Workflow Notation

### Standard Elements

**Steps:**
```
[1. Action name]
   ↓
[2. Action name]
   ↓
[3. Action name]
```

**Decision Points:**
```
    ↓
   <Decision?>
   /         \
 Yes         No
  ↓           ↓
[Step A]   [Step B]
```

**Pain Points:**
```
[2. Data entry] ⚠️ 10 min, manual, error-prone
```

**Workarounds:**
```
[Official step] ─╳─> [Workaround] 💡 personal spreadsheet
```

**Tool Switches:**
```
[Step in System A] 🔄 → [Step in System B] 🔄 → [Step in System C]
```

**Waiting/Delays:**
```
[Submit request] ⏱️ 2-5 min wait → [Approval appears]
```

### Legend Symbols

- ⚠️ = Pain point / friction
- 💡 = Workaround / adaptation
- 🔄 = Context/tool switch
- ⏱️ = Waiting period
- ❌ = Error-prone step
- 📝 = Manual entry
- 👥 = Requires collaboration
- 🔍 = Verification/checking
- 🔁 = Repeated/loop
- ⚡ = Quick/easy step
- 🐌 = Slow/time-consuming

## Simple Text-Based Workflow

### Linear Process

```
START: [Trigger event]

1. [Step name] - X min
   Tools: [System A]
   Notes: [Observations]

2. [Step name] - X min ⚠️
   Tools: [System A, System B]
   Pain point: [Description]
   Notes: [What you saw]

3. [Step name] - X min
   Tools: [System B]
   Workaround: [Description] 💡
   Notes: [What they do instead]

4. <Decision: [Question]>
   IF Yes → Step 5
   IF No → Step 7

5. [Step name] - X min
   Tools: [System C]

END: [Output achieved]

TOTAL TIME: XX minutes
FRICTION TIME: XX minutes
```

### With Parallel Paths

```
1. [Initial step]
   ↓
   ├─→ Path A: [Fast but risky]
   │   └→ [Result A]
   │
   └─→ Path B: [Slow but safe] ⚠️ Usually chosen
       └→ [Result B]
   
Both paths continue to:
2. [Next step]
```

## Visual Workflow Mapping

### Swimlane Diagram

Shows which person/system handles each step:

```
ACTOR         | WORKFLOW
─────────────────────────────────────────────
User          | [1. Request] → [3. Review] → [5. Implement]
                     ↓             ↓
System        |    [2. Validation] [4. Generate]
                     ↓
Manager       |                [4b. Approval] ⏱️ 2 days
```

### Time-Based Flow

Shows duration of each step:

```
TIME    STEP
────────────────────────────────
0:00    [Start task]
        ↓
0:05    [Login to system] ⏱️ System slow
        ↓
0:07    [Navigate to form]
        ↓
0:10    [Fill section 1] ⚠️ Manual entry
        ↓
0:25    [Switch to spreadsheet] 🔄 Get reference data 💡
        ↓
0:30    [Return to form]
        ↓
0:35    [Fill section 2]
        ↓
0:38    [Submit] ⏱️ Wait for validation
        ↓
0:42    [Fix errors] ❌ Common issue
        ↓
0:45    [Complete]
```

## Comparing Actual vs. Intended

### Side-by-Side Comparison

```
OFFICIAL PROCESS          | ACTUAL OBSERVED PROCESS
─────────────────────────────────────────────────────
1. Login                  | 1. Login ⏱️ 2 min (system slow)
                          | 2. Check sticky note 💡 (remember password changes)
2. Access form            | 3. Access form
                          | 4. Open personal spreadsheet 💡 (get reference data)
3. Fill form              | 5. Fill section 1 📝
                          | 6. Call colleague 👥 (clarify code)
                          | 7. Fill section 2 📝
                          | 8. Double-check entries 🔍 (past errors)
4. Submit                 | 9. Submit
                          | 10. Verify in system 🔍 (confirm it worked)
5. Done                   | 11. Update personal log 💡 (tracking)
                          | 12. Done
───────────────────────────────────────────────────
TIME: 5 min (estimated)   | TIME: 18 min (observed)
STEPS: 5                  | STEPS: 12
```

## Detailed Step Analysis

For each step, document:

```
STEP: [Step name and number]

DURATION: [X minutes]
TOOLS USED: [List of systems/tools]
FREQUENCY: [Every time / Sometimes / Rarely]

WHAT HAPPENS:
[Detailed description of actions]

PAIN POINTS:
- [Issue 1]: [Impact]
- [Issue 2]: [Impact]

WORKAROUNDS OBSERVED:
- [Workaround 1]: [Why they do this]
- [Workaround 2]: [Why they do this]

VARIATIONS:
- Expert users: [What they do differently]
- Novice users: [What they do differently]

IMPROVEMENT OPPORTUNITIES:
- [Opportunity 1]
- [Opportunity 2]

QUOTES:
> "[What subject said about this step]"
```

## Pattern Mapping Across Sessions

### Variation Analysis

```
STEP 3: Data Entry

SESSION 1 (Expert):
└→ 5 min, used keyboard shortcuts, no reference check

SESSION 2 (Intermediate):
└→ 12 min, checked reference 2x, one error corrected

SESSION 3 (Novice):
└→ 25 min, checked reference 5x, asked for help, 3 errors

PATTERN: Entry time correlates with experience
        References needed decrease with time
        Error rate highest for new users
        
INSIGHT: Initial learning curve steep, 
        need better onboarding/training
```

### Consistency vs. Variability

```
CONSISTENT ACROSS ALL SESSIONS:
✓ Step 2 always takes 10-15 min (system limitation)
✓ Step 4 always requires verification (lack of confidence)
✓ Everyone uses spreadsheet workaround at Step 6

VARIES BY CONTEXT:
• Morning sessions: 20% faster (less interruptions)
• High workload: More shortcuts, skip verification
• Team available: Collaboration for Step 3
• Alone: Use workaround instead

VARIES BY USER:
• Experts: Skip Steps 2, 8, optimize Step 5
• Novices: Add verification steps, slower throughout
• Different roles: Different data needed at Step 6
```

## Workflow Metrics Summary

Create a metrics table:

```
METRIC                    | VALUE      | TARGET    | GAP
──────────────────────────────────────────────────
Total task time           | 45 min     | 15 min    | 30 min
Productive time           | 20 min     | -         | -
Waiting time              | 8 min      | 0 min     | 8 min
Rework/error correction   | 7 min      | 0 min     | 7 min
Tool switching            | 5 min      | 2 min     | 3 min
Manual entry              | 15 min     | 5 min     | 10 min
Verification/checking     | 10 min     | 3 min     | 7 min
──────────────────────────────────────────────────
Steps in process          | 15         | 8         | 7 extra
Context switches          | 6          | 2         | 4 extra
External dependencies     | 3          | 1         | 2 extra
```

## Problem Clustering

Group related issues:

```
PROBLEM CLUSTER 1: Data Entry Issues
├─ Pain: Manual entry takes 15 min
├─ Pain: High error rate (30% need correction)
├─ Pain: No auto-save, losing work
└─ Workaround: Copy to notepad first 💡

TOTAL IMPACT: 20 min per task, user frustration

PROBLEM CLUSTER 2: System Integration Gaps
├─ Pain: Must switch between 3 systems
├─ Pain: Copy data manually between systems
├─ Pain: Each switch takes 1-2 min
└─ Workaround: Personal spreadsheet as bridge 💡

TOTAL IMPACT: 8 min per task, 6 context switches

PROBLEM CLUSTER 3: Unclear Requirements
├─ Pain: Must ask colleague for clarification
├─ Pain: Checking reference materials multiple times
├─ Pain: Uncertainty about approval codes
└─ Workaround: Sticky note with common codes 💡

TOTAL IMPACT: 10 min per task, interrupts others
```

## Opportunity Mapping

Identify improvement opportunities:

```
QUICK WINS (Low effort, high impact):
1. Auto-save during data entry → Saves 2 min risk
2. Keyboard shortcuts guide → Saves 3-5 min
3. Code dropdown instead of manual → Saves 5 min

MEDIUM EFFORT:
1. Integration between System A & B → Saves 8 min
2. Pre-fill known fields → Saves 4 min
3. Inline validation → Prevents errors, saves 7 min

LONG TERM:
1. Full automation of Steps 2-5 → Saves 20 min
2. AI-assisted data entry → Saves 15 min
3. Workflow redesign → Saves 30 min total
```

## Presenting Workflow Maps

### Executive Summary Format

```
WORKFLOW: [Name]
FREQUENCY: [X times per day/week]
CURRENT STATE: [X] steps, [Y] minutes, [Z] systems

KEY PROBLEMS:
1. [Problem]: Costs [X] min × [frequency] = [total cost]
2. [Problem]: Costs [X] min × [frequency] = [total cost]
3. [Problem]: Costs [X] min × [frequency] = [total cost]

TOTAL WASTE: [X] hours per week per person
SCALE: [Y] people affected = [Z] hours total waste

RECOMMENDED ACTIONS:
1. [Action] → [Impact]
2. [Action] → [Impact]
```

### Before & After Vision

```
CURRENT STATE (Observed):
[1] → [2] → ⚠️ [3] → 🔄 [4] → [5] → ⚠️ [6] → [7]
45 minutes, 15 steps, 3 systems, 30% error rate

PROPOSED STATE:
[1] → [2+3 automated] → [4+5 integrated] → [6]
15 minutes, 6 steps, 1 system, 5% error rate

SAVINGS: 30 min per task × 10 tasks/day = 5 hours/day
```

## Tips for Effective Mapping

### During Observation
- Sketch rough flow as you watch
- Note timestamp at each transition
- Mark pain points with ⚠️ immediately
- Circle workarounds to explore in Q&A
- Draw arrows for unexpected paths

### After Observation
- Expand rough sketch into clean diagram
- Add time durations to each step
- Annotate with quotes and observations
- Highlight patterns and clusters
- Compare to previous observations

### Across Multiple Sessions
- Create composite "typical" workflow
- Show variations as branches
- Calculate average times
- Identify universal vs. individual pain points
- Document expertise-based differences

## Common Workflow Patterns

### The "Verification Loop"
When users don't trust results:
```
[Do work] → [Check result] → [If unsure, ask colleague] → [Re-check] → [Confirm again]
```
**Indicates:** Lack of confidence or system reliability issues

### The "Context Switch Cascade"
Frequent tool switching:
```
[System A] 🔄 → [System B] 🔄 → [Spreadsheet] 🔄 → [System A] 🔄 → [System C]
```
**Indicates:** Integration gaps, poor tool design

### The "Workaround Web"
Multiple workarounds for one process:
```
Official: [A] → [B] → [C]
Actual:   [A] → [Personal tool 1] → [B workaround] → [Manual step] → [C]
```
**Indicates:** Process broken at fundamental level

### The "Hurry Up and Wait"
Active work interrupted by delays:
```
[Active] → ⏱️ Wait 5 min → [Active] → ⏱️ Wait 3 min → [Active]
```
**Indicates:** System performance or approval bottlenecks

## Workflow Mapping Tools

**Simple (Text-based):**
- Plain text with ASCII art
- Markdown with symbols
- Bulleted lists with indentation

**Medium (Visual):**
- Hand-drawn diagrams (paper/whiteboard)
- Flowchart tools (Lucidchart, Draw.io)
- Swimlane diagrams (Miro, Mural)

**Advanced (Process mining):**
- Process mining software (Celonis, ProcessGold)
- Time-motion study tools
- Video analysis software

**Recommendation:** Start simple, add complexity only if needed for your audience.

## Using Workflow Maps

**For validation:**
- Does this workflow have significant waste? (>30% non-productive time)
- Are pain points consistent across users? (>70% experience them)
- Do workarounds indicate real problems? (Used by multiple people)

**For solution design:**
- Which steps can be automated?
- Where can integration eliminate switching?
- What verification can be built in?
- Which workarounds reveal unmet needs?

**For communication:**
- Show stakeholders actual vs. intended
- Quantify waste for business case
- Visualize improvement opportunities
- Compare before/after scenarios

The best workflow map is one that clearly communicates the problems and opportunities to your audience—whether that's yourself, your team, or executives approving a project.
