# Proposal: LLM-Powered Spider Robot Tutor Class  
**"Vibe Coding in Robotics" – Teaching Students to Control Robots with Natural Language**

## Project Overview
This tutor class introduces students to **vibe coding** — controlling hardware through natural language commands powered by Large Language Models (LLMs). Students will command a spider robot with phrases like:

- "Crawl forward 5 steps"
- "Turn left and scan the area"
- "Dance a little wave"

The LLM translates these high-level "vibes" into precise servo instructions, making robotics accessible, fun, and creative without requiring deep low-level coding knowledge upfront.

The class combines:
- Hardware building (mechanical assembly + electronics)
- Software integration (LLM prompting + robot control code)
- Creative experimentation (designing new robot behaviors via prompts)

**Target audience**: AILT9018 students interested.

## Why Build Physical Robots?
We currently have **no working robot hardware**. To run the class effectively with hands-on experience, we need to build:
- **8 robots** for students (one per student or small team)
- **2 robots** for instructor testing, demonstration, and backup

Total: **10 identical Spider Bots** based on the provided `Spider_bot` project (README_Robot.md).

## Hardware Requirements (Per Robot)
Based on the material list in the project documentation:

| Material          | Description                          | Quantity per Robot | Unit Price (HKD) | Subtotal per Robot (HKD) |
|-------------------|--------------------------------------|--------------------|------------------|--------------------------|
| SG90 Servo       | Servo Motor                          | 8                  | 7                | 56                       |
| ESP32-S3         | Main Control Board (WiFi ready)      | 1                  | 30               | 30                       |
| 3D Prints        | Mechanical parts                     | <100 g             | 10               | 10                       |
| Battery          | Power Source                         | 1                  | 45               | 45                       |
| **Total per Robot** |                                      |                    |                  | **141 HKD**              |

**Note**: Router and PCB are shared / one-time costs (see below). Prices are taken directly from the project document (Taobao links).

## Total Cost Estimation for 10 Robots

### Per-Robot Components (x10)
- 80 × SG90 Servos: 80 × 7 = **560 HKD**
- 10 × ESP32-S3: 10 × 30 = **300 HKD**
- 3D Prints (~1 kg total filament): 10 × 10 = **100 HKD**
- 10 × Batteries: 10 × 45 = **450 HKD**
- **Subtotal (per-robot parts)**: **1,410 HKD**

### Shared / One-Time Items
- **Router** (shared for the entire class WiFi communication): 1 × 125 HKD = **125 HKD**
- **PCB** (custom control board, price TBD after design; using conservative upper estimate from document): 10 × 100 HKD = **1,000 HKD** (or lower if simple design / bulk order)

**Grand Total Estimated Cost**: **1,410 + 125 + 1,000 = 2,535 HKD**

This is an extremely budget-friendly setup (~253.5 HKD per robot on average). Actual costs may be slightly lower with bulk purchasing or current market discounts on Taobao/AliExpress.

## How This Class Helps Students

1. **Hands-on "Vibe Coding" Experience**  
   Students learn that AI can bridge natural language and physical actions. They experiment with prompting techniques, understand LLM limitations, and iteratively improve commands — building intuition for modern AI-human collaboration.

2. **Full Robotics Pipeline**  
   - Mechanical: 3D-printed parts + servo assembly  
   - Electronics: Wiring ESP32-S3 and power  
   - Software: LLM integration + control logic  
   This gives a complete view of real-world robot development, far beyond simulation.

3. **Creativity & Problem-Solving**  
   Students design new behaviors ("make the robot look happy"), debug hardware issues, and optimize prompts. It encourages creative thinking rather than rote coding.

4. **Accessibility & Engagement**  
   Natural language control lowers the barrier for beginners. Students who dislike traditional programming still feel empowered. The "spider" form factor is visually fun and motivating.

5. **Future-Ready Skills**  
   - Understanding AI + hardware integration (a growing field in robotics, IoT, and automation)  
   - Prompt engineering  
   - Basic embedded systems and mechatronics  
   - Collaborative teamwork (building and sharing robot "personalities")

6. **Low Cost, High Impact**  
   At under 2,600 HKD total, the program is scalable and repeatable. Students leave with a physical robot they helped build and "taught" to understand them — creating lasting pride and motivation for STEM.

## Implementation Flow (from README)
```mermaid
flowchart TD
    A[Human Command] --> B{LLM / AI Brain}
    B --> C[Set of Instructions]
    C --> D[Spider Robot Control Board]
    D --> E[Servo Motor]
