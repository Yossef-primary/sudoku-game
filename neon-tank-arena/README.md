# Neon Tank Arena ⚡

An action-packed, browser-only 2D cybernetic tank combat simulator engineered with pure mathematics, HTML5 Canvas, and native Web APIs. Zero external frameworks, zero media assets, and 100% client-side.

---

## 🔬 Core Engineering Features

### 1. 💥 2D Collision Physics & Ricochet Ballistics
- **Continuous Collision Detection (CCD)**: Projectile paths are raycast against geometry segments each tick, preventing tunneling through walls even at high velocities.
- **Specular Law of Reflection**: Laser shells calculate exact specular reflections off barriers ($v' = v - 2(v \cdot n)n$), allowing players and AI to score trick bank shots around corners.
- **Rigid-Body Kinematics & Momentum**: Tanks possess inertia, linear acceleration, angular steering damping, tread friction, and cannon recoil kickback.
- **Particle System**: Explosions and spark showers calculate velocity damping, alpha decay, and bloom lighting.

### 2. 🔊 100% Procedural Web Audio Synthesizer
*Zero audio files are downloaded or buffered — every sound is synthesized mathematically in real-time:*
- **Laser Fire**: Dual-wave frequency sweeps (exponential downward chirp from 880Hz to 110Hz).
- **Ricochet Chimes**: High-resonance sine waveforms with rapid envelope decay.
- **Noise-Generated Explosions**: Algorithmic white noise generated in an AudioBuffer, routed through an exponential low-pass Biquad filter sweep.
- **Dynamic Engine Hum**: Low-frequency triangular oscillator dynamically pitch-bent with tank acceleration and velocity.

### 3. 🤖 Autonomous Neural AI Opponent (`NEXUS-PRIME`)
- **Raycast Line-of-Sight (LOS)**: Real-time geometric line intersection tests to verify if the player is exposed or behind cover.
- **Predictive Target Leading**: Calculates projectile interception points based on player velocity vectors and bullet flight time.
- **Ricochet Bank-Shot Algorithm**: If direct LOS is obstructed by a pillar, the AI casts reflective bounce rays off perimeter walls to hunt for an angle that bounces into the player!
- **Whisker Obstacle Avoidance**: 5 forward sensory feelers steer the hull away from obstacles to prevent snagging on corners.
- **Evasion Subroutine**: Detects incoming player shells within close proximity and executes evasive lateral dodges.

### 4. 📈 Real-Time Animated Telemetry HUD
- **Audio Synthesizer Oscilloscope**: Connected directly to the Web Audio `AnalyserNode`, rendering live time-domain waveforms of generated sounds on an animated canvas.
- **Combat Telemetry Strip-Chart**: Rolling time-series chart plotting Player velocity against AI velocity in real time.

---

## 🎮 How to Play

| Control | Action |
| :--- | :--- |
| **W, A, S, D** or **Arrow Keys** | Drive & Steer Tank Hull |
| **Mouse Cursor** | Aim Turret Cannon |
| **Left Click** | Fire Ricochet Laser Shell |
| **Spacebar** or **Shift** | Activate Nitro Thrusters (Consumes Energy) |
| **M** | Toggle Sound On / Mute |

---

## 🚀 Running Locally & Deploying

1. **Directly in Browser**: Double-click [index.html](file:///Users/ywspswsn/Projects/AgenticProgramming/neon-tank-arena/index.html).
2. **Local Python Server**:
   ```bash
   cd neon-tank-arena
   python3 -m http.server 8080
   ```
   Then visit `http://localhost:8080`.
