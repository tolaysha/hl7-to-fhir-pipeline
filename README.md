🏥 HL7 to FHIR Pipeline with Aidbox, n8n and Telegram
This project implements an event-driven healthcare data ingestion pipeline that receives HL7v2 messages, parses and transforms them into FHIR resources, and stores them in an Aidbox FHIR server.

It also integrates with n8n for orchestration and monitoring, and sends status updates and errors to a Telegram bot.

🚀 Features
✅ HL7v2 ingestion from AMQP (CloudAMQP or Kafka)

🔄 HL7 → FHIR transformation using custom JS or LLMs (OpenRouter)

🏥 FHIR resource upload (e.g. Patient, Encounter, Observation) to Aidbox

🔔 Telegram bot notifications for success/failure/status

🧠 Optionally uses OpenRouter LLM for smart message parsing

📦 Fully automated via n8n workflow engine



🔧 Stack
Aidbox — FHIR-compliant data store and rules engine

n8n — Workflow orchestration

RabbitMQ / Kafka — HL7 transport (AMQP / stream)

OpenRouter (optional) — HL7 → FHIR parsing via LLM

Telegram Bot — Notifications and control



📄 Example Flow
HL7 message arrives in queue

n8n workflow picks up the message

Message is validated and parsed

Data is mapped to FHIR (e.g. Patient)

Resource is POSTed to Aidbox

Telegram bot notifies of result
