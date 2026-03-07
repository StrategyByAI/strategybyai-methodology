# Implementation: Strategic State Representation Prototype

## Building Subject-Specific Strategic World Models

This prototype defines the data architecture for a strategic world model instance. It models the state representation — the 34-document portfolio structure — as queryable Python classes.

**What this code is:** A schema defining how strategic state is structured, queried, and validated. It demonstrates the architecture that makes strategic world models possible.

**What this code is not:** The reasoning framework that populates these structures. To actually fill `Enemy.status` with a correct classification, you need Module Three's analytical framework. To calculate `Campaign.capacity_allocation`, you need Module Five's formulation logic. The code is the container; the methodology is the content.

**The methodology is available at [strategybyai.org](https://strategybyai.org).**

---

## Strategic State Classes

```python
"""
Strategy by AI — Strategic World Model State Representation
============================================================

This module defines the data architecture for subject-specific
strategic world models. Each class corresponds to a document or
document group in the 34-document portfolio.

The five state dimensions:
  1. IdentityState      (Documents 1–4)
  2. HostileEnvironment (Documents 5–13)
  3. SituationState     (Documents 14–20)
  4. StrategyState      (Documents 21–24)
  5. ExecutionState     (Documents 25–34)

Together they form a StrategicWorldModel — a queryable, updatable,
self-consistent representation of an organisation's competitive reality.
"""

from dataclasses import dataclass, field
from enum import Enum
from typing import Optional
from datetime import date


# ──────────────────────────────────────────────────────────────
# Enumerations — the methodology's classification taxonomies
# ──────────────────────────────────────────────────────────────

class FoeStatus(Enum):
    """Module Three Section 3.2: Four-level threat taxonomy."""
    ALIEN = "alien"           # Latent, future threat
    RIVAL = "rival"           # Parallel competition, non-existential
    ADVERSARY = "adversary"   # Active confrontation, survivable
    ENEMY = "enemy"           # Existential, compromise impossible

class Trajectory(Enum):
    """Entity movement direction within the hierarchy."""
    ESCALATING = "escalating"
    STABLE = "stable"
    DE_ESCALATING = "de-escalating"

class Confidence(Enum):
    """Evidence confidence level for all assessments."""
    HIGH = "high"
    MEDIUM = "medium"
    LOW = "low"

class ExecutionRating(Enum):
    """Module Six: execution dimension assessment scale."""
    EXEMPLARY = "exemplary"
    ADEQUATE = "adequate"
    MARGINAL = "marginal"
    DEFICIENT = "deficient"

class OverallGrade(Enum):
    """Module Six Section 6.12: final assessment grades."""
    A = "A"   # Exemplary execution
    B = "B"   # Adequate execution
    C = "C"   # Mixed execution
    D = "D"   # Operations attempted and failed
    F = "F"   # Operations absent — strategy collapsed before execution

class DecisionTier(Enum):
    """Module Six: AI-human authority distribution."""
    TIER_1 = 1   # War-level: human decides, AI analyses
    TIER_2 = 2   # Operational: AI proposes, human approves
    TIER_3 = 3   # Tactical: AI executes within parameters


# ──────────────────────────────────────────────────────────────
# Dimension 1: Identity State (Documents 1–4)
# ──────────────────────────────────────────────────────────────

@dataclass
class StrategicMission:
    """Document 1: what the organisation exists to do."""
    primary: str                         # Core mission statement
    secondary: list[str] = field(default_factory=list)
    constraints: list[str] = field(default_factory=list)
    foreclosed_options: list[str] = field(default_factory=list)

@dataclass
class StrategicDoctrine:
    """Document 3: principles governing organisational behaviour."""
    explicit_doctrines: list[str] = field(default_factory=list)
    implicit_doctrines: list[str] = field(default_factory=list)
    contradictions: list[str] = field(default_factory=list)
    has_explicit_doctrine: bool = False

@dataclass
class IdentityState:
    """Documents 1–4: complete identity dimension."""
    mission: StrategicMission
    doctrine: StrategicDoctrine
    heritage_years: int = 0
    coherence_rating: str = ""          # e.g., "FUNDAMENTAL INCOHERENCE"
    key_capabilities: list[str] = field(default_factory=list)
    capability_gaps: list[str] = field(default_factory=list)
    readiness_module_three: str = ""    # Quality gate rating
    readiness_module_four: str = ""
    readiness_module_five: str = ""


# ──────────────────────────────────────────────────────────────
# Dimension 2: Hostile Environment (Documents 5–13)
# ──────────────────────────────────────────────────────────────

@dataclass
class HostileEntity:
    """Single entity in the hostile environment."""
    name: str
    status: FoeStatus
    trajectory: Trajectory
    confidence: Confidence
    capacity_required_pct: float        # % of org capacity this entity demands
    capacity_allocated_pct: float       # % of org capacity currently allocated
    evidence_sources: list[str] = field(default_factory=list)
    mutation_timeline: str = ""         # When status may change
    intrinsic_hostility: str = ""       # Structural vs contingent

    @property
    def allocation_gap(self) -> float:
        """Positive = under-allocated. Negative = over-allocated."""
        return self.capacity_required_pct - self.capacity_allocated_pct

@dataclass
class HostileEnvironment:
    """Documents 5–13: complete hostile environment dimension."""
    entities: list[HostileEntity] = field(default_factory=list)
    assessment_date: Optional[date] = None

    @property
    def enemies(self) -> list[HostileEntity]:
        return [e for e in self.entities if e.status == FoeStatus.ENEMY]

    @property
    def total_enemy_capacity_required(self) -> float:
        return sum(e.capacity_required_pct for e in self.enemies)

    @property
    def total_capacity_allocated(self) -> float:
        return sum(e.capacity_allocated_pct for e in self.entities)

    @property
    def escalating_entities(self) -> list[HostileEntity]:
        return [e for e in self.entities if e.trajectory == Trajectory.ESCALATING]

    def capacity_deficit(self, available_capacity: float) -> float:
        """How much capacity is missing to address all enemies."""
        return self.total_enemy_capacity_required - available_capacity


# ──────────────────────────────────────────────────────────────
# Dimension 3: Situation State (Documents 14–20)
# ──────────────────────────────────────────────────────────────

@dataclass
class Theatre:
    """Operational theatre with distinct competitive physics."""
    name: str
    segment: str                        # e.g., "<$5K", "$5K–$20K", ">$20K"
    favourability_pct: float            # % of forces favourable
    defensible: bool = False
    key_dynamics: list[str] = field(default_factory=list)

@dataclass
class SituationState:
    """Documents 14–20: complete situation dimension."""
    theatres: list[Theatre] = field(default_factory=list)
    overall_favourability_pct: float = 0.0
    factors_unfavourable_count: int = 0
    factors_total_count: int = 0
    situation_typology: str = ""        # e.g., "late Shaping / early Clash"
    critical_junctures: str = ""        # e.g., "Q2–Q4 2026"
    power_poles: list[str] = field(default_factory=list)
    environment_trend: str = ""         # e.g., "fragmenting toward vacuum"

    @property
    def best_theatre(self) -> Optional[Theatre]:
        if not self.theatres:
            return None
        return max(self.theatres, key=lambda t: t.favourability_pct)


# ──────────────────────────────────────────────────────────────
# Dimension 4: Strategy State (Documents 21–24)
# ──────────────────────────────────────────────────────────────

@dataclass
class StrategicObjective:
    """Single objective with mode-subject-foe structure."""
    mode: str                           # e.g., "ESTABLISH"
    subject: str                        # e.g., "ultra-luxury positioning"
    foe: str                            # e.g., "LGD commodity convergence"
    deadline: str = ""
    measurable_parameters: list[str] = field(default_factory=list)

@dataclass
class Campaign:
    """Single campaign within the operational strategy."""
    name: str
    capacity_allocation_pct: float
    budget_low: float                   # $ millions
    budget_high: float
    start: str                          # e.g., "Q1 2026"
    end: str
    dependencies: list[str] = field(default_factory=list)
    status: str = "NOT_LAUNCHED"        # Updated during execution

@dataclass
class Target:
    """Strategic target with prioritisation assessment."""
    name: str
    priority: int                       # 1 = highest
    accessibility: int                  # 0–10 scale
    criticality: int                    # 0–10 scale
    offence_defence_balance: str = ""
    excluded: bool = False              # Formally excluded targets
    exclusion_reason: str = ""

@dataclass
class StrategyState:
    """Documents 21–24: complete strategy dimension."""
    war_name: str = ""
    war_timeframe: str = ""
    bounded_segment: str = ""           # What theatre the war is fought in
    supreme_objective: Optional[StrategicObjective] = None
    campaigns: list[Campaign] = field(default_factory=list)
    targets: list[Target] = field(default_factory=list)
    victory_probability_pct: float = 0.0
    defeat_probability_pct: float = 0.0
    contingency_probability_pct: float = 0.0
    change_triggers: list[str] = field(default_factory=list)

    @property
    def total_budget(self) -> tuple[float, float]:
        low = sum(c.budget_low for c in self.campaigns)
        high = sum(c.budget_high for c in self.campaigns)
        return (low, high)

    @property
    def active_targets(self) -> list[Target]:
        return [t for t in self.targets if not t.excluded]

    @property
    def campaigns_launched(self) -> list[Campaign]:
        return [c for c in self.campaigns if c.status != "NOT_LAUNCHED"]


# ──────────────────────────────────────────────────────────────
# Dimension 5: Execution State (Documents 25–34)
# ──────────────────────────────────────────────────────────────

@dataclass
class ExecutionDimension:
    """Single execution assessment dimension."""
    name: str                           # e.g., "Command and Control"
    document_number: int                # e.g., 26
    rating: ExecutionRating = ExecutionRating.DEFICIENT
    key_finding: str = ""
    root_cause: str = ""

@dataclass
class CulminationAssessment:
    """Document 30: timing prediction."""
    capability_peak: str = ""           # e.g., "mid-2027"
    decisive_moment: str = ""           # e.g., "late 2028"
    gap_months: int = 0
    alignment: str = ""                 # e.g., "FATAL MISALIGNMENT"

@dataclass
class ExecutionState:
    """Documents 25–34: complete execution dimension."""
    dimensions: list[ExecutionDimension] = field(default_factory=list)
    culmination: Optional[CulminationAssessment] = None
    overall_grade: OverallGrade = OverallGrade.F
    phases_completed: int = 0
    phases_total: int = 7
    objectives_achieved: int = 0
    objectives_total: int = 0
    targets_engaged: int = 0
    targets_total: int = 0
    cost_consumed_low: float = 0.0      # $ millions
    cost_consumed_high: float = 0.0
    strategic_return: str = "ZERO"

    @property
    def deficient_count(self) -> int:
        return sum(1 for d in self.dimensions
                   if d.rating == ExecutionRating.DEFICIENT)

    @property
    def execution_rate(self) -> float:
        """Fraction of phases completed."""
        if self.phases_total == 0:
            return 0.0
        return self.phases_completed / self.phases_total


# ──────────────────────────────────────────────────────────────
# The Complete Strategic World Model
# ──────────────────────────────────────────────────────────────

@dataclass
class StrategicWorldModel:
    """
    Complete subject-specific strategic world model.

    This is the instance — the methodology (general model) applied
    to a specific subject, producing a queryable representation of
    that subject's competitive reality.

    The general model (Strategy by AI methodology) provides the
    transition rules and analytical frameworks. This class provides
    the state representation that those rules operate on.
    """
    subject_name: str
    assessment_date: Optional[date] = None
    identity: Optional[IdentityState] = None
    hostile_environment: Optional[HostileEnvironment] = None
    situation: Optional[SituationState] = None
    strategy: Optional[StrategyState] = None
    execution: Optional[ExecutionState] = None

    # ── Queries ───────────────────────────────────────────────

    def capacity_gap(self) -> Optional[float]:
        """How much capacity is missing to address all enemies?"""
        if not self.hostile_environment:
            return None
        available = 100.0 - sum(
            e.capacity_allocated_pct
            for e in self.hostile_environment.entities
            if e.status != FoeStatus.ENEMY
        )
        return self.hostile_environment.capacity_deficit(available)

    def culmination_aligned(self) -> Optional[bool]:
        """Does capability peak align with decisive moment?"""
        if not self.execution or not self.execution.culmination:
            return None
        return self.execution.culmination.gap_months <= 0

    def strategy_execution_gap(self) -> dict:
        """Compare strategy design against execution reality."""
        if not self.strategy or not self.execution:
            return {}
        return {
            "campaigns_designed": len(self.strategy.campaigns),
            "campaigns_launched": len(self.strategy.campaigns_launched),
            "targets_identified": len(self.strategy.active_targets),
            "targets_engaged": self.execution.targets_engaged,
            "objectives_set": self.execution.objectives_total,
            "objectives_achieved": self.execution.objectives_achieved,
            "cost_consumed": (self.execution.cost_consumed_low,
                              self.execution.cost_consumed_high),
            "strategic_return": self.execution.strategic_return,
        }

    # ── Consistency checks ────────────────────────────────────

    def check_capacity_consistency(self) -> list[str]:
        """Verify that allocations don't exceed 100%."""
        issues = []
        if self.hostile_environment:
            total = self.hostile_environment.total_capacity_allocated
            if total > 100.0:
                issues.append(
                    f"Total capacity allocated ({total:.0f}%) exceeds "
                    f"100% — over-commitment detected"
                )
        return issues

    def check_strategy_respects_constraints(self) -> list[str]:
        """Verify strategy doesn't ignore identity constraints."""
        issues = []
        if self.identity and self.strategy:
            for option in self.identity.mission.foreclosed_options:
                for campaign in self.strategy.campaigns:
                    if option.lower() in campaign.name.lower():
                        issues.append(
                            f"Campaign '{campaign.name}' may conflict "
                            f"with foreclosed option: '{option}'"
                        )
        return issues

    def check_enemy_mission_alignment(self) -> list[str]:
        """Verify enemy classifications align with mission."""
        issues = []
        if self.identity and self.hostile_environment:
            if not self.identity.mission.primary:
                issues.append(
                    "No primary mission defined — enemy classifications "
                    "cannot be validated against mission criteria"
                )
        return issues

    def validate(self) -> list[str]:
        """Run all consistency checks."""
        issues = []
        issues.extend(self.check_capacity_consistency())
        issues.extend(self.check_strategy_respects_constraints())
        issues.extend(self.check_enemy_mission_alignment())
        return issues
```

---

## De Beers Instance: Demonstrating the Model

```python
"""
De Beers UK Strategic World Model — Instance Demonstration
===========================================================

This demonstrates how the classes above are populated with findings
from the De Beers 34-document portfolio. The methodology (general
model) produced these findings; the classes (state representation)
make them queryable.
"""

de_beers = StrategicWorldModel(
    subject_name="De Beers UK Limited",
    assessment_date=date(2026, 2, 8),

    identity=IdentityState(
        mission=StrategicMission(
            primary="Maintain natural diamond premium pricing through "
                    "provenance-based differentiation",
            secondary=["Preserve Botswana partnership",
                        "Execute ownership transition"],
            foreclosed_options=["Mass-market cost leadership",
                                "Lab-grown pivot",
                                "Rapid retail excellence"],
        ),
        doctrine=StrategicDoctrine(
            implicit_doctrines=["Legacy monopoly control",
                                "Defensive brand protection",
                                "Financial optimisation"],
            contradictions=["Monopoly control vs brand building",
                            "Financial short-termism vs luxury investment"],
            has_explicit_doctrine=False,
        ),
        heritage_years=138,
        coherence_rating="FUNDAMENTAL INCOHERENCE",
        readiness_module_three="MODERATE",
        readiness_module_five="CRITICAL WEAKNESS",
    ),

    hostile_environment=HostileEnvironment(
        entities=[
            HostileEntity("Lab-Grown Diamond Producers", FoeStatus.ENEMY,
                          Trajectory.ESCALATING, Confidence.HIGH,
                          capacity_required_pct=45.0,
                          capacity_allocated_pct=8.0),
            HostileEntity("Anglo American PLC", FoeStatus.ENEMY,
                          Trajectory.STABLE, Confidence.HIGH,
                          capacity_required_pct=15.0,
                          capacity_allocated_pct=60.0),
            HostileEntity("Transparency Platforms", FoeStatus.ENEMY,
                          Trajectory.ESCALATING, Confidence.MEDIUM,
                          capacity_required_pct=45.0,
                          capacity_allocated_pct=4.0),
            HostileEntity("Government of Botswana", FoeStatus.ENEMY,
                          Trajectory.ESCALATING, Confidence.MEDIUM,
                          capacity_required_pct=45.0,
                          capacity_allocated_pct=25.0,
                          mutation_timeline="Adversary→Enemy Q4 2026"),
        ],
        assessment_date=date(2026, 1, 18),
    ),

    situation=SituationState(
        theatres=[
            Theatre("Mass market", "<$5K", 15.0, defensible=False),
            Theatre("Premium", "$5K–$20K", 40.0, defensible=False),
            Theatre("Ultra-luxury", ">$20K", 60.0, defensible=True),
        ],
        overall_favourability_pct=35.0,
        factors_unfavourable_count=15,
        factors_total_count=20,
        situation_typology="Late Shaping / early Clash transition",
        critical_junctures="Q2–Q4 2026",
    ),

    strategy=StrategyState(
        war_name="Natural Diamond Premium Defence War",
        war_timeframe="2025–2030",
        bounded_segment="Ultra-luxury (>$20K retail)",
        supreme_objective=StrategicObjective(
            mode="ESTABLISH",
            subject="Ultra-luxury natural diamond market positioning",
            foe="LGD commodity convergence AND transparency destruction",
            deadline="2030-12-31",
        ),
        campaigns=[
            Campaign("Brand Transformation", 27.5, 150, 200,
                     "Q1 2026", "Q4 2027"),
            Campaign("Distribution Optimisation", 37.5, 300, 400,
                     "Q3 2027", "Q4 2030"),
            Campaign("Counter-Narrative", 12.5, 50, 75,
                     "Q3 2026", "Q4 2030"),
            Campaign("Botswana Partnership", 12.5, 40, 60,
                     "Q1 2026", "Q4 2027"),
            Campaign("Anglo Management", 6.5, 25, 40,
                     "Q1 2026", "Q4 2030"),
        ],
        targets=[
            Target("Generational Consumer Narrative", 1, 7, 9),
            Target("Sightholder Control System", 1, 8, 8),
            Target("LGD Sustainability Legitimacy", 2, 6, 7),
            Target("LGD Cost Advantage", 3, 0, 10, excluded=True,
                   exclusion_reason="Accessibility 0/10 — unassailable"),
        ],
        victory_probability_pct=30.0,
        defeat_probability_pct=55.0,
        contingency_probability_pct=15.0,
    ),

    execution=ExecutionState(
        dimensions=[
            ExecutionDimension("Commitment", 25, ExecutionRating.MARGINAL,
                               "3/5 components crossed threshold"),
            ExecutionDimension("Command and Control", 26,
                               ExecutionRating.DEFICIENT,
                               "No command structure exists",
                               root_cause="ROOT CAUSE of cascade"),
            ExecutionDimension("Cohesion-Collision", 27,
                               ExecutionRating.DEFICIENT),
            ExecutionDimension("Tempo and Friction", 28,
                               ExecutionRating.DEFICIENT),
            ExecutionDimension("Centre of Gravity", 29,
                               ExecutionRating.DEFICIENT),
            ExecutionDimension("Culmination", 30,
                               ExecutionRating.DEFICIENT),
            ExecutionDimension("Fog-Chaos", 31,
                               ExecutionRating.DEFICIENT),
            ExecutionDimension("Adaptation", 32,
                               ExecutionRating.MARGINAL,
                               "Strategy maintained — correct direction"),
            ExecutionDimension("Termination", 33,
                               ExecutionRating.DEFICIENT),
        ],
        culmination=CulminationAssessment(
            capability_peak="mid-2027",
            decisive_moment="late 2028",
            gap_months=15,
            alignment="FATAL MISALIGNMENT",
        ),
        overall_grade=OverallGrade.F,
        phases_completed=0, phases_total=7,
        objectives_achieved=0, objectives_total=10,
        targets_engaged=0, targets_total=9,
        cost_consumed_low=245.0, cost_consumed_high=375.0,
    ),
)

# ── Query the world model ─────────────────────────────────────

print(f"Subject: {de_beers.subject_name}")
print(f"Enemies: {len(de_beers.hostile_environment.enemies)}")
print(f"Enemy capacity required: "
      f"{de_beers.hostile_environment.total_enemy_capacity_required:.0f}%")
print(f"Capacity gap: {de_beers.capacity_gap():.0f}%")
print(f"Best theatre: {de_beers.situation.best_theatre.name} "
      f"({de_beers.situation.best_theatre.favourability_pct:.0f}% favourable)")
print(f"Culmination aligned: {de_beers.culmination_aligned()}")
print(f"Strategy-execution gap: {de_beers.strategy_execution_gap()}")
print(f"Consistency issues: {de_beers.validate()}")
```

**Expected output:**
```
Subject: De Beers UK Limited
Enemies: 4
Enemy capacity required: 150%
Capacity gap: 147%
Best theatre: Ultra-luxury (60% favourable)
Culmination aligned: False
Strategy-execution gap: {'campaigns_designed': 5, 'campaigns_launched': 0, ...}
Consistency issues: []
```

---

## What a Developer Does With This

1. **Build strategic analysis platforms** that store findings in structured, queryable form instead of unstructured documents
2. **Implement agent memory** where strategic state persists between sessions and across multi-step reasoning
3. **Create simulation engines** that predict consequences of proposed actions by applying transition rules to current state
4. **Enforce consistency** by running validation checks across the portfolio after each update
5. **Compare instances** — produce strategic world models for multiple competing organisations and analyse the competitive landscape as interacting state machines

The classes are the container. The methodology — available at [strategybyai.org](https://strategybyai.org) — is the reasoning framework that fills them with accurate, evidence-based, cross-referenced strategic intelligence.

→ [Concept: why strategic world models are needed](CONCEPT.md) | [Architecture: general model and instances](ARCHITECTURE.md) | [Back to README](../README.md)
