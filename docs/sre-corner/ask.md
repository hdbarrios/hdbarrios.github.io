# Service Provided

# How to get help in #sre-corner slack channel

* Ensure it is a service SRE provide in #sre-corner.
* Post with **!ask** bot the required information as detailed as possible in slack.
* If your question is related to GovCloud,please ask in #sre-corner-gov slack channel.
* SRE will prioritize the requests accordingly based on resource availability.

<!--
* Ensure it is a service SRE provide in #sre-corner.
* Create sreint ticket with required information as detailed as possible.
* Post the sreint ticket with !ask bot and mention ticket subject in slack.
* If your question is related to GovCloud,please ask in #sre-corner-gov slack channel.
* SRE will prioritize the requests accordingly based on resource availability.-->
___
**Reminder:** Hi everyone! <img src="./img/wave.png" width="20px" />

Here’s what you need to know about requests in our MS SRE [#sre-corner](https://salesforce-internal.slack.com/archives/CGEN054QP) channel

  -  Take a look at our docs, most questions are answered there already.
  - Search the channel. Your question may have been asked before
  - Didn’t find your answer? Feel free to ask in this channel or create a Work Item in our Gus queue (product tag MS SRE ASSISTANCE REQUEST)

<img src="./img/check.png" width="20px" /> **What we handle**:

  - Encrypt/update secrets/values for production in kilonova
  - Retrieve lower environments secrets from terraform state files
  - Spinnaker Pipelines and Nexus Spinnaker repository
  - Out of Window Change Cases execution: once approved in #pccr-triage first
  - Release Change Cases execution: once approved and assigned in the respective release channel
  - Terraform pipeline (groovy build script)
  - Monitoring Cloud: tooling usage (examples, troubleshooting)

___
<img src="./img/x.png" width="20px" /> **What we don’t**:

  - Valkyr/Unified pipeline issues. Please go to <a href="https://salesforce-internal.slack.com/archives/C03UAEK0TNY">#ms-prodeng-asks</a>
  - CorePaaS/EKS platform issues. Please go to <a href="https://salesforce-internal.slack.com/archives/C02TKKV39D0" >#prodeng-run-k8s-support</a>
  - Approve Change Cases -> <a href="https://salesforce-internal.slack.com/archives/C90C7JYFN" >#pccr-triage</a>
  - Release-Related Change Cases -> Each release has its own dedicated channel. Ex: <a href="https://salesforce-internal.slack.com/archives/C04SEAC0T97" >#rel-apr-29-2023</a>
  - Manually manage AWS resources: You can ask for permission in <a href="https://salesforce-internal.slack.com/archives/CB3L3UGUU" >#ask-mulesec-engineering</a> For higher environments: you need a change case approved in <a href="https://salesforce-internal.slack.com/archives/C90C7JYFN" >#pccr-triage</a>
  - PagerDuty and incident related questions: please ask in <a href="https://salesforce-internal.slack.com/archives/C027TMP2N67" >#ms-incident-problem-ama</a>
  - All things Okta -> <a href="https://salesforce-internal.slack.com/archives/C01PS1EFTQF" >#help-bt-central</a>
  - Zscaler/cisco VPN issues -> <a href="https://salesforce-internal.slack.com/archives/C01PS1EFTQF" >#help-bt-central</a>
  - New Relic -> <a href="https://salesforce-internal.slack.com/archives/C01PS1EFTQF" >#help-bt-central</a> to add tile to Okta and <a href="https://salesforce-internal.slack.com/archives/C022UDM2PD4" >#prodeng-observability</a> for permissions
  - Gus Issues -> <a href="https://salesforce-internal.slack.com/archives/C02NYHYAX1V" >#ms-gus-support</a>
  - Nessus Manager -> <a href="#ask-tvm" >#ask-tvm</a>
  - Github access -> Concierge
  - Public nexus <a href="http://repository.mulesoft.org/nexus" >repository.mulesoft.org/nexus</a> and <a href="http://repository-master.mulesoft.org/nexus" >repository-master.mulesoft.org/nexus</a> -> Concierge
  - Access Requests for:
    - FreeIPA, Keycloak, Nexus3/Nexus, Jenkins, AWS
    - GovCloud Access Requests
    - Appgate Access/Issues
    - Anypoint Admin Console Access
    - Monitoring Cloud access requests
___
Other channels of interest -> 
<pre>
    • <a href="https://salesforce-internal.slack.com/archives/CQU8MGG3S" >#ask-idm</a>
    • <a href="https://salesforce-internal.slack.com/archives/C022UDM2PD4" >#prodeng-observability</a>
    • <a href="https://salesforce-internal.slack.com/archives/CB3L3UGUU" >#ask-mulesec-engineering</a>
    • <a href="https://salesforce-internal.slack.com/archives/C01S5N12ENN" >#prodeng-deploy</a>
    • <a href="https://salesforce-internal.slack.com/archives/C01FKLB0G2C" >#sre-govcloud-support</a>
    • <a href="https://salesforce-internal.slack.com/archives/C03UAEK0TNY" >#ms-prodeng-asks</a>
    • <a href="https://salesforce-internal.slack.com/archives/C027TMP2N67" >#ms-incident-problem-ama</a> 
</pre>
(check out their descriptions!)
___

* General Guidance on [SRE provided services](https://sre-docs.kbuild.msap.io/scope.html).

***Service NOT Provided***

* PagerDuty access is provided via Keycloak :
Please follow [MuleSoft T&P: How do I access...?](https://confluence.internal.salesforce.com/pages/viewpage.action?pageId=335280091) for related access requests. For questions please refer to [#ask-mulesec-engineering](https://salesforce-internal.slack.com/archives/CB3L3UGUU) slack channel
* Decrypt and share production environment secrets.
* Anything not limited by your user's access level.
* Anything not included in SRE team's roles and responsibilities.
* For urgent tasks, please create S4 incident and PCCR.
* `multiple releases in DEPLOYED state` please create S4 incident and PCCR (including `kstg`)
* For production breaking fix, please create S0-3 incident and PCCR.
* To understand how things work at Mulesoft as a new hire, please ask your teammates before ask in #sre-corner.

***Documentation related***

* [MuleSoft T&P: How do I access...?](https://confluence.internal.salesforce.com/pages/viewpage.action?pageId=335280091) for related access requests.

### FAQ

* For GUS Related queries, please reach out [#pki-support](https://salesforce-internal.slack.com/archives/CBZ9FA2CT) channel. 
*	CDN repository and document can be found here - [CDN Repository](https://github.com/mulesoft-ops/tf-cdn) and [Integrate Apps with CDN pipeline](https://github.com/mulesoft/anypoint-ui/blob/master/docs/cdn-build-pipeline.md) 
*	For incident reference guide, please follow [Incident Management](https://confluence.internal.salesforce.com/pages/viewpage.action?spaceKey=SRE&title=5.+Incident+Management+at+MuleSoft)  
	-	Go to the [#incident](https://mulesoft.slack.com/archives/C599RDWRF) channel and start an Incident by using the Incident bot using this command:
            [@incident-bot](https://mulesoft.slack.com/team/WJLKEH91N) start description of the incident.
  - Declare incident with severity level. Severity level and definition can be found here [Severity Definitions and Triggers](https://confluence.internal.salesforce.com/pages/viewpage.action?spaceKey=SRE&title=5.+Incident+Management+at+MuleSoft#id-5.IncidentManagementatMuleSoft-SeverityDefinitions&Triggers)
	-	Provide the incident JIRA ticket in the thread. 
	-	Reach out to the [@incident-command](https://mulesoft.slack.com/admin/user_groups) team for driving the incident.
* Getting PR approvals in [#sre-corner](https://salesforce-internal.slack.com/archives/CBZ9FA2CT)
* For PCCR reviews and approvals, please reach out [#pccr-triage](https://mulesoft.slack.com/archives/C90C7JYFN) channel.
*	For Nerdgraph API Key Requests/Questions, please reach out [#prodeng-observability](https://mulesoft.slack.com/archives/C022UDM2PD4)
* Since SRE team was assigned to be responsible for kilonova secrets in production, we changed the process to ask for CCs if something needs to be updated/deleted in production. The reason is that we had some incidents in the past executing updates in kilonova and it was asked if we had change cases for that to track the issue.
Also, when deployed by valkyr, we know there is a pre-approved change case for your deploy but that CC doesn't add the kilonova PRs for tracking/compliance.
We understand that this "CC for a PR" is not the best scenario and we are working on a Decision Record to make sure we find the best solution and share proper communication.
I hope that clarifies. Please let us know if you still have questions or comments regarding this.

## Alias

| Group | Purpose |
| ----- | ------- |
| @ms-sre-team | All SRECOM and SREGOV team members |
| @ms-sre-com | All SRECOM team members |
| @ms-sre-gov | All SREGOV team members |
| @pccr-gatekeeper | SRE's members that Approve OOW PCCRs |
| @ms-sre-com-oncall | Current SRECOM Oncall |
| @ms-sre-com-onduty | Current SRECOM Onduty |
| @sre-gov-oncall | Current SREGOV Oncall |
| @sre-gov-onduty | SRE GOV member to execute OOW gov PCCRs |
| @ms-sre-cc-executors | SRE COM member to execute OOW com PCCRs |
| @ms-sre-global-action| SRE team members on Global Actions |
| @ms-sre-engineering-support | SRE team members on Engineering Support |
| @ms-sre-hf-executors  | SRE team member Hiperforce support |
<!--| @sre-ba | SRECOM team members on ART time |-->

<!-- 
## Saltmaster
## Spinnaker
## Anypoint-webserver
## [SumoLogic](../sumologic/index.html)
## Terraform
-->