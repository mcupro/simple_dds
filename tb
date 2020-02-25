 
 
 
module tb ;
reg clk =0,rst=1,clr=1;
reg [15:0] cnt=0 ;
reg [7:0]  step =1;
 
wire [11:0] sin,cos;
 
 
 
always #5 clk  = !clk ;
initial begin 
 
 
#20 {rst,clr} =0 ; 
 
cnt = 1 ;step= 1 ;   //720dot 
#360_00 ;
cnt = 0 ;step= 1 ;   //360dot 
#360_00 ;
cnt = 0 ;step= 2 ;   //180dot 
#360_00 ;
 
$finish ;
 
end 
 
  initial begin
      $dumpfile("tb.vcd");
      $dumpvars( 0 , tb );
  end
 
my_dds my_dds(
.clk(clk ) ,
.rst(rst ) ,
.clr (clr ) ,
.cnt(cnt ) ,
.step(step )  ,
.sin( sin)  ,
.cos(cos )  
); 
 
 
endmodule 
