The Electronic Voting Machine (EVM) logic is designed to securely capture, store, and display votes cast by users. In a Verilog-based simulation, the system typically consists of the following components:
- Ballot Unit Logic: Detects button presses corresponding to candidates. Each button press is debounced and registered as a valid vote.
- Control Unit Logic: Manages the voting session, enabling/disabling the ballot unit, and storing vote counts. It may include a state machine to handle different phases: idle, voting enabled, vote cast, and voting closed.
- Vote Storage: Implemented using registers or memory arrays to count votes per candidate. Each candidate has a dedicated counter that increments upon a valid vote.
- Display Logic: Shows the final vote count after the voting session ends. This can be modeled using multiplexers and seven-segment display drivers or simple output registers.
The system operates synchronously with a clock signal. Inputs such as button presses and control signals are sampled on clock edges. The simulation testbench mimics user interaction by applying stimulus to input signals and observing the system's response.
Waveform analysis helps verify correct vote registration, state transitions, and final tally display.
