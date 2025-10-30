# Integrated Assessment Risk Framework

A web-based tool for analysing the security risks of online assessments in the age of AI agents. This framework helps educators and institutions make informed decisions about assessment design by combining vulnerability analysis with contextual risk factors.

**Live Tool:** https://auralsculpture.github.io/assessment-risk-tool/

## Purpose

This tool addresses a critical challenge in higher education: **if you cannot verify authorship, you cannot assign grades**. With AI agents now capable of completing most traditional assessment tasks, institutions need systematic approaches to evaluate which assessments can remain secure online versus which require face-to-face verification.

The framework emerged from research into assessment reform in Australian higher education, particularly work with TEQSA (Tertiary Education Quality and Standards Agency) on maintaining academic integrity standards.

## How It Works

### Four-Step Process

**1. Select Assessment Type** (23 types available)
- Choose from essays, code assignments, creative portfolios, case studies, and more
- Each type has been analysed for inherent AI vulnerabilities

**2. Review Dual-Layer Analysis**
- **Primary Vulnerability**: How AI completes the assessment itself
- **Mitigation Risk**: How AI defeats typical security measures
- **Base Risk Level**: Inherent security risk of this assessment type

**3. Apply Contextual Factors** (6 weighted factors)
- Cohort size and anonymity
- Mixed online/on-campus delivery constraints
- Camera-off rates and legitimacy
- Student technical capability
- Stakes level
- Engagement requirements

**4. Get Final Risk Assessment**
- Combined base + contextual risk
- Specific modification recommendations
- Alternative assessment suggestions
- Risk level: LOW → MODERATE → MODERATE-HIGH → HIGH → CRITICAL

## Key Principles

### The Dual-Layer Framework

Traditional approaches only consider "Can AI do this assessment?" This framework asks two critical questions:

1. **How does AI complete the assessment task?**
   - Text generation, code writing, image creation, analysis, etc.

2. **How does AI defeat the mitigation strategies?**
   - Second screens invisible to proctoring
   - Audio assistance via earpiece
   - Real-time response feeding during oral defences
   - Cannot verify what's happening off-camera

This dual analysis reveals that many "mitigated" assessments remain critically vulnerable online.

### Risk Adjustment Logic

- **Base Risk** comes from the assessment type's inherent vulnerability
- **Contextual Risk** comes from your specific situation (cohort size, stakes, technical capability, etc.)
- **Final Risk** is the adjusted assessment based on both factors

Example: An essay (CRITICAL base risk) in a small cohort (30 students) with cameras enforced might adjust to HIGH. The same essay in a 500-student cohort with cameras optional remains CRITICAL.

## Understanding Risk Levels

### CRITICAL Risk
- Cannot drop below HIGH even with best contextual factors
- Primary vulnerabilities cannot be secured online with grading
- **Recommendation**: Face-to-face verification required OR convert to Pass/Fail OR use for ungraded learning only

### HIGH Risk
- Significant security concerns
- Can adjust to MODERATE-HIGH or CRITICAL based on context
- **Recommendation**: Substantial modifications needed or consider alternatives

### MODERATE-HIGH Risk
- Notable vulnerabilities but some mitigation possible
- Can adjust to MODERATE or HIGH
- **Recommendation**: Strong contextual controls and enhanced verification

### MODERATE Risk
- Manageable with proper controls
- Can drop to LOW with good contextual factors
- **Recommendation**: Standard security measures likely sufficient

### LOW Risk
- Minimal security concerns in most contexts
- Generally secure for online delivery with grading

## The 23 Assessment Types Analysed

### Critical Base Risk
- Essays, Reports, Written Analysis
- Creative Reflections, Artist Statements
- Case Study Analysis
- Data Analysis/Interpretation
- Design Brief Response
- Time-Constrained Written Exams (online)
- Portfolio + Interview (Creative Admissions)

### High Base Risk
- Creative Portfolios (Design, Visual Arts)
- Music Compositions
- Code/Programming Assignments
- Multiple Choice/Short Answer Exams
- Collaborative Group Projects
- Critical Literature Review
- Research Proposals
- Professional Workplace Simulations
- Peer Teaching/Presentations

### Moderate-High Base Risk
- Problem-Solving Tasks (Maths, Science)
- Practical Skills Demonstration (recorded)
- Annotated Bibliographies

### Moderate Base Risk
- Reflective Journals/Learning Logs

## The Six Contextual Factors

### 1. Cohort Anonymity vs. Accountability
Social accountability is a deterrent. Students are less likely to deceive someone who knows them personally.
- Small (<30): Staff know students by name
- Medium (30-100): Staff recognize most students
- Large (>100): Students largely anonymous
- Massive (>300): Completely anonymous

### 2. Mixed Cohort Constraints
If online and on-campus students must use identical assessments for equity, security options are limited.
- Separate cohorts: Can use different methods
- Mixed: Can justify different methods
- Mixed: Must use identical assessment

### 3. Camera-Off Rate × Legitimacy
What proportion habitually have cameras off, and why?
- Rate: <20% to >60%
- Legitimacy: Predominantly safety/privacy vs. No policy requirement

This creates opportunity but may be legitimate (privacy, safety, bandwidth issues).

### 4. Technical Capability
Do students have skills to circumvent mitigations?
- Low: Non-technical disciplines
- Medium: Some technical content
- High: Technical disciplines (IT, Engineering)
- Critical: Cybersecurity, hacking culture

### 5. Stakes Level
Higher stakes = higher motivation to circumvent.
- Low: Formative or ≤15% of grade
- Medium: 15-30% of grade
- High: 30-50% of grade
- Critical: >50% or pass/fail gate

### 6. Engagement Hurdles (Multiplier)
Can you require camera-on for assessment activities?
- Strong: Can enforce camera-on (×0.5 to risk score)
- Weak: Can request but not enforce (×0.75)
- None: Cannot require camera-on (×1.0)

## Risk Calculation

```
Contextual Risk Score = (F1 + F2 + (F3_rate × F3_legitimacy) + F4 + F5) × F6

Score 0-5: LOW contextual risk
Score 6-10: MEDIUM contextual risk
Score 11-15: HIGH contextual risk
Score 16+: CRITICAL contextual risk
```

The final risk level combines base risk with contextual risk, with CRITICAL base risks unable to drop below HIGH regardless of context.

## Important Limitations

### This is an Interim Framework
This tool is designed for a **2-3 year transition period** while comprehensive assessment redesign occurs. It distinguishes between:
- **Opportunistic AI use** (88-92% in unsecured contexts) - documented
- **Deliberate security circumvention** (unknown prevalence) - requires empirical research

### What This Framework Cannot Do
- Eliminate all risk (fundamental paradigm shift required)
- Verify authorship in fully online contexts for high-risk assessments
- Replace professional judgement about institutional risk tolerance
- Guarantee any online assessment against determined circumvention

### What This Framework Can Do
- Identify which assessments have highest vulnerability
- Quantify how contextual factors affect risk
- Provide evidence-based recommendations
- Support risk-informed decision making
- Help institutions allocate resources appropriately

## Use Cases

### For Assessment Designers
- Evaluate security of current assessment designs
- Make informed decisions about online vs. face-to-face delivery
- Identify specific modifications that reduce risk
- Find alternative assessment types with lower vulnerability

### For Course Coordinators
- Assess entire assessment schedules
- Balance developmental vs. summative assessment appropriately
- Justify assessment design decisions to leadership
- Plan resource allocation for secure assessment delivery

### For Academic Leadership
- Develop evidence-based assessment policies
- Understand institutional risk exposure
- Make informed decisions about online program delivery
- Support curriculum development with clear risk frameworks

### For Compliance Officers
- Demonstrate systematic approach to academic integrity
- Document risk assessment processes
- Support TEQSA or equivalent regulatory requirements
- Provide evidence for quality assurance

## Technical Details

### Built With
- React 18.3.1
- Tailwind CSS
- Lucide React (icons)
- Vite (build tool)

### Browser Compatibility
Modern browsers with JavaScript enabled (Chrome, Firefox, Safari, Edge)

### Hosting
Static site hosted on GitHub Pages. No backend required, no data collection.

## Research Background

This framework operationalizes research from the Assessment Reform in Higher Education project, specifically:
- The Context-Standard-Range (CSR) Framework
- Dual-layer susceptibility analysis
- The "preparation paradox" in online assessment
- TEQSA regulatory compliance considerations

### Key Research Insights
1. **Paradigm Shift**: AI has moved from homework assistant to autonomous agent capable of full participation in learning communities
2. **Mitigation Vulnerability**: Most traditional "mitigations" (proctoring, time pressure, oral defence) are defeatable online
3. **Behaviour vs. Policy**: Students will use AI based on actual behaviour patterns, not policy restrictions
4. **Fundamental Contradiction**: Cannot verify authorship remotely while maintaining accessibility

## Citation

If you use this framework in academic work, research, or institutional policy:

> Webber, C. (2025). *Integrated Assessment Risk Framework*. https://github.com/Auralsculpture/assessment-risk-tool

## License

This tool is provided for educational and institutional use. Feel free to use, modify, and share with attribution.

## Contact & Feedback

This framework is under active development. Feedback, suggestions, and institutional experiences are welcome.

**Repository:** https://github.com/Auralsculpture/assessment-risk-tool

---

## Acknowledgments

Developed through collaboration with:
- TEQSA (Tertiary Education Quality and Standards Agency)
- SAE University College
- Australian higher education institutions working on AI-era assessment reform

This work builds on extensive literature review and sector consultation regarding academic integrity in the age of generative AI.

---

**Version:** 1.0.0  
**Last Updated:** October 2025  
**Status:** Production - Active Development
