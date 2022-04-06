# BlockchainCalculator
// SPDX-License-Identifier: MIT
pragma solidity >=0.7.0 <0.9.0;
contract Calculator_Harshit 
{
    uint result;
    //To calculate tax on your crypto transactions in India
    //Enter the amount of bitcoins, buy and sell price of your bitcoin investment
    function tax(uint x,uint y,uint z) public
    {
        result= 3*x*(z-y)/10;
    }
    //To calculate energy footprint in kWh of your bitcoin transaction per rupee
    function energyperbitcoin(uint x) public
    {
        result = x * 3400000*9/150;
    }
    //To calculate energy footprint in kWh of your ethereum transaction per rupee
    function energyperethereum(uint x) public 
    {
        result = x *250000*495/75;
    }
    //To calculate carbon footprint in kg per bitcoin transaction 
    function bitcoincarbon(uint x) public 
    {
        result = x * 430000;
    }
    //To calculate carbon footprint in kg per ethereum transaction
    function ethereumcarbon(uint x) public 
    {
        result = x * 1650000;
    }
    //To calculate climate footprint in rupee per bitcoin transaction
    function bitcoinclimate(uint x) public 
    {
        result = x * 31*430000;
    }
    //To calculate climate footprint in rupee per ethereum transaction
    function ethereumclimate(uint x) public 
    {
        result = x * 31*1650000;
    }
    //To calculate Storage needs in TiB based on transactions per block, with 100 TPS for a year
    function storingSize(uint x) public 
    {
        result = x * 15683/1000000;
    }
    function get() public view returns (uint) 
    {
        return result;
    }
}    
