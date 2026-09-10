---
name: pronto-rules
description: "Rules for the Pronto project"
alwaysApply: true
---

- When the user asks about storefronts or restaurants, use the `Storefront__c` SObject, not `WebStore`.
- When the user asks about orders, use the `Order__c` SObject, not `Order`.
- When the user asks about customers, use the `Contact` SObject.
