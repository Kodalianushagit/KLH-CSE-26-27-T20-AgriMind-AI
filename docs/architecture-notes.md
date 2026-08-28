# Architecture Notes

## Novelty Summary
1. Proactive cross-agent triggering — agents act and alert the farmer
   without being asked, rather than only responding to queries.
2. Vernacular voice-first interface — designed for low-literacy users who
   can't easily navigate a text-heavy app.
3. Cross-agent reasoning — e.g., crop recommendation factors in live market
   price forecasts, not just soil/weather data.

## Example Agentic Flow
1. Farmer uploads a leaf photo.
2. Disease Detection Agent identifies blight risk.
3. Disease Detection Agent autonomously notifies the Advisory Agent
   (no user request involved).
4. Advisory Agent pushes a voice alert to the farmer via the Voice Agent,
   in their local language.

## SOA Integration
- Communication: REST/gRPC between services; message queue (Kafka/RabbitMQ)
  for asynchronous alerts
- Entry point: single API Gateway
- Data: data-per-service pattern — each agent owns its own database
