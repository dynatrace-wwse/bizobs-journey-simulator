--8<-- "snippets/2-getting-started.js"

# Getting Started

Welcome to the **BizObs Journey Simulator**! This guide shows you how to create comprehensive customer journeys with business observability through our intuitive **4-Step Workflow**.

## 🚀 Quick Setup

### Access the Platform

**Option 1: GitHub Codespaces (Recommended)**
```bash
# Navigate to: https://github.com/dynatrace-wwse/bizobs-journey-simulator
# Click: Code → Codespaces → Create codespace on main
# Platform automatically starts at: localhost:8080
```

**Option 2: Local Setup**
```bash
git clone https://github.com/dynatrace-wwse/bizobs-journey-simulator.git
cd bizobs-journey-simulator/app
npm install && npm start
# Access at: http://localhost:8080
```

## 🎯 App Overview & Navigation

When you open the platform, you'll see the main interface with four distinct sections:

> 📸 **[Screenshot Needed: Main App Interface]**  
> *Show the complete 4-step workflow interface with Step 1-4 tabs visible*

### Main Interface Components:
- **Step Navigation Tabs**: Clear 1-4 step progression at the top
- **Business Context Panel**: Company and journey configuration area  
- **Real-time Metrics**: Live business and technical performance data
- **Action Buttons**: Execute simulations and generate LoadRunner tests

## 🎯 Step-by-Step Customer Journey Creation

Follow this complete walkthrough to create your first business observability demonstration:

### **Step 1: Customer Details** 👤 
**Define Your Business Foundation**

> 📸 **[Screenshot Needed: Step 1 - Customer Details Tab]**  
> *Show the input form with Company Name, Domain, and Journey Requirements fields*

Fill in your business context:

1. **Company Name**: Enter your business name (e.g., "TechFlow Inc")
2. **Website Domain**: Add your domain (e.g., "techflow.com")  
3. **Journey Requirements**: Describe your customer flow

**Example Input:**
```
Company Name: TechFlow Inc
Domain: techflow.com
Journey Requirements: SaaS trial signup process with onboarding, 
feature exploration, and conversion to paid subscription
```

**💡 What Happens Next:**
The platform analyzes your inputs and prepares industry-specific prompts and service architecture recommendations.

### **Step 2: Generate Prompts** 🤖
**AI-Powered Business Intelligence Creation**

> 📸 **[Screenshot Needed: Step 2 - Generate Prompts Tab]**  
> *Show the generated prompts section with C-suite and Customer Journey prompt text areas*

Click **"Generate Prompts"** to create AI-powered business scenarios:

**What You'll See:**
- **C-suite Analysis Prompt**: Executive-level business insights for your company
- **Customer Journey Prompt**: Detailed user flow optimized for GitHub Copilot
- **Copy to Clipboard**: Easy integration with AI coding assistants

**Example Generated Output:**
```markdown
🎯 TechFlow Inc Customer Journey Analysis

Create a comprehensive SaaS trial journey focusing on:
- Freemium signup with email verification and onboarding
- Feature discovery through guided tutorials and tooltips  
- Usage tracking with conversion triggers at 7-day and 14-day marks
- Revenue target: $99-299 per conversion with 23% trial-to-paid rate
```

**💡 Next Action:**
Copy these prompts and use them with GitHub Copilot to enhance your business scenarios and technical implementation.

### **Step 3: Process Check** ⚡
**Validation & Configuration**

> 📸 **[Screenshot Needed: Step 3 - Process Check Tab]**  
> *Show the validation dashboard with journey steps, business metrics, and configuration options*

Review and configure your journey before execution:

**Journey Validation:**
- ✅ **Journey Steps**: Review the generated customer touchpoints
- ✅ **Business Metrics**: Validate revenue and conversion rate calculations  
- ✅ **Service Architecture**: Confirm microservices that will be created
- ⚠️ **Error Simulation**: Toggle realistic failure scenarios (optional)

**Key Configuration Options:**
```
Customer Persona: Choose from Karen, Raj, Alex, or Sophia
Think Time: 1-10 seconds (user behavior pacing)
Error Rate: 0-20% (failure simulation percentage) 
Service Count: 5-18 services (architecture complexity)
```

**💡 Pro Tip:**
Enable error simulation to demonstrate how business metrics correlate with technical performance issues.

### **Step 4: Generate Data** 📊
**Execute Comprehensive Simulations**

> 📸 **[Screenshot Needed: Step 4 - Generate Data Tab]**  
> *Show both Single Simulation and LoadRunner Testing Mode buttons with results dashboard*

Choose your execution mode:

#### **🎯 Single Simulation Mode**
Perfect for live demonstrations:

> 📸 **[Screenshot Needed: Single Simulation Results]**  
> *Show real-time business metrics dashboard with revenue, conversion rate, and service status*

**What You'll See:**
```
🔄 TechFlow Journey - Alex Persona (Live)
💰 Revenue: $199.99 projected
 Step: 5/7 completed (71% progress)
⏱️  Response: 0.9s avg (Excellent)
😊 Satisfaction: 4.4/5.0
🔄 Services: 12/12 active
```

#### **🏎️ LoadRunner Testing Mode**
Enterprise performance testing:

> 📸 **[Screenshot Needed: LoadRunner Script Generation]**  
> *Show the generated C-script preview and download options*

**Generated Artifacts:**
- **Complete C-Scripts**: Ready-to-run LoadRunner tests
- **Multiple Scenarios**: Light (20 users) → Heavy (300 users)
- **Business Context**: Revenue tracking under load
- **Download Options**: Scripts and configuration files

**Sample Generated Script:**
```c
Action() {
    lr_start_transaction("BizObs_TechFlow_SaaS_Journey");
    
    web_add_header("dt-meta-businessRevenue", "199.99");
    web_add_header("dt-meta-customerPersona", "Alex");
    
    web_custom_request("saas_signup", 
        "URL=http://localhost:8080/api/journey/signup",
        "Method=POST",
        "Body={\"company\":\"TechFlow\",\"persona\":\"Alex\"}",
        LAST);
        
    lr_end_transaction("BizObs_TechFlow_SaaS_Journey", LR_AUTO);
}
```

## � What You Get

After completing the 4-step workflow, you'll have:

**📊 Complete Business Observability Stack**
- **Live Customer Journeys**: Real-time business metrics with revenue tracking
- **Dynamic Microservices**: 5-18 services that scale based on your journey complexity
- **Dynatrace Integration**: BizEvents and distributed traces with business context
- **Performance Testing**: LoadRunner C-scripts ready for enterprise testing

## 🎭 Customer Personas

> 📸 **[Screenshot Needed: Customer Personas Selection]**  
> *Show the 4 persona cards (Karen, Raj, Alex, Sophia) with their behavioral profiles*

Choose from 4 realistic behavioral profiles:

**🛍️ Karen - Retail Customer**
- Mobile-first shopper, quick decisions, deal-driven
- Revenue: $45-85 | Conversion: 68% | Journey: E-commerce

**🛡️ Raj - Insurance Professional** 
- Risk-aware researcher, methodical analysis, brand-focused
- Revenue: $180-350 | Conversion: 84% | Journey: Insurance

**🚀 Alex - Tech Enthusiast**
- Innovation-focused early adopter, rapid exploration
- Revenue: $95-180 | Conversion: 72% | Journey: SaaS

**🏢 Sophia - Enterprise Buyer**
- Process-oriented, compliance-focused, multi-stakeholder
- Revenue: $2500-5000 | Conversion: 91% | Journey: Enterprise

## 🔍 What Happens in Dynatrace

> 📸 **[Screenshot Needed: Dynatrace BizEvents Dashboard]**  
> *Show business metrics dashboard with revenue, conversion rates, and customer satisfaction*

**Automatically Generated:**
- **BizEvents**: Revenue and conversion tracking for each journey step
- **Service Map**: Dynamic microservices appearing based on your business flow
- **Distributed Traces**: End-to-end customer journey visibility with business context
- **Business Dashboards**: Executive-level KPI reporting and trend analysis

## 🚀 Try Your First Journey

**Quick 5-Minute Demo:**
1. Access the platform at localhost:8080
2. Enter your company details (Step 1)
3. Generate AI prompts (Step 2) 
4. Review configuration (Step 3)
5. Execute single simulation (Step 4)
6. Watch real-time business metrics and Dynatrace traces

!!! tip "Ready to Start?"
    The platform combines the simplicity of a 4-step workflow with the sophistication of enterprise observability. Perfect for demonstrations, proof-of-concepts, and business stakeholder presentations.

## 📋 Screenshot Requirements Summary

To complete this documentation, capture these key screenshots:

1. **Main App Interface**: 4-step workflow tabs
2. **Step 1**: Customer Details input form
3. **Step 2**: Generated prompts with copy buttons
4. **Step 3**: Validation dashboard with configuration options
5. **Step 4**: Both simulation modes and results
6. **Customer Personas**: 4 persona selection cards
7. **Dynatrace Integration**: BizEvents dashboard with business metrics

<div class="grid cards" markdown>
- [📚 Core Concepts :octicons-arrow-right-24:](3-concepts.md)
- [🎪 App Functionality :octicons-arrow-right-24:](app-functionality.md)
- [🧪 Advanced Features :octicons-arrow-right-24:](5-advanced-features.md)
</div>
