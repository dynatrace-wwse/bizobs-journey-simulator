--8<-- "snippets/index.js"

--8<-- "snippets/disclaimer.md"

# Business Observability Journey Simulator

Experience the complete **4-Step Workflow** for creating AI-powered customer journeys with real business observability, LoadRunner integration, and Dynatrace BizEvents. Transform simple business requirements into comprehensive observability demonstrations.

<p align="center">
  <img src="img/bizobs_banner.png" alt="BizObs Journey Simulator" width="600">
</p>

## 🎯 The Complete 4-Step App Workflow

### **Step 1: Customer Details** 👤 
**Define Your Business Foundation**

Start by establishing the core business context for your simulation:

- **Company Name**: Set your business identity (e.g., *ShopMart*, *TechFlow*, *SecureBank*)
- **Website Domain**: Define the digital presence (e.g., *shopmart.com*, *techflow.io*, *securebank.net*)
- **Journey Requirements**: Describe the customer flow you want to simulate

**Real Examples:**
```
Company: GlobalRetail Inc
Domain: globalretail.com  
Requirements: "Complete e-commerce journey from product discovery 
through checkout, payment processing, and order fulfillment with 
mobile-first customer experience"
```

### **Step 2: Generate Prompts** 🤖
**AI-Powered Business Intelligence Creation**

The platform generates sophisticated prompts for GitHub Copilot integration:

- **C-suite Analysis Prompt**: Executive-level business insights and KPI focus areas
- **Customer Journey Prompt**: Detailed user interaction flows with conversion points
- **Industry-Specific Context**: Tailored scenarios for your business domain
- **Copilot Integration Ready**: Structured prompts optimized for AI collaboration

**Generated Prompt Example:**
```markdown
Create a comprehensive customer journey for GlobalRetail Inc focusing on:
- Mobile-first shopping experience with 3.2-second page load targets
- Cart abandonment recovery with personalized email sequences  
- Payment processing with fraud detection and multiple gateway failover
- Post-purchase engagement through order tracking and review requests
- Revenue optimization with cross-sell and upsell touchpoints
```

### **Step 3: Process Check** ⚡
**Validation & Configuration**

Before execution, validate and fine-tune your journey configuration:

- **Journey Data Preview**: Review generated customer touchpoints and business logic
- **Business Fields Validation**: Examine revenue metrics, conversion rates, and KPI calculations
- **Error Simulation Toggle**: Enable realistic failure scenarios for resilience testing
- **Configuration Options**: Adjust timing, persona behaviors, and service complexity

**Validation Dashboard:**
```
✅ Journey Steps: 8 validated touchpoints
✅ Business Metrics: Revenue tracking configured  
✅ Service Architecture: 12 microservices ready
⚠️  Error Simulation: Optional failure patterns available
🔧 LoadRunner: Performance test scripts pre-generated
```

### **Step 4: Generate Data** 📊
**Execute Comprehensive Simulations**

Choose your execution mode for complete business observability:

#### **🎯 Single Simulation Mode**
Perfect for demonstrations and real-time analysis:

- **Live Journey Execution**: Real customer interactions with Dynatrace correlation
- **Business Metrics Tracking**: Revenue, conversion rates, customer satisfaction scores
- **Response Time Analysis**: Performance impact on business outcomes
- **Error Scenario Testing**: Realistic failure patterns with business impact quantification
- **Export Capabilities**: Results available for further analysis and reporting

#### **�️ LoadRunner Testing Mode**
Enterprise-grade performance testing with business context:

- **Automated Script Generation**: Complete LoadRunner C-scripts with Dynatrace integration
- **Multiple Load Scenarios**: 
  - Light Load: 20 concurrent users
  - Medium Load: 100 concurrent users  
  - Heavy Load: 300 concurrent users
  - Extreme Load: 600 concurrent users
- **Business Context Correlation**: Revenue tracking under load conditions
- **Stress Testing Reports**: Performance vs. business outcome analysis

## � What Gets Created in Each Step

### **Realistic Customer Journeys**
```json
{
  "companyName": "GlobalRetail Inc",
  "domain": "globalretail.com",
  "journeySteps": [
    "Product Discovery",
    "Category Browsing", 
    "Product Details",
    "Add to Cart",
    "Checkout Process",
    "Payment Processing",
    "Order Confirmation",
    "Fulfillment Tracking"
  ],
  "businessMetrics": {
    "averageRevenue": 127.50,
    "conversionRate": 0.734,
    "customerSatisfaction": 4.2,
    "journeyDuration": "8.4 minutes"
  }
}
```

### **Dynamic Microservices Architecture**
- **Auto-Scaling Services**: 15+ services spawned based on journey complexity
- **Dynatrace Service Splitting**: Each step runs as a separate, traceable service
- **Business Context Tagging**: Revenue and customer data embedded in all traces
- **Health Monitoring**: Real-time service status and performance metrics

### **LoadRunner Performance Tests**
```c
// Auto-generated LoadRunner C-script with business context
Action() {
    lr_start_transaction("BizObs_GlobalRetail_ProductDiscovery");
    
    web_add_header("dt-meta-businessRevenue", "67.25");
    web_add_header("dt-meta-customerPersona", "Karen");
    web_add_header("dt-meta-conversionStep", "discovery");
    
    web_custom_request("product_discovery", 
        "URL=http://localhost:8080/api/journey/discover",
        "Method=POST",
        "Body={\"company\":\"GlobalRetail\",\"persona\":\"Karen\",\"step\":\"discovery\"}",
        LAST);
    
    lr_end_transaction("BizObs_GlobalRetail_ProductDiscovery", LR_AUTO);
    return 0;
}
```

### **Business Observability Data**
- **Dynatrace BizEvents**: Revenue, conversion, and satisfaction metrics
- **Distributed Traces**: End-to-end journey visibility with business context
- **Performance Correlation**: How technical metrics impact business outcomes  
- **Error Business Impact**: Quantified revenue loss from technical failures

## 🎪 Real-World Demo Scenarios

<div class="grid cards" markdown>
- **🛍️ E-Commerce Journey** 
  
    GlobalRetail customer flow: Browse → Cart → Checkout → Payment → Fulfillment
    
    *Average Revenue: $87.50 | Duration: 6.2 min | Services: 10*

- **🛡️ Insurance Application**
  
    SecureLife policy process: Quote → Application → Underwriting → Approval → Activation
    
    *Average Revenue: $425.00 | Duration: 22.1 min | Services: 14*

- **🚀 SaaS Onboarding**
  
    TechFlow platform journey: Trial → Demo → Purchase → Setup → Activation
    
    *Average Revenue: $199.99 | Duration: 15.7 min | Services: 12*

- **🏢 Enterprise Procurement**
  
    GlobalCorp solution buying: RFP → Evaluation → Demo → Contract → Implementation
    
    *Average Revenue: $4,250.00 | Duration: 89.3 min | Services: 18*
</div>

## 🚀 Getting Started Options

### **⚡ Quick Start (5 Minutes)**
1. **Launch GitHub Codespaces** - Pre-configured environment ready instantly
2. **Access Web Interface** - Navigate to localhost:8080 for the 4-step workflow
3. **Follow the Steps** - Complete Steps 1-4 to create your first business journey
4. **Watch Live Results** - Real-time business metrics and Dynatrace traces

### **🔧 Production Deployment**
1. **Install Dynatrace OneAgent** - Full observability stack for production environments
2. **Configure BizEvents** - Business intelligence and revenue tracking setup
3. **LoadRunner Integration** - Enterprise performance testing with business context
4. **Kubernetes Deployment** - Scalable microservices architecture

### **📊 Business Intelligence Focus**
1. **Persona-Based Scenarios** - Realistic customer behavior modeling
2. **Revenue Correlation** - Connect technical performance to business outcomes
3. **Conversion Analysis** - Track funnel performance and optimization opportunities
4. **Executive Dashboards** - Business KPI reporting and trend analysis

## 🎯 Key Learning Outcomes

**Master Business Observability**
- Transform technical monitoring into business intelligence
- Implement revenue tracking in distributed microservices architectures  
- Create realistic customer journey simulations with measurable outcomes
- Build executive-level observability dashboards

**Technical Implementation Skills**
- Dynatrace BizEvents integration patterns and best practices
- Microservices observability with business context correlation
- LoadRunner automation with performance-to-business impact analysis
- Advanced error simulation and system resilience testing

**AI-Powered Development**
- GitHub Copilot integration for sophisticated business scenario creation
- Automated prompt generation for domain-specific business contexts
- Intelligent customer persona development and behavioral modeling
- AI-driven journey optimization and conversion improvement

!!! success "Transform Your Observability Strategy"
    This platform demonstrates the evolution from pure technical monitoring to business-intelligent observability. Learn to build systems that provide measurable value to both engineering teams and business stakeholders.

## 🎬 Ready to Experience the 4-Step Workflow?

Start with **Step 1: Customer Details** and progress through AI-powered prompt generation, validation, and comprehensive data generation to see how technical observability transforms into business intelligence.

<div class="grid cards" markdown>
- [🚀 **Launch the Platform** :octicons-arrow-right-24:](2-getting-started.md)
</div>
