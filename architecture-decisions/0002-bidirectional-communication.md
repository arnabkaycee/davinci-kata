# Bidirectional communication with a fridge and kiosk

## Status

Proposed

## Context
We can sell offline and online via smart fridges and kiosks. We operate with fridges via API of cloud based management system, we don't work with fridges directly.
A customer should be able to use smart fridge without account in our system.
The user is identified by his/her credit/debit card used to get access to a fridge.

## Decision Drivers
1. Registered user should be able to apply coupons and use promotional pricing.
2. Fridges and kiosks should support online and offline selling including booking of sold meal until it's taken by the owner.

## Considered Options
### 1. Kiosks and fridges use our software to operate with meals.

#### Pros
1. We fully controll whole selling chain and have a freedom to change anything in this chain.
2. We can easily add loyality flows and online and offline selling since we control the chain.

#### Cons
1. Complex and expensive onboarding process for new fridges and kiosks.
2. Not all fridges support our software.
3. We are responsible for maintenance of software in fridges and kiosks.
4. Additional complexity. We need to balance between security of whole system (that can be compromised by some outdated software on edge device) and availability (let a fridge operate with outdated and not secure software).

### 2. Kiosks and fridges don't use our software to operate with meals.

#### Pros
1. We can add loyality flows in our system after a purchase is made.
2. Maintenance of fridges and kioks is not our responsibility.
3. We can add any fridge to our system that cloud based management system supports.

#### Cons
1. We cannot support online selling.
2. Hard to add anything to selling chain since we don't controll it. We can work after a purchase when we take a control.

## Decision
Kiosks and fridges use our software to operate with meals.
Rationale is that we have to support both online and offline selling.