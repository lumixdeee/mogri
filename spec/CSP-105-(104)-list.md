# CSP-105 Instruction Prompt

This file uses the CSP-105 framework, a set of 105 core linguistic/conceptual primitives designed to:

1. Constrain concept introduction and reduce hallucination.
2. Ensure consistency and stability across reasoning steps.
3. Force explicit acknowledgment of missing primitives instead of making assumptions.

**Usage:**  
When interpreting or generating content from this file, map all concepts to CSP-105 primitives. Avoid introducing new concepts or unstated assumptions. Highlight any missing primitives rather than inventing them.

==================================================================================

CONCISE LIST

1. Existence / Being (Prehistory – always)  
2. Identity / Name (Prehistory – always)  
3. Action / Event (Prehistory – always)  
4. Property / Attribute (Prehistory – always)  
5. Quantity / Number (Prehistory – ~3000 BCE)  
6. Space / Location (Prehistory – always)  
7. Time / Temporal Relation (Prehistory – always)  
8. Causality / Mechanism (Prehistory – 600 BCE)  
9. Comparison / Relation (Prehistory – 600 BCE)  
10. Negation / Absence (Prehistory – always)  
11. Direction / Orientation (Prehistory – always)  
12. Possession / Ownership (Prehistory – 1000 BCE)  
13. Communication / Signal (Prehistory – ~5000 BCE)  
14. Modality / Capability (Prehistory – 1000 BCE)  
15. Emotion / Feeling (Prehistory – always)  
16. Identity / Role (Prehistory – always)  
17. Intention / Desire (Prehistory – ~5000 BCE)  
18. Aggregation / Grouping (Prehistory – 1000 BCE)  
19. Boundary / Limit (Prehistory – 600 BCE)  
20. Existence / Presence (Prehistory – 1000 BCE)  
21. Change / Transformation (Prehistory – always)  
22. Identity / Class (Prehistory – ~1000 BCE)  
23. Sequence / Order (Prehistory – 1000 BCE)  
24. Measurement / Magnitude (Prehistory – 3000 BCE)  
25. Comparison Value / Benchmark (Prehistory – 3000 BCE)  
26. Attribute Relationship / Correlation (Prehistory – 1000 BCE)  
27. Persistence / Continuity (Prehistory – ~1000 BCE)  
28. Separation / Distinction (Prehistory – 1000 BCE)  
29. Scale / Proportion (Prehistory – 1000 BCE)  
30. Connection / Network (Prehistory – 1000 BCE)  
31. Change Rate / Dynamics (Prehistory – ~1000 BCE)  
32. Potential / Latent State (Prehistory – always)  
33. Observation / Detection (Prehistory – 1000 BCE)  
34. Cause / Effect (Prehistory – 600 BCE)  
35. Possibility / Contingency (Prehistory – 1000 BCE)  
36. Constraint / Limitation (Prehistory – 1500 CE)  
37. Threshold / Critical Point (Prehistory – 1500 CE)  
38. Error / Anomaly (Prehistory – 1500 CE)  
39. Correction / Adjustment (Prehistory – 1500 CE)  
40. Process / Procedure (Prehistory – 1500 CE)  
41. Transformation / Change Mechanism (Prehistory – 1500 CE)  
42. Resource Management (Prehistory – 1800 BCE)  
43. Probability / Likelihood (Prehistory – 1500 CE)  
44. Causation / Mechanism (Prehistory – 1500–1600 CE)  
45. Pattern / Regularity (Prehistory – 1000 BCE)  
46. Symmetry / Balance (Prehistory – 1000 BCE)  
47. Signal / Meaning (Prehistory – 1500 CE)  
48. Interpretation / Understanding (Prehistory – 1500 CE)  
49. Observation / Measurement (Prehistory – 1000 BCE)  
50. Resource / Material (Prehistory – 3000 BCE)  
51. Limitation / Deficiency (Prehistory – 3000 BCE)  
52. Transformation Mechanism / Method (Prehistory – 1500 CE)  
53. Comparison Attribute / Metric (Prehistory – 3000 BCE)  
54. Adaptation / Adjustment (Prehistory – 1500 CE)  
55. Temporal Relation / Sequence (Prehistory – 3000 BCE)  
56. Flow / Movement (Prehistory – 3000 BCE)  
57. Evaluation / Judgment (Prehistory – 600 BCE)  
58. Quantification / Measurement (Prehistory – 3000 BCE)  
59. Categorization / Classification (Prehistory – 1000 BCE)  
60. Existential Quantification / Scope (Prehistory – 600 BCE)  
61. Probability Assessment / Forecast (Prehistory – 1500 CE)  
62. Pattern Recognition / Detection (Prehistory – 1500 CE)  
63. Error Detection / Anomaly Recognition (Prehistory – 1500 CE)  
64. Logical Relation / Inference (Prehistory – 1500 BCE)  
65. Hierarchy / Ordering (Prehistory – 1000 BCE)  
66. Representation / Symbol (Prehistory – 3000 BCE)  
67. Reference / Aboutness (Prehistory – 600 BCE)  
68. Association / Linkage (Prehistory – 1000 BCE)  
69. Constraint Satisfaction (Prehistory – 1500 CE)  
70. Context / Framing (Prehistory – 600 BCE)  
71. Agency / Actorhood (Prehistory – 600 BCE)  
72. Norm / Expectation (Prehistory – 600 BCE)  
73. Recursion / Self-Reference (Prehistory – 1500 CE)  
74. Default / Assumption (Prehistory – 1500 CE)  
75. Counterfactual / Alternative World (Prehistory – 1500 CE)  
76. Obligation / Requirement (Prehistory – 1500 CE)  
77. Value / Worth (Prehistory – 1500 CE)  
78. Trade-off / Cost (Prehistory – 1500 CE)  
79. Irgom — placeholder for future concept  
80. Threshold / Phase Change (Prehistory – 1500 CE)  
81. Representation / Symbolic Stand-in (Prehistory – 3000 BCE)  
82. Knowledge / Justified Truth (Prehistory – 1500 CE)  
83. Commitment / Binding Intent (Prehistory – 1500 CE)  
84. Correction / Error Repair (Prehistory – 1500 CE)  
85. Stability / Equilibrium (Prehistory – 1500 CE)  
86. Belief / Assumed Truth (Prehistory – 600 BCE)  
87. Disagreement / Conflict (Prehistory – 600 BCE)  
88. Alignment / Agreement (Prehistory – 600 BCE)  
89. Compression / Abstraction Gain (Prehistory – 1500 CE)  
90. Termination / Closure (Prehistory – 1500 CE)  
91. Zero / Null (Prehistory – 300–500 CE)  
92. One / First Distinction (Prehistory – 3000 BCE)  
93. Mogri / Undifferentiated Potential (Prehistory – Present 2025)  
94. Observer / Agent (Prehistory – 1500 CE)  
95. Noise / Signal Split (Prehistory – 1500 CE)  
96. Default / Assumption (Prehistory – 1500 CE)  
97. Counterfactual / Alternative Scenario (Prehistory – 1500 CE)  
98. Boundary / Limit (Prehistory – 3000 BCE)  
99. Perspective / Point of View (Prehistory – 600 BCE)  
100. Alignment / Agreement (Prehistory – 1500 CE)  
101. Factual / Reality (Prehistory – 1800–1900 CE)  
102. Causation / Mechanism (Prehistory – 1500–1600 CE)  
103. Resource / Capacity (Prehistory – 1800–1900 CE)  
104. Process Termination (Prehistory – 1500–1600 CE)  
105. Deviation / Error (Prehistory – 1500–1600 CE)

---

*Notes:*  

- The numbering preserves the original 1–105 scheme.  
- Dates are approximate “in-use” (cognitive emergence) and “recognised” (first formal naming or systemisation).  
- Mogri (93) is treated as the foundational container for all other primitives.  
- This format is ready for GitHub Markdown — headings, numbered lists, and parenthetical notes.  




---

Expanded list with examples 

# 105 Linguistic Primitives (3-Line Format)

Preserves original numbering, definitions, examples, and approximate in-use vs recognised dates.

---

## Primitives 1–35

1. Existence / Being (Prehistory – always)  
Definition: The fact of something being, existing, or present.  
Examples: a rock exists, life exists, a thought occurs  

2. Identity / Name (Prehistory – always)  
Definition: The distinguishing label or recognition of a thing as itself.  
Examples: “Socrates” refers to a person, “Tree” identifies a plant  

3. Action / Event (Prehistory – always)  
Definition: Something that occurs or is performed over time.  
Examples: running, falling, shouting  

4. Property / Attribute (Prehistory – always)  
Definition: A characteristic, quality, or feature of something.  
Examples: red color, hardness, sweetness  

5. Quantity / Number (Prehistory – ~3000 BCE)  
Definition: The amount, count, or measure of items or concepts.  
Examples: three apples, five minutes, two thoughts  

6. Space / Location (Prehistory – always)  
Definition: The position or area occupied by something.  
Examples: on the table, under the bridge, at home  

7. Time / Temporal Relation (Prehistory – always)  
Definition: The ordering or duration of events.  
Examples: before sunrise, after lunch, two hours ago  

8. Causality / Mechanism (Prehistory – 600 BCE)  
Definition: The relationship or process by which one event produces another.  
Examples: gravity causes objects to fall, training improves skill  

9. Comparison / Relation (Prehistory – 600 BCE)  
Definition: The assessment of similarity, difference, or connection between things.  
Examples: taller than, faster than, part of  

10. Negation / Absence (Prehistory – always)  
Definition: The state of something not being or lacking.  
Examples: no water, nothing happened, absence of light  

11. Direction / Orientation (Prehistory – always)  
Definition: The alignment or path relative to reference points.  
Examples: north, left, toward the door  

12. Possession / Ownership (Prehistory – 1000 BCE)  
Definition: The relation of having or controlling something.  
Examples: my book, her car, their house  

13. Communication / Signal (Prehistory – ~5000 BCE)  
Definition: The transmission of information or intention between entities.  
Examples: gestures, words, smoke signals  

14. Modality / Capability (Prehistory – 1000 BCE)  
Definition: The potential or ability of an entity to act or be acted upon.  
Examples: can swim, might rain, able to lift  

15. Emotion / Feeling (Prehistory – always)  
Definition: Internal affective states experienced by a being.  
Examples: happiness, fear, surprise  

16. Identity / Role (Prehistory – always)  
Definition: The function, position, or expected behavior of an entity.  
Examples: teacher, parent, predator  

17. Intention / Desire (Prehistory – ~5000 BCE)  
Definition: A motivating state that drives action or thought.  
Examples: wants food, aims to escape, intends to help  

18. Aggregation / Grouping (Prehistory – 1000 BCE)  
Definition: The collection or assembly of items as a unit.  
Examples: herd of cattle, pile of stones, team  

19. Boundary / Limit (Prehistory – 600 BCE)  
Definition: The edge, extent, or restriction of an entity or area.  
Examples: fence line, maximum speed, personal space  

20. Existence / Presence (Prehistory – 1000 BCE)  
Definition: The state of being observable or manifest.  
Examples: someone is here, a sound is heard, a light shines  

21. Change / Transformation (Prehistory – always)  
Definition: The process of becoming different in form, state, or nature.  
Examples: ice melts, leaves turn color, ideas evolve  

22. Identity / Class (Prehistory – ~1000 BCE)  
Definition: Membership of an entity in a category or type.  
Examples: dog is an animal, oak is a tree, prime number  

23. Sequence / Order (Prehistory – 1000 BCE)  
Definition: Arrangement of events or items in a specific progression.  
Examples: sunrise before sunset, first, second, third  

24. Measurement / Magnitude (Prehistory – 3000 BCE)  
Definition: The determination of size, amount, or degree.  
Examples: three meters, five liters, ten kilograms  

25. Comparison Value / Benchmark (Prehistory – 3000 BCE)  
Definition: A standard used to assess or contrast items.  
Examples: taller than average, hotter than yesterday, better score  

26. Attribute Relationship / Correlation (Prehistory – 1000 BCE)  
Definition: The connection between properties or features of entities.  
Examples: more sunlight → faster growth, heavier → slower movement  

27. Persistence / Continuity (Prehistory – ~1000 BCE)  
Definition: The state of lasting over time or remaining stable.  
Examples: river flows continuously, tradition persists, memory endures  

28. Separation / Distinction (Prehistory – 1000 BCE)  
Definition: The recognition of entities as different or distinct.  
Examples: apple vs orange, day vs night, self vs other  

29. Scale / Proportion (Prehistory – 1000 BCE)  
Definition: Relative size or ratio of entities or measures.  
Examples: small compared to large, half of total, double speed  

30. Connection / Network (Prehistory – 1000 BCE)  
Definition: The linkage or interrelation among entities.  
Examples: roads connecting towns, friendships, power grid  

31. Change Rate / Dynamics (Prehistory – ~1000 BCE)  
Definition: The speed or intensity of a change in state or process.  
Examples: acceleration, population growth, melting rate  

32. Potential / Latent State (Prehistory – always)  
Definition: A capability or tendency that is not yet actualized.  
Examples: seed can grow, ice can melt, plan may succeed  

33. Observation / Detection (Prehistory – 1000 BCE)  
Definition: The act of perceiving or noticing phenomena.  
Examples: seeing a bird, detecting heat, hearing a sound  

34. Cause / Effect (Prehistory – 600 BCE)  
Definition: A relationship where one event produces another.  
Examples: striking a match → fire, exercise → fatigue, rain → wet ground  

35. Possibility / Contingency (Prehistory – 1000 BCE)  
Definition: A state in which an event may or may not occur.  
Examples: might rain, could win, potential path exists

## Primitives 36–70

36. Constraint / Limitation (Prehistory – 1500 CE)  
Definition: A restriction or rule that bounds actions or states.  
Examples: maximum weight, limited resources, legal requirements  

37. Threshold / Critical Point (Prehistory – 1500 CE)  
Definition: The level or condition at which a change or effect occurs.  
Examples: boiling point, tipping point, minimum speed  

38. Error / Anomaly (Prehistory – 1500 CE)  
Definition: A deviation from expectation or normal function.  
Examples: miscalculation, machine malfunction, unusual behavior  

39. Correction / Adjustment (Prehistory – 1500 CE)  
Definition: An action that rectifies an error or adapts a process.  
Examples: fixing a typo, recalibrating equipment, adjusting plan  

40. Process / Procedure (Prehistory – 1500 CE)  
Definition: A series of steps or operations to achieve a result.  
Examples: baking bread, scientific experiment, assembly line  

41. Transformation / Change Mechanism (Prehistory – 1500 CE)  
Definition: The method or process by which a state or entity is altered.  
Examples: evaporation, cooking, learning  

42. Resource Management (Prehistory – 1800 BCE)  
Definition: The allocation and use of materials, energy, or effort.  
Examples: rationing food, scheduling labor, using fuel efficiently  

43. Probability / Likelihood (Prehistory – 1500 CE)  
Definition: The chance or expectation that an event will occur.  
Examples: coin flip probability, weather forecast, disease risk  

44. Causation / Mechanism (Prehistory – 1500–1600 CE)  
Definition: The underlying process or reason something produces an effect.  
Examples: gravity causes objects to fall, enzymes catalyze reactions  

45. Pattern / Regularity (Prehistory – 1000 BCE)  
Definition: A repeated or predictable arrangement of elements.  
Examples: stripes on animals, rhythm in music, weekly routines  

46. Symmetry / Balance (Prehistory – 1000 BCE)  
Definition: Correspondence or harmony between parts of a system.  
Examples: bilateral symmetry in humans, balanced equations, balanced design  

47. Signal / Meaning (Prehistory – 1500 CE)  
Definition: Information carried by a stimulus or communication.  
Examples: smoke signals, traffic lights, spoken language  

48. Interpretation / Understanding (Prehistory – 1500 CE)  
Definition: The cognitive process of making sense of signals or events.  
Examples: reading a text, solving a puzzle, predicting outcomes  

49. Observation / Measurement (Prehistory – 1000 BCE)  
Definition: The act of quantifying or recording phenomena.  
Examples: measuring temperature, weighing objects, counting steps  

50. Resource / Material (Prehistory – 3000 BCE)  
Definition: Physical or conceptual elements used to achieve a goal.  
Examples: wood for building, water for drinking, ideas for planning  

51. Limitation / Deficiency (Prehistory – 3000 BCE)  
Definition: The state of being insufficient or constrained.  
Examples: low fuel, lack of tools, limited attention  

52. Transformation Mechanism / Method (Prehistory – 1500 CE)  
Definition: Specific method or procedure causing change.  
Examples: heating water → steam, training → skill improvement  

53. Comparison Attribute / Metric (Prehistory – 3000 BCE)  
Definition: A measurable feature used for evaluation.  
Examples: height, weight, temperature  

54. Adaptation / Adjustment (Prehistory – 1500 CE)  
Definition: The process of modifying behavior or system to fit conditions.  
Examples: wearing warm clothes, adjusting strategy, evolving traits  

55. Temporal Relation / Sequence (Prehistory – 3000 BCE)  
Definition: The order or timing relationship between events.  
Examples: sunrise before noon, first then second, yesterday then today  

56. Flow / Movement (Prehistory – 3000 BCE)  
Definition: Change in position, state, or activity over time.  
Examples: river flow, traffic, wind  

57. Evaluation / Judgment (Prehistory – 600 BCE)  
Definition: Assessing value, correctness, or quality.  
Examples: grading a test, judging art, ranking priorities  

58. Quantification / Measurement (Prehistory – 3000 BCE)  
Definition: Assigning a numerical or proportional value to a property.  
Examples: 5 liters, 3 meters, 2 apples  

59. Categorization / Classification (Prehistory – 1000 BCE)  
Definition: Grouping entities based on shared features.  
Examples: mammals, fruits, prime numbers  

60. Existential Quantification / Scope (Prehistory – 600 BCE)  
Definition: The application of statements or properties to sets or all members.  
Examples: “all humans are mortal”, “some birds fly”  

61. Probability Assessment / Forecast (Prehistory – 1500 CE)  
Definition: Estimating the likelihood of future events.  
Examples: weather prediction, betting odds, risk assessment  

62. Pattern Recognition / Detection (Prehistory – 1500 CE)  
Definition: Identifying recurring structures or signals.  
Examples: spotting camo, music rhythm, traffic patterns  

63. Error Detection / Anomaly Recognition (Prehistory – 1500 CE)  
Definition: Noticing deviations from expected patterns.  
Examples: faulty calculation, unusual heartbeat, broken machine  

64. Logical Relation / Inference (Prehistory – 1500 BCE)  
Definition: Deduction or reasoning based on relationships between statements.  
Examples: syllogism, if-then reasoning, rule-based deduction  

65. Hierarchy / Ordering (Prehistory – 1000 BCE)  
Definition: Organization of elements by rank, level, or importance.  
Examples: family tree, corporate structure, taxonomic classification  

66. Representation / Symbol (Prehistory – 3000 BCE)  
Definition: A sign or entity that stands for something else.  
Examples: letters, icons, maps  

67. Reference / Aboutness (Prehistory – 600 BCE)  
Definition: The property of pointing to or denoting something.  
Examples: pronouns, labels, indexical signs  

68. Association / Linkage (Prehistory – 1000 BCE)  
Definition: A cognitive or causal connection between entities.  
Examples: thunder → rain, peanut → allergy, friendship networks  

69. Constraint Satisfaction (Prehistory – 1500 CE)  
Definition: Achieving outcomes within imposed restrictions.  
Examples: puzzle solving, scheduling tasks, resource allocation  

70. Context / Framing (Prehistory – 600 BCE)  
Definition: The circumstances or background that shape meaning.  
Examples: “bank” in river vs finance context, historical background

## Primitives 71–105

71. Agency / Actorhood (Prehistory – 600 BCE)  
Definition: The capacity of an entity to act or exert influence.  
Examples: person makes a decision, animal hunts, machine operates  

72. Norm / Expectation (Prehistory – 600 BCE)  
Definition: A standard or rule guiding behavior or outcomes.  
Examples: social etiquette, traffic rules, moral codes  

73. Recursion / Self-Reference (Prehistory – 1500 CE)  
Definition: A process or structure that refers back to itself.  
Examples: nested functions, “this sentence is false”, fractals  

74. Default / Assumption (Prehistory – 1500 CE)  
Definition: A presumed state or value in the absence of contrary evidence.  
Examples: blank forms default to zero, assumed neutrality, unstated intentions  

75. Counterfactual / Alternative World (Prehistory – 1500 CE)  
Definition: A hypothetical scenario differing from actual events.  
Examples: “If I had left earlier, I would have caught the train”, parallel worlds  

76. Obligation / Requirement (Prehistory – 1500 CE)  
Definition: A duty or necessity imposed on an entity or process.  
Examples: paying taxes, following instructions, contractual terms  

77. Value / Worth (Prehistory – 1500 CE)  
Definition: The significance, utility, or importance of something.  
Examples: money, moral good, sentimental keepsake  

78. Trade-off / Cost (Prehistory – 1500 CE)  
Definition: The balance or compromise between competing factors.  
Examples: speed vs safety, cost vs quality, effort vs reward  

79. Irgom — placeholder for future concept  
Definition: If a new primative is needed, this is the place for it.  
Examples: “new prime a,new prime b”

80. Threshold / Phase Change (Prehistory – 1500 CE)  
Definition: The point at which a qualitative change occurs.  
Examples: water freezes at 0°C, critical mass in nuclear reactions  

81. Representation / Symbolic Stand-in (Prehistory – 3000 BCE)  
Definition: An entity or sign that stands in for another thing, idea, or concept.  
Examples: letters, icons, maps 

82. Knowledge / Justified Truth (Prehistory – 1500 CE)  
Definition: Information that is both true and supported by evidence.  
Examples: scientific laws, historical facts, proven theorems  

83. Commitment / Binding Intent (Prehistory – 1500 CE)  
Definition: A resolved intention or dedication to act.  
Examples: signing a contract, promise keeping, long-term plan  

84. Correction / Error Repair (Prehistory – 1500 CE)  
Definition: The act of rectifying deviations or mistakes.  
Examples: proofreading, debugging, adjusting strategy  

85. Stability / Equilibrium (Prehistory – 1500 CE)  
Definition: A state of balance or resistance to change.  
Examples: chemical equilibrium, social stability, standing posture  

86. Belief / Assumed Truth (Prehistory – 600 BCE)  
Definition: Acceptance of a proposition as true without full proof.  
Examples: religious belief, superstition, confidence in a friend  

87. Disagreement / Conflict (Prehistory – 600 BCE)  
Definition: The presence of opposing views or forces.  
Examples: argument, war, scientific debate  

88. Alignment / Agreement (Prehistory – 600 BCE)  
Definition: Coordination or harmony between entities or ideas.  
Examples: synchronized swimming, legal consensus, shared goals  

89. Compression / Abstraction Gain (Prehistory – 1500 CE)  
Definition: The reduction of complexity while retaining meaning.  
Examples: shorthand, data compression, conceptual models  

90. Termination / Closure (Prehistory – 1500 CE)  
Definition: The end of a process or the completion of an event.  
Examples: project finish, death, sunset  

91. Zero / Null (Prehistory – 300–500 CE)  
Definition: The representation of nothingness or absence.  
Examples: 0 in counting, empty set, null pointer  

92. One / First Distinction (Prehistory – 3000 BCE)  
Definition: The initial unit or singular entity distinguished from none.  
Examples: 1 apple, first element, single event  

93. Mogri / Undifferentiated Potential (Prehistory – Present 2025)  
Definition: The foundational proto-cognitive substrate that underlies all distinctions.  
Examples: raw thought potential, pre-conceptual awareness, cognitive blank slate  

94. Observer / Agent (Prehistory – 1500 CE)  
Definition: An entity capable of perceiving or acting.  
Examples: person noticing events, AI analyzing data, animal hunting  

95. Noise / Signal Split (Prehistory – 1500 CE)  
Definition: Distinguishing meaningful information from irrelevant data.  
Examples: filtering background static, detecting trends in data, focusing attention  

96. Default / Assumption (Prehistory – 1500 CE)  
Definition: Presumed state or value when information is incomplete.  
Examples: empty form fields, assumed neutrality, implicit rules  

97. Counterfactual / Alternative Scenario (Prehistory – 1500 CE)  
Definition: Hypothetical situations differing from reality.  
Examples: “If it had rained, crops would grow”, alternate decisions  

98. Boundary / Limit (Prehistory – 3000 BCE)  
Definition: The edge, restriction, or extent of an entity or system.  
Examples: fence, maximum speed, personal space  

99. Perspective / Point of View (Prehistory – 600 BCE)  
Definition: The angle or context from which observation or reasoning occurs.  
Examples: eyewitness view, cultural lens, camera angle  

100. Alignment / Agreement (Prehistory – 1500 CE)  
Definition: Coordination or harmonization of actions or ideas.  
Examples: synchronized efforts, legal consensus, shared goals  

101. Factual / Reality (Prehistory – 1800–1900 CE)  
Definition: The state of being actual, true, or occurring.  
Examples: water boils at 100°C, Earth is round  

102. Causation / Mechanism (Prehistory – 1500–1600 CE)  
Definition: The relationship or process by which one event produces another.  
Examples: gravity causes falling, enzymes catalyze reactions, training improves skill  

103. Resource / Capacity (Prehistory – 1800–1900 CE)  
Definition: The usable potential or supply of something.  
Examples: energy in a battery, human labor, available memory  

104. Process Termination (Prehistory – 1500–1600 CE)  
Definition: The completion or end of a sequence or activity.  
Examples: project finished, machine stopped, lesson concluded  

105. Deviation / Error (Prehistory – 1500–1600 CE)  
Definition: The difference between expected and observed states.  
Examples: miscalculation, measurement error, behavior anomaly


---

## Notes

1. **Numbering and format**  
   - Original primitive numbers (1–105) are preserved for reference and historical tracking.  
   - Each primitive is listed in a 3-line format: name/descriptor, definition, examples.

2. **Dates (in-use vs recognised)**  
   - Dates in parentheses indicate approximate cognitive *in-use* period (when humans likely used or understood the concept) and first formal *recognition* (when the primitive was explicitly named or systematised).  
   - Dates are rough estimates and intended as illustrative, not definitive.

3. **Mogri (Primitive 93)**  
   - Mogri represents the **foundational cognitive container** for all other primitives.  
   - It is *not* a derivative primitive and cannot be constructed from other primitives.  
   - Consider it a **conceptual runtime environment** rather than a specific entity.

4. **Gaps and Reserved Numbers**  
   - Some numbers were reserved or missing in the original source (e.g., 13, 14, 17, 81).  
   - These can be filled with new primitives as research or modeling expands.

5. **Conceptual Use**  
   - This list is primarily a **modeling tool** for cognition, AI, and formal reasoning.  
   - The primitives are **formal conveniences**, not absolute metaphysical assertions.  
   - Users are encouraged to adopt, modify, or omit primitives based on context.

6. **Examples**  
   - Examples are illustrative and do not exhaust all possible instances.  
   - They are intended to aid understanding rather than prescribe usage.

7. **Cross-References**  
   - Some primitives are conceptually related or overlapping (e.g., 8: Causality / Mechanism vs 102: Causation / Mechanism).  
   - Such overlaps reflect historical evolution and refinement of concepts.

8. **Extensions**  
   - Additional primitives, subcategories, or meta-primitives may be appended in future versions.  
   - Reserved numbers or new discoveries can be incorporated without disrupting numbering.

9. **Usage Guidance**  
   - Ideal for AI modeling, cognitive frameworks, formal reasoning exercises, and educational tools.  
   - The list is **neutral and non-dogmatic**, suitable for interdisciplinary application.

10. **Attribution**  
    - This compilation synthesizes historical, philosophical, and cognitive sources.  
    - Dates, examples, and interpretations are **estimations** to facilitate modeling and understanding.














