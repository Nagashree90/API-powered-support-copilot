# API-powered-support-copilot

AI-powered RESTful APIs to assist support executives by analyzing customer issues, recommending responses, summarizing conversations, and monitoring unattended critical issues in real-time.

Project Overview

The Support Copilot helps customer support teams by:

Analyzing new support issues for severity and criticality.
Recommending message templates based on past issue resolutions and customer history.
Summarizing full customer-agent conversations automatically.
Monitoring unattended critical issues to ensure SLA compliance.
The solution is API-driven, cloud-hosted (AWS recommended), and designed for real-time responsiveness.

Features

Issue intake and analysis.
Recommended message generation.
Conversation summarization.
Unattended critical issue monitoring.
RESTful API endpoints using FastAPI.
Deployed using ngrok for quick testing.

Tech Stack

Backend: Python, FastAPI
Deployment (Prototype): Google Colab + Ngrok
API Documentation: Swagger (OpenAPI 3.0)
Future Production Hosting: AWS EC2, Lambda, or Azure Functions
Database (Future Expansion): MySQL / Amazon RDS

API Documentation

Interactive Swagger UI available when running APIs:
https://532bcf736135.ngrok-free.app/docs

For detailed API specification, see:
support_copilot_api.yaml

Setup Instructions

Local or Colab Setup:
Install dependencies:

pip install fastapi uvicorn pyngrok nest-asyncio

Run API (example in Colab notebook):

from fastapi import FastAPI
from pyngrok import ngrok
import uvicorn


Access Swagger UI:

https://532bcf736135.ngrok-free.app/docs


API Endpoints:
/api/issues/analyze
/api/issues/history
/api/issues/similar
/api/messages/recommend-template
/api/conversations/summary
/api/issues/unattended

Architecture Diagram

Project Files

https://colab.research.google.com/drive/1w0cczuTOzhtCO4j9x-rmwZKg5c2_7YVg?usp=sharing – FastAPI Colab Notebook
support_copilot_api.yaml – API Documentation (OpenAPI Spec)
system architecture.png – System Architecture
explanation_document.docs – Technical Explanation

Security

Production API should implement OAuth 2.0 / JWT for authentication.
Ensure HTTPS for all API endpoints.

Future Improvements

Connect APIs to actual MySQL/AWS RDS databases.
Use real LLM APIs for summarization and message recommendation.
Deploy to AWS EC2 / Lambda for scalable production usage.

Author

Developed by Nagashree
Contact: ygnagashree@gmail.com
