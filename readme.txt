Netlist Format:

Primary Output
Circuit Name
Primary Input
OUT_NODE GATE_TYPE IN_NODE
....
END

Gate type can be:
AND
OR
NOT
XOR


Functions:
netlist_loader:
input: path (path of the .txt file containing netlist)
return: netlist as List format desired by circuit

input_file_generator:
input: path (path of the .txt file containing input)
Input format in file:
The order of input should be same as given in PI
PI0 PI1 PI2 ...
PI0 PI1 PI2 ...
.
.
.
PI0 PI1 PI2 ...
return: a list of input, as desired for logic simulation


Class circuit:
Input: Netlist
Using cicuit we can:
Can carry out logical simualtion of specified circuit.
Automatically generate a test vecctor for a given stuk at fault.

Class Functions:

output:
To carry out the logic simulation for one input
input: PI value (Format: ["PI0 VALUE","PI2 VALUE",...,"PIN VALUE"]
return: Result at output nodes

outputs:
To carry out the logic simulation for one input
input: List of input (Format: ["PI0_VALUE","PI2_VALUE",...],...]
return: None
Outputs: Print the input and output according the Input list provided

test_vector_generator:
To return Test Vector for specified Fault
Input: Fault location, Fault type
Note: Input your fault Location in the variable Fault_Location and type in SA
Output: 
	If Fault detecatable: Test Vector
			      True
	If Fault Not detectable:False
