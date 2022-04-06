#Blockchain Calculator

// SPDX-License-Identifier: UNLICENSED

pragma solidity >=0.7.0 <0.9.0;

contract HCalc {

     uint result;
    
 //To calculate tax using given amount of bitcoins and buy and sell price of trade
 
     function tax(uint x, uint y, uint z) public {
     
         result = x *3400000*9/150;
     }
 //to calculate energy footprint in kWh for bitcoin transaction
 
      function energyBTC(uint x) public {
      
         result = x *3400000*9/150;
      }   
 //to calculate energy footprint in kWh for ethereum transaction
 
      function energyETH(uint x) public {
      
         result = x *250000*495/75;
      }
  //to calculate carbon footprint in kg for bitcoin transaction
  
      function carbonBTC(uint x) public {
      
         result = x *3400000*9/150*475/1000;
      }
  //to calculate carbon footprint in kg for ethereum transaction
    
       function carbonETH(uint x) public {
        
          result = x *250000*495/75*475/1000;
       }
   //to calculate climate footprint in rupee for bitcoin transaction
    
        function climateBTC(uint x) public {
         
          result = x *31*3400000*9/150*475/1000;
        }
   //to calculate climate footprint in rupee for ethereum transaction
     
        function climateETH(uint x) public {
            
           result = x *31*250000*495/75*475/1000;
        }
   //to calculate storage needs for transactions per block with 100 TPS speed in TiB per year
      
        function storing(uint x) public {
        
           result = x *15683/1000000;
        }
        function get() public view returns (uint) {
        
           return result;
        }
}
 

