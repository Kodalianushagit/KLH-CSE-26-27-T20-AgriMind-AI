# AgriMind: An Agentic Multi-AI Advisory Ecosystem for Smallholder Farmers

## Team
- [Name] – [ID Number]
- [Name] – [ID Number]
- [Name] – [ID Number]
<!-- Add all team members here -->

## Supervisor
Dr. Srikanth Cherukuvada

## Abstract
Smallholder farmers often lack timely, personalized access to crop guidance,
disease diagnosis, market pricing, and weather alerts, particularly where
literacy or connectivity is limited. Existing agricultural tools are largely
reactive, single-purpose, and text/English-heavy, requiring the farmer to
actively seek out information. AgriMind addresses this gap through a
Service-Oriented Architecture of five autonomous AI agents — crop
recommendation, crop disease detection, market price forecasting, weather
and irrigation advisory, and a vernacular voice/chat interface — coordinated
through an API Gateway and message queue. The system's core novelty lies in
proactive, agent-to-agent triggering (agents act and alert without being
asked), a voice-first interface designed for low-literacy users, and
cross-agent reasoning that blends multiple data sources into a single
recommendation. AgriMind aligns with SDG 2 (Zero Hunger) and SDG 1 (No
Poverty), aiming to improve crop decisions and reduce preventable losses for
underserved farming communities.

<!-- Replace/refine this abstract once the instructor formally approves the
     final title and abstract. -->

## System Architecture (Overview)
- **Crop Recommendation Agent** — classification model suggesting suitable crops
- **Disease Detection Agent** — computer vision model diagnosing crop disease from leaf images
- **Market Price Forecasting Agent** — time-series model forecasting crop prices
- **Weather/Irrigation Advisory Agent** — proactively alerts farmers on weather/irrigation needs
- **Voice/Chat Agent** — LLM-based vernacular interface for farmer interaction

All agents run as independent microservices, communicating via REST/gRPC and
an event bus/message queue, behind a single API Gateway (data-per-service
pattern).

## Setup and Execution Instructions

### Prerequisites
- Python 3.10+
- Docker & Docker Compose
- (add any additional dependencies as they're introduced, e.g. specific ML libraries)

### Installation
```bash
git clone <repo-url>
cd <repo-name>
docker-compose up --build
```

### Running Individual Services
```bash
# Example — update per actual service names once implemented
cd src/crop-recommendation-service
python app.py
```

### Environment Variables
<!-- List any API keys / config needed once services are implemented -->

## Current Phase Status
- [ ] Checkpoint 1 (Day 15): Core architecture + 2 agents functional
- [ ] Checkpoint 2 (Day 25): All 5 agents integrated with orchestration
- [ ] Checkpoint 3 (Day 35): Voice interface completed + system polish

**Current status:** Project direction finalized (pending instructor
approval of title/abstract); repository scaffolded; implementation not yet
started.

## Repository Structure
```
/src        - All source code (agent services, orchestration logic)
/docs       - Abstract, architecture diagrams, design notes
/data       - Datasets used, or DATA_SOURCES.md if data is external/live
/results    - Model outputs, metrics logs, screenshots
/reports    - Checkpoint reports, review PPTs, submissions
```
