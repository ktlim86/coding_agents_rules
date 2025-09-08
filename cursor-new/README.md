# Agile Software Development Lifecycle Rules

## Overview
This directory contains the restructured cursor rules organized according to the 7-phase agile software development lifecycle. All rules follow MVP principles and emphasize evidence-based development, testing, and continuous improvement.

## Directory Structure

```
.cursor/review/
├── README.md                           # This file
├── master-rules.mdc                    # Master rules with lifecycle overview
├── root-cause-analysis.mdc             # Cross-phase root cause analysis & troubleshooting
├── date-commands.mdc                   # Centralized date/time commands reference
├── po-demo.mdc                         # Product Owner demonstration requirements
├── conceptualization/                  # Phase 1: Conceptualization
│   └── requirements-gathering.mdc      # Requirements gathering and story card creation
├── designing/                          # Phase 2: Designing
│   └── system-architecture.mdc        # System architecture and design
├── planning/                           # Phase 3: Planning
│   ├── story-card-creation.mdc        # Story card structure and management
│   ├── estimation.mdc                 # Story estimation and sizing
│   └── backlog-management.mdc         # Backlog management and feature planning
├── development/                        # Phase 4: Development
│   ├── engineering-principles.mdc     # Software engineering principles
│   ├── logging.mdc                    # User experience guidelines for logging
│   └── spike.mdc                      # SPIKE process for uncertainty and ambiguity
├── integration-testing/                # Phase 5: Integration and Testing
│   ├── evidence-based-testing.mdc     # Evidence-based testing strategy
│   └── test-case-templates.mdc        # Test case acceptance templates
├── release-deployment/                 # Phase 6: Release and Deployment
│   ├── deployment-strategy.mdc        # Deployment strategy and release management
│   └── documentation.mdc              # Post-deployment documentation requirements
└── review/                            # Phase 7: Review
    └── retrospectives.mdc             # Retrospectives and continuous improvement
```

## Lifecycle Phases

### 1. Conceptualization Phase
**Purpose**: Accept requirements from Product Owner and convert to story cards
**Key Rules**:
- `requirements-gathering.mdc` - Requirements gathering and story card creation

### 2. Designing Phase
**Purpose**: Create system architecture, user experience design, and technical specifications
**Key Rules**:
- `system-architecture.mdc` - System architecture and design

### 3. Planning Phase
**Purpose**: Break down work into manageable story cards, estimate effort, and prioritize
**Key Rules**:
- `story-card-creation.mdc` - Story card structure and management
- `estimation.mdc` - Story estimation and sizing
- `backlog-management.mdc` - Backlog management for future ideas and considerations

### 4. Development Phase
**Purpose**: Implement features following engineering principles and MVP approach
**Key Rules**:
- `engineering-principles.mdc` - Software engineering principles (DRY, SOLID, KISS, etc.)
- `logging.mdc` - User experience guidelines for logging and error messages
- `@root-cause-analysis.mdc` - Cross-phase root cause analysis and troubleshooting
- `spike.mdc` - SPIKE process for uncertainty and ambiguity resolution

### 5. Integration and Testing Phase
**Purpose**: Comprehensive testing, integration validation, and quality assurance
**Key Rules**:
- `evidence-based-testing.mdc` - Evidence-based testing strategy
- `test-case-templates.mdc` - Test case acceptance templates

### 6. Release and Deployment Phase
**Purpose**: Deploy to production, monitor performance, and manage releases
**Key Rules**:
- `deployment-strategy.mdc` - Deployment strategy and release management
- `documentation.mdc` - Post-deployment documentation requirements

### 7. Review Phase
**Purpose**: Evaluate outcomes, gather feedback, and plan improvements
**Key Rules**:
- `retrospectives.mdc` - Retrospectives and continuous improvement

## Core Principles

### MVP Principles
- Focus on core functionality first
- Avoid over-engineering
- Test feasibility, desirability, and viability
- Iterative development and validation

### Software Engineering Principles
- **DRY**: Don't Repeat Yourself
- **SOLID**: Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion
- **KISS**: Keep It Simple, Stupid
- **YAGNI**: You Aren't Gonna Need It
- **Abstraction**: Hide complex implementation details
- **Modularity**: Independent, self-contained components
- **High Cohesion**: Elements work together for single purpose
- **Low Coupling**: Minimal dependencies between modules

### Testing Principles
- Evidence-based testing (no mocks unless justified)
- Test as close to production as possible
- Comprehensive test coverage (unit → integration → system)
- Real environment validation
- Screenshot evidence for UI testing
- Database validation for data operations

### Quality Assurance
- Definition of Done: All acceptance criteria met, tests pass, code review completed
- Product Owner approval required at key stages
- Comprehensive root cause analysis before troubleshooting
- SPIKE process for uncertainty/ambiguity
- Continuous improvement through self-reflection

## Usage Instructions

### For New Conversations
1. Review past conversation history
2. Review relevant rules for current context
3. Refer to appropriate phase-specific rules before starting tasks

### For Story Card Development
1. Use `@planning/story-card-creation.mdc` for story structure
2. Include start/end datetime (Singapore time) and duration
3. Map test cases to acceptance criteria
4. Require Product Owner approval before development

### For Development Process
1. Refer to `@development/engineering-principles.mdc` before coding
2. Follow TDD approach (tests first, then implementation)
3. Present implementation options with pros/cons
4. Get Product Owner confirmation before proceeding

### For Testing Process
1. Use `@integration-testing/evidence-based-testing.mdc` for test strategy
2. Provide evidence that software works (unit tests, integration tests, screenshots)
3. Validate external services with actual connectivity tests
4. No mock data unless absolutely necessary

### For Troubleshooting Process
1. Use `@root-cause-analysis.mdc` for comprehensive analysis
2. Use `@development/spike.mdc` for uncertainty and ambiguity
3. Present evidence-based analysis before proposing solutions
4. Get Product Owner approval before implementing fixes
5. Document lessons learned

## Key Features

### Story Card Management
- Comprehensive story card templates with acceptance criteria
- T-shirt sizing methodology (XS=1, S=3, M=5, MH=8, L=13, XL=21 points)
- Realistic duration estimates (S=2-5h, M=5-8h, MH=8-12h, L=1d, XL=2d)
- De-risking rule: Stories larger than 8 points must be broken down
- Status workflow: Not Started → Pending PO Approval → Dev In Progress → Testing In Progress → Pending PO Accepted → Done
- Start/end datetime tracking with duration calculation

### Evidence-Based Testing
- Real environment testing with minimal mocking
- Comprehensive test case templates for all test types
- Screenshot evidence for UI testing
- Database validation for data operations
- External service connectivity testing

### Root Cause Analysis
- Systematic 5 Whys analysis
- Fishbone diagram (Ishikawa) analysis
- Fault tree analysis
- Comprehensive evidence gathering
- Integration with SPIKE process for uncertainty/ambiguity

### Deployment Strategy
- Blue-green, canary, and rolling deployment strategies
- Comprehensive monitoring and alerting
- Automated rollback capabilities
- Infrastructure as Code (IaC) practices
- Security considerations and secrets management

### Continuous Improvement
- Regular retrospectives with multiple frameworks
- Action item tracking and management
- Metrics and KPIs for team performance
- Knowledge sharing and documentation
- Process optimization and enhancement

## Product Owner Engagement
- Always seek clarification when in doubt
- Present options with pros/cons analysis
- Require explicit approval before proceeding
- No assumptions without confirmation
- Regular status updates and demonstrations

## Self-Reflection Requirements
- Review actions on every story card
- Identify what was done well, what can be improved, what was not done well
- Document lessons learned for continuous improvement
- Address any issues that may have upset the Product Owner

## Environment Setup
- Use conda environment `platform` for Python development
- Verify environment before starting development
- Read requirements.txt and package.json for dependencies
- Never modify working code without explicit approval

## Migration from Existing Rules
The following existing rules have been migrated and reorganized:
- `story-card-structure.mdc` → `planning/story-card-creation.mdc`
- `t-shirt-sizing.mdc` → `planning/estimation.mdc`
- `development-workflow.mdc` → Integrated into `development/engineering-principles.mdc`
- `mvp-principles.mdc` → Integrated into `master-rules.mdc` and phase-specific rules
- `testing.mdc` → `integration-testing/evidence-based-testing.mdc`
- `debugging-troubleshooting.mdc` + `evidence-first-debugging.mdc` → `root-cause-analysis.mdc`
- `backlog-management.mdc` → `planning/story-card-creation.mdc`
- Other rules integrated into appropriate lifecycle phases

## Next Steps
1. Review all rules in this directory
2. Test the rules with actual development work
3. Provide feedback for improvements
4. Move approved rules to the main `.cursor/rules/` directory
5. Update team processes to align with new rule structure
