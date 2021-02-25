### **Catagory of MD/DFT Calculation**

- **离子间结合能**（binding energy of solvent and Li^+^）（e.g. Li^+^$\cdot$(DCM) ）：可以看出Li^+^与溶剂结合的强弱性

- **配位数**（coordination number，CN）,solvation cluster：平均配位数和Li^+^与自由溶剂的个数比例、local solvation structure

- **Li^+^扩散系数**（方法：MSD，mean-squared displacements）



### Calculation图

**正文**

| 图   | 内容                                     | 备注                                   |
| ---- | ---------------------------------------- | -------------------------------------- |
| 1    | snapshot of box                          | 投料截图                               |
| 2    | 配位数（溶剂与锂离子）                   | 不同电解质 *v.* CN                     |
| 3    | MSD（mean-squared displacement） at RT   | 计算扩散系数<br />Time(ps) *v.* MSD(A) |
| 3    | MSD（mean-squared displacement）at Low-T | 计算扩散系数<br />Time(ps) *v.* MSD(A) |

注：以上构成一张图

**SI**

| 图/表 | 内容                                  | 备注                         |
| ----- | ------------------------------------- | ---------------------------- |
| 1     | 分子式/binding energy                 | 一般是分子式＋键能           |
| 2     | binding energy比较                    | 分别由DFT与MD得出的不同结果  |
| 3     | force field type/charge（分子式）     | 不同原子的力场与电荷标注     |
| 4     | 性质表（如后附表）                    | 主要是配位数和扩散系数       |
| 5     | snapshot of MD box                    | 图                           |
| 6     | RDF（cut off distance(埃) *v.* g(r)） | radial distribution function |
| 7     | CN（cut off distance(埃) *v.* CN）    | 配位数                       |



### Computational details

**Classical molecular dynamics (MD) simulation** was used to investigate the solvation structure of electrolyte with various concentrations.

**Step 1  投料**：First, **an amorphous cell** was constructed with randomly packed LiTFSI, EA and DCM with certain ratio. 

The solution structure was then optimized with the **compass force field**.[1] 

> [1] H. Sun, J. Phys. Chem. B, 1998, 102, 7338-7364.

The force field types and the atomic charges are listed in Figure S15. 

The optimized cell was first subjected to a classical MD simulation with NPT ensemble at 298K. The converged density, calculated as the average density of the last **50 ps**, was listed in Table S5. 



The solvation shell structure of Li was determined by analyzing the **radial distribution function (RDF)** and the **coordination number (CN)** in the MD trajectory of the last **50 ps**. 

After determining the density of each electrolyte solution with the <u>NPT</u> ensemble, another classical MD simulation with <u>NVT</u> (constant volume and constant temperature) ensemble at 298K was run for to investigate the diffusion of Li in each electrolyte. 

For EA based electrolyte, the NVT simulation time was set to be 100 ps with the **mean-squared displacement (MSD)** tracked. For co-solvent electrolytes, the NVT simulation time was set to be 200 ps due to more complicated diffusion, and the MSDs are tracked during the last 100 ps to avoid short time regions when molecules are confined. By tracking the mean squared displacement (MSD), the diffusion coefficient can be represented as:

$D=\frac{1}{6N_a}\lim_{t \rightarrow \infty}\frac{d}{dt}\sum_{i=1}^{N_a}\{[r_i(t)-r_i(0)]^2\} = \frac{1}{6}\lim_{t \rightarrow \infty}\frac{d}{dt}MSD $

in which 𝑟𝑖 (𝑡) and 𝑟𝑖 (0) is the position of atom i at time t and time 0.
All the classical MD simulations were done through forcite modulus in Materials Studio. The timestep was set to be 1 fs. 



The temperature was controlled by ***Nosé algorithm*** [2] 

The pressure was controlled by ***Berendsen algorithm*** [3]. 

An ***Ewald summation*** was used for the <u>elestrostatic interaction</u>, and the van der waals interaction was truncated at 18.5 Å.

> [2] S. Nosé, Molecular Physics 1984, 52, 255–268.
>
> [3] H. J. C. Berendsen, J. P. M. Postma, W. F. van Gunsteren, A. DiNola, J. R. Haak, J. Chem. Phys. 1984, 81, 3684–3690.

***DFT计算键能（binding energy）***

Density function theory (DFT) calculation were performed to obtain the binding energy. 

A spin-polarized, all-electron, local (Double Numerical plus polarization, DNP [4]) basis set DFT implemented in Dmol3 (ref. 5) module in Materials Studio was used.

The exchange correlation was treated with the generalized gradient approximation (GGA) Perdew-Wang-91 functional. [6] 

Only the ion positions were relaxed during energy minimization, until one of the three convergence criteria, as 3 × 10−4eV/system, 0.05eV/Å, and 0.005Å for energy change, force, and displacement, respectively, was reached. To ensure the configuration of lowest energy, geometry optimization was conducted with several different initial configurations and the optimized configuration with lowest energy was selected.