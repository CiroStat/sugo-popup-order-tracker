SUGO Pop-up Order Tracker

A lightweight operational tracking and analytics tool designed for pop-up food events.

The application is not a POS system and does not handle payments. SUGO already relies on the POS systems of the restaurants, bars and venues hosting our events. This application was built to solve a different problem: independently tracking products served during each event and turning that activity into structured, analysable data.

Why I Built This

SUGO regularly participates in pop-ups, food markets and temporary collaborations with restaurants and other venues.

During these events, payments are normally handled by the hosting venue through its own POS system. They add our menu to their system, customers pay them directly, and at the end of the event we reconcile the sales.

The problem was that we did not have an independent and reliable way to track what we were actually serving.

In practice, this sometimes created discrepancies. An item could leave the counter without being correctly recorded, someone could forget to charge a customer, or a sale could otherwise be difficult to reconcile at the end of service.

To protect ourselves from these situations, we started keeping our own records. Initially, that often meant handwritten notes and pieces of paper.

That solution introduced a new set of problems. During busy service it was easy to forget to write something down, handwriting was not always easy to interpret afterwards, and calculating totals required manually reconstructing the entire event product by product.

More importantly, the information generated during every event was being lost.

We had transactions happening in front of us, but no structured dataset from which we could analyse performance, create KPIs, compare locations or study how the business evolved over time.

I therefore decided to build a tool specifically around our workflow rather than forcing our workflow into an existing restaurant management system.

The objective was to keep the operational experience extremely informal and flexible while making the data generated behind it structured and useful.

Project Objectives

The project has four main objectives:

* Create an independent record of what is sold during each event.
* Make end-of-event reconciliation with hosting venues faster and more transparent.
* Replace handwritten tracking with a fast and flexible mobile interface.
* Transform live operational activity into structured data that can be analysed afterwards.

Why This Project Matters

The immediate benefit is operational: fewer handwritten notes, faster reconciliation and a clearer record to share with the venues we collaborate with.

The longer-term value is the dataset.

Each event generates information about transactions, products, inventory, locations, time and sales composition. By collecting this information consistently, the business can begin to build historical data rather than treating every pop-up as an isolated event.

This creates the foundation for:

* business KPIs;
* product performance analysis;
* recurring-location comparisons;
* inventory analysis;
* cross-sectional transaction analysis;
* time-series analysis across events;
* demand forecasting;
* better production and event-planning decisions.

The application is therefore both an operational tracking tool and a data collection system for future business analytics.

The real value of the tracker is not only the interface used during service, but the structured dataset created behind every event.

Current Scope

The current version supports the complete workflow of a temporary food event:

Event setup
Each event records its name, date, venue and settlement agreement. Recurring venues can be associated through stable location identifiers, allowing performance at the same location to be analysed over time.

Reusable event menus
Menus can be created from scratch or loaded from reusable presets. Products can have prices, starting quantities and optional customisations.

Live sales tracking
During service, each transaction receives a unique ID. Products are added quickly from a mobile-friendly interface, party size can optionally be recorded, and revenue can be hidden for privacy when customers are in front of the counter.

Inventory tracking
Starting quantities can be recorded for individual products. Available quantities decrease as products are sold, while remaining flexible enough to allow additional portions to be added during service.

Combo management
Temporary combinations can be created from existing products. Selling a combo consumes the corresponding quantities of its underlying components.

Live menu editing
Prices, quantities and products can be modified while an event is running without changing historical prices in transactions that have already been completed.

Event reconciliation
At the end of the event, the application calculates revenue, venue share and the amount due to the hosting venue.

Data export
The system produces structured datasets for orders, order items, inventory and transaction-level analysis, together with a venue settlement PDF.

Data Outputs

The full event export currently contains:

* orders.csv — one observation per transaction;
* order_items.csv — item-level transaction data;
* analytics.csv — transaction-level analytical dataset;
* inventory_summary.csv — inventory consumption and adjustments;
* settlement_report.pdf — venue-facing reconciliation report.

This separation preserves granular transactional data while also providing datasets that can be used directly for analysis.

Tech Stack

The current prototype is intentionally lightweight:

* HTML
* CSS
* Vanilla JavaScript
* Browser Local Storage
* jsPDF
* JSZip
* Git / GitHub
* GitHub Pages

The project currently prioritises speed, flexibility and ease of use during live events over architectural complexity.

Roadmap

This repository will continue to evolve based on actual use during SUGO events.

Planned areas of development include:

* improved mobile UX based on real event feedback;
* stronger data validation and persistence;
* offline-first functionality;
* cloud storage and multi-device synchronisation;
* automated analytics dashboards;
* event and location performance analysis;
* inventory and production analytics;
* demand forecasting.

Status

The project is currently in active development and is being tested through real pop-up workflows.

Feedback from actual event use will guide future iterations.
