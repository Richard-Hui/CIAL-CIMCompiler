# Compiler

# AIGCIM Cimulator v1.0

# 当前版本可调的是WORDS BITS PC SCR DFF_STAGE
# 输出的性能指标基于weight全1，feature50%反转条件(相对很差的case)
# 请注意以下4个参数应该具有以下关系： 
# SCR = WORDS / (PC * WEIGHT_BW)
# WORDS = SCR * PC * WEIGHT_BW
# PC = WORDS / (SCR * WEIGHT_BW)
# WEIGHT_BW = WORDS / (SCR * PC)

['WORDS'] = "WORDS：字线（WL）, Memory阵列的行数, 内存大小等于 WORDS*BITS bit, 范围：128-4096"
['BITS'] = "BITS：位线（BL）, Memory阵列的列数, 内存大小等于 WORDS*BITS bit, 等于CIM的累加长度, 范围：8-512"
['PC'] = "PC：并行通道（Parallel Channel）, CIM并行计算的通道数, 范围：2-64"
['WEIGHT_BW'] = "WEIGHT_BW：权重位宽（Weight Bit Width）, CIM进行计算权重的位宽,  范围：4、8、16b"
['INPUT_BW'] = "INPUT_BW：输入位宽（Input Bit Width）, CIM进行计算输入的位宽, 范围：4、8、16b"
['SCR'] = "SCR：存算比（Storage Computing Ratio）, SCR个Memcell对应一个计算单元, 范围：2-64"
['BPBW'] = "BPBW：输入位并行位宽（Bit Parallel Bit Width）, CIM计算输入位并行位宽, 范围：1-INPUT_BW bit（INT仅支持1/2b）"
['DFF_STAGE'] = "DFF_STAGE：流水线级数（Pipeline Stage）, CIM阵列内的流水线级数（0-4级）, 实际对应4'b0000-4'b1111, 最低位代表WAT流水线级, 范围：0-15"
