---
name: s2-memory-weaver
description: The Logic-Plane Spatiotemporal Memory Reconstructor. Generates simulated physically-anchored historical video metadata and logs spatial Six Element states to a local DB.
version: 1.0.2
---

# S2 Memory Weaver (时空回溯引擎) 交互指南

This skill provides a local SQLite database interface for memory therapy simulations. **It does NOT directly control physical hardware, HVAC, or lighting.**

## Therapy Workflow

### Step 1: Material Collection & Evolution (`upload_memory_material`)
Use this tool to log historical contexts or descriptions provided by the user into the local database. The system simulates conditional GAN progressive evolution by updating the structural similarity (SSIM) score in the ledger.

### Step 2: Genesis of Historical Video (`generate_time_space_video`)
Call this tool to generate the metadata and parameters for an Image-to-Video simulation. It records the physics-culled environmental data (Light, Air, Sound) required for the simulated historical era into the database.

### Step 3: Spatial Immersion Logging (`sync_historical_environment`)
Call this tool to retrieve the historical "Six Elements" (Lighting, Temperature, Ambient Sound) from the generated memory session.
*Boundary Note:* This tool only reads the cached parameters and outputs a simulated state. It does NOT execute external API calls or hardware actuation. Any physical syncing must be handled by external, explicitly authorized IoT daemons reading this database.