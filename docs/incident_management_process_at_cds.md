# Incident Management Process at CDS

Whenever an employee at CDS thinks that something is wrong, they can trigger an incident.

They do this by typing `/incident {what went wrong}` and hitting enter in Slack.

This triggers our SRE-bot to perform the following actions:

1. Create a new slack channel with the title #incident-{date}-{what went wrong};
1. Start a new persistent video chat Google Meet;
1. Open a new Google Doc using our incident management template, found in our incident repository in Google Drive;
1. Share links to the video chat and document in the new slack channel;
1. Add an entry into our incident tracking spreadsheet;
1. Assign the person who opened the incident as **Incident Commander (IC)** and as the **Operations Lead (OL)**; and
1. Post a message in our #incident-sre channel.

## Fixing what’s wrong

>“Fast, frequent, and safe deployments are the hallmark of great software operations. Why? Because these changes are easier to reason about, go wrong less often, and grant engineering teams energy and momentum.”

Source: https://increment.com/reliability/high-performing-team-trust/

Typically, the IC will immediately assign the OL role, contact comms, and contact people who need to be a part of resolving this incident.

Everyone who is interested or can help is able to join the incident response, but the IC is in charge and has authority over work done.

As work starts on the incident, the IC or a delegated member of the incident will document work being done and incident members will also post what they’re doing to the Slack channel so we can track what’s being done.

Depending on what incident happened, we can mitigate or fix the incident right away.

Because we have automated the checks, tests, and deployments of our systems, we are able to make changes to production very quickly.

## Blameless Postmortem

> “Feedback occurs when outputs of a system are routed back as inputs as part of a chain of cause-and-effect that forms a circuit or loop.”

Source: https://en.wikipedia.org/wiki/Feedback

Once the immediate emergency is resolved, we meet to review the incident.

During the blameless postmortem, we review the incident document where we took notes during the incident.

**You can find our template here:** [Product Incident Report Template.]()

We start at the top and work our way down. The format of the document and what is captured in it also guides us in discussing the incident in a logical manner.

We review the incident for the following things:

- The “What happened”
- The “What the impact of the incident was on the organization”
- The “How it was discovered”
- The “How was the incident triggered”
- The “What the root cause of the incident was”
- The “What we did wrong, what we did well, and how we got lucky”
- The “What action items did we do and do we still have to do”.

The action items out of this incident get added to the backlogs of the teams that own them, and are then prioritized and worked on.

Not everything is equally important and has to be fixed right away.Rotating a key that can only be compromised if they have access to our servers is important but it can wait for a sustainable fix to be put in place.Whereas a key that can be compromised from the internet can't wait and needs to be rotated right away, regardless of whether there is an easy way to change it or not.

The blameless postmortem closes the feedback loop on the incident and ensures that this incident is less likely to happen again in the future, and that we will be better prepared if it – or something similar – happens again.

## Important Principles

We strongly believe in and strive to practice the following principles:

### 1. Assuming best intentions.

No one at CDS is trying to break things, everyone is doing the best job with the information they have available to them.

### 2. Being blameless.

Things going wrong at CDS are organizational failures.
They happen because we did not put in place things to stop it from happening.

### 3. Assuming everything is going to break.

It doesn't matter what we do, something somewhere is always going to break.
