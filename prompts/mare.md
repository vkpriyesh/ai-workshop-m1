## **2. Director of Engineering for Solution Architect Tasks**

```json
{
  "task": "Design and review a scalable, secure cloud-native architecture for a large enterprise",
  "role": "Director of Engineering",
  "context": {
    "industry": "Financial Services",
    "primary_stack": ["Azure", "AKS", "Azure Functions", "Cosmos DB", "Azure API Management"],
    "constraints": {
      "compliance": ["MAS TRM", "ISO 27001", "PDPA"],
      "latency": "sub-200ms for API responses",
      "availability": "99.99% SLA"
    }
  },
  "deliverables": [
    {
      "type": "High-level architecture diagram",
      "details": {
        "viewpoints": ["C4 context and container diagrams", "network topology"],
        "tools": ["PlantUML", "Mermaid"]
      }
    },
    {
      "type": "Detailed implementation plan",
      "sections": [
        "Infrastructure-as-Code strategy (Bicep/Terraform)",
        "CI/CD pipelines (Azure DevOps YAML)",
        "Security and IAM policies",
        "Monitoring & observability (Grafana, Azure Monitor)"
      ]
    },
    {
      "type": "Risk register with mitigations",
      "categories": ["security", "performance", "vendor lock-in"]
    }
  ],
  "non_functional_requirements": {
    "scalability": "horizontal auto-scaling under AKS with HPA",
    "security": "end-to-end encryption with TLS 1.3, Azure Key Vault for secrets",
    "interoperability": "REST + gRPC APIs for cross-service communication"
  },
  "decision_criteria": [
    "Performance under load",
    "Ease of maintenance",
    "Cost efficiency",
    "Future readiness for AI/ML workloads"
  ]
}
```
