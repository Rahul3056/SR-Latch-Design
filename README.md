### **SR Latch Design**  

#### **Concept Overview**  
An **SR (Set-Reset) Latch** is a **fundamental sequential circuit** that stores one bit of information. It consists of **two cross-coupled NOR or NAND gates** and operates based on the **Set (S) and Reset (R) inputs**. It is widely used in **basic memory storage and control applications**.  

#### **Detailed Explanation**  
- **S = 1, R = 0 → Q = 1 (Set State)**  
- **S = 0, R = 1 → Q = 0 (Reset State)**  
- **S = 0, R = 0 → Q remains unchanged (Hold State)**  
- **S = 1, R = 1 (Invalid State for NOR, Undefined for NAND)**  

#### **Boolean Expressions**  
For **NOR-based SR Latch**:  
- `Q = NOT (S + Q')`  
- `Q' = NOT (R + Q)`  

For **NAND-based SR Latch**:  
- `Q = (S NAND Q')`  
- `Q' = (R NAND Q)`  

#### **Truth Table (NOR-Based SR Latch)**  

| S | R | Q (Next) | Q' (Next) |  
|---|---|---------|----------|  
| 0 | 0 | Q (Hold) | Q' (Hold) |  
| 0 | 1 | 0 | 1 (Reset) |  
| 1 | 0 | 1 | 0 (Set) |  
| 1 | 1 | Invalid | Invalid |  

#### **Applications**  
Used in **registers, memory storage, and control circuits** where basic bistable elements are needed.  

#### **Execution Steps**  
1. Open **QuestaSim, ModelSim, Xilinx ISE, or Vivado**.  
2. Write the **SR Latch Verilog code**.  
3. Create a **testbench** to verify the latch behavior.  
4. Simulate and check the **waveform or console output**.  

#### **Real-World Example for Practice**  
Design a **Debounce Circuit** using an SR Latch to remove noise in button press detection.  


#### **Further Enhancements**  
- Implement a **Clock-Enabled SR Latch** for better stability.  
- Design a **D Latch** by modifying the SR Latch to avoid the invalid state.
