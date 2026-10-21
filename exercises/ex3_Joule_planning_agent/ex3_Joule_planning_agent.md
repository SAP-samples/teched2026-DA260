# Using the Enterprise Planning & Simulation Agent

In this exercise, we will use Joule to do planning with us. You can follow all instructions or play around with your own ideas and prompts. It is recommended to first follow the preparation steps. 

> [!NOTE]
> The enterprise Planning & Simulation Agent is scheduled to be released on Q4 2026. In this demo, we will use the beta version of the agent that was validated in June 2026. It has known limitations and sometimes is unstable. In case of system issues during the hands-on, we will fall back to a demo provided by the instructors on another tenant. Known limitations are:
> - A table must be selected in the story when asking Joule to do planning.
> - A public edit version must be available

> [!NOTE]
> What can the agent do?
> 
> The Planning Agent assists users in complex planning workflows including assessing risk, generating new plans and forecasts, and simulating different scenarios using natural language input.
> Accelerate planning cycles and improve forecast accuracy by enabling planners to simulate scenarios, generate forecasts, incorporate external data, and execute data actions through natural language.
> Example prompts:  ”Increase Revenue by 20% in 2026, but freeze Q1” or “Forecast shows that I will not achieve the annual plan target.  Please propose some adjustments to return to plan”

> [!NOTE]
> What other agents are planned in SAP Analytics Cloud?
> - Data Action Design Agent
> - Analytics and Planning Modeling Agent
> - Data and Analytics Insights Agent
> - Analytics Narrative Agent


## Prepare plan version and table
> [!NOTE]
> Joule can create new versions. Adding a version upfront is more straight-forward to start planning given the used beta state of the agent. Feel free to try out version creation with Joule by yourself!

1. Open version management.
![](../images/ex3_1.png)

2. Add new blank public version and call it 'DA260_Forecast'. Assign the 'Forecast' category. 

![](../images/ex3_2.png)
![](../images/ex3_3.png)

3. In the version management panel, start the edit mode on this version. Do not customize the planning area. 
![](../images/ex3_4.png)
![](../images/ex3_5.png)

> [!WARNING]
> Ignoring the planning area is not best practice in customer projects. In real life, use the planning area to optimize performance.

4. Close the side panel.
![](../images/ex3_6.png)

The version should be displayed on the table as we did not set a filter on versions when designing the table. 

## Joule

Say hi to Joule! See how to start a new conversation and handle a common error of the beta version. 
![](../images/ex3_J1.gif)
