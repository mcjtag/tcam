# tcam
TCAM ( Ternary Content-Addressable Memory) on Verilog.

## Specifications
* Index table implemented on distributed memory (registers)
* Data table implemented on Simple Dual Port Memory (distributed or block)
* Set/Clear latency: 1
* Request latency: 3

## Parameters:
* ADDR_WIDTH     - Address width
* KEY_WIDTH      - Key and Mask width
* DATA_WIDTH     - Data width
* MASK_DISABLE   - Disable mask flag
* RAM_STYLE_DATA - ram_style attribute for data memory

## Ports

* clk       - Input clock
* rst       - Synchronous reset (active-HIGH)
* set_addr  - Input Address for Set/Clear operation
* set_data  - Input Data for Set operation
* set_key   - Input Key for Set operation
* set_xmask - Input Mask for Set operation
* set_clr   - Input Clear flag for Set/Clear operation
* set_valid - Input Valid flag for Set/Clear operation
* req_key   - Input Key for Request operation
* req_valid - Input Valid flag for Request operation
* req_ready - Output Ready flag for Request operation
* res_addr  - Output Address for Request operation
* res_data  - Output Data for Request operation
* res_valid - Output Valid flag for Request operation
* res_null  - Output Null flag for Request operation ('not found')

## Example
![TCAM](/img/timings.gif)