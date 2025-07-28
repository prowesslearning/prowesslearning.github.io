---
layout: post
title: 'Azure AI Foundry'
category: AI 
author: your_author_id
excerpt: 'Lets decompose Azure AI Foundry'
tags: azure ai aisecurity
image: /assets/images/Azure-AI-Foundry-logo.jpg
---

# What is Azure AI Foundry

Azure AI Foundry is a unified end-to-end platform for enterprise AI operations. It empowers developers to drive innovation and shape the future with AI in a safe, secure and responsible way.

# What is Azure Foundry used for?

Azure AI Foundry provides a comprehensive environment for building, evaluating, monitoring, and scaling AI applications, particularly those driven by generative AI models and agents. It aims to bridge the gap between AI experimentation and robust, production-grade deployment.

# Azure AI Foundry Architecture: A layered approach

![Azure AI Foundry Architecture ](/assets/images/ai-foundry-architecture.png "Azure AI Foundry Architecture")
*Image courtesy: [Microsoft]*

Azure AI Foundry is built using existing Azure services, providing a unified management and development experience. Its architecture involves serveral key components:

- **Azure AI Foundry Hub**
   - This is the top-level resource in Azure AI Foundry and serves as a central management point and governance.
   - The hub provides security configurations (including a managed network that can span projects and model endpoints), compute resources for interactive development, fine-tuning, and model deployment, and connections to other Azure services (Azure OpenAI, Azure AI Services, Azure AI Search).
   - Hub-scoped connections are shared with projects created from the hub, simplifying resource management.
   - Associated with an Azure Storage account for data upload and artifact storage. 
   - Ideal for organisations managing multiple AI projects.
   - Access via dedicated url ai.azure.com

- **Azure AI Foundry Project**
    - A project is a child resource of the hub, representing a specific AI use case.
    - It provides isolated containers for data, models, and development tools.
    - Projects offer access to development tools (like chat playground, prompt flow), reusable components (datasets, models, indexes), and project-scoped connections for more granular access control (e.g., private access to a specific data source for only that project).

- **Connected Azure Services**
  Azure AI Foundry integrates seamlessly with a multitude of other Azure services that provide the underlying AI capabilities and infrastructure. These include:
    - Azure OpenAI Service: For access to advanced OpenAI models (GPT series (o4-mini, o3, gpt-4.1 etc), DALL-E, etc.).
    - Azure AI Services: The collection of pre-built AI models for vision, speech, language, and decision.
    - Azure Machine Learning: Powers the compute, model training, and deployment aspects.
    - Azure AI Search: Critical for Retrieval Augmented Generation (RAG) patterns, providing knowledge grounding for generative AI models.
    - Azure Storage: For storing data, models, and application artifacts.
    - Azure Key Vault: For secure secret management and customer-managed keys.
    - Azure Monitor & Log Analytics: For observability and logging.
    - Azure Virtual Network (VNet) & Private Link: For network isolation and secure connectivity.

- **Foundry Agent Sevice (for AI Agents)**
    - A capability hosted within Azure AI Foundry for defining and hosting AI agents.
    - Manages chat threads, orchestrates tool calls, enforces content safety, and integrates with identity, networking, and observability systems.

