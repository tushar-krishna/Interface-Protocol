---------------------------------------------
Interface Protocol Design
Contact: Eric Qin < ecqin@gatech.edu>
---------------------------------------------

Summary: This is a simple RTL implementation of a strawman-like chiplet protocol. 
The aim of the protocol is to provide lightweight communication with minimal IO connections.

File Structure:
  src/chiplet_sys.v - top file connecting the fifo queues and RX / TX FSMs
  src/fifo.v - simple fifo implementation
  src/fifos_interface.v - fifos interface between Master and Slave
  src/strawman_rx_fsm.v - recieving protocol fsm
  src/strawman_tx_fsm.v - transmitting protocol fsm
  tb/tb_chiplet_sys.sv - top level testbench
  tb_fifo.v - simple fifo testbench
  tb_fifos_interface.v -simple fifo interface testbench
  
Tools Needed: 
  Verilog Compiler / Waveform Viewer of your choice:
    - Icarus Verilog
    - ModelSim
    - Verilator
    - Xilinx ISE
    - Altera Quartus
    - GTKWave
  
Alternative Online Verilog Compiler
  https://www.edaplayground.com/ 
  
To run the code, upload all of the code and similate tb_chiplet_sys.v.

This work was supported by the DARPA CHIPS program.

![alt text](https://i.postimg.cc/tJ6xFMw2/protocol.png)