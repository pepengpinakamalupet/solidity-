contract StarToken {

    
        string public name = "StardenHardenBurdenBartz";
        string public abbrv = "Star";
        uint public supply = 0;
    
        mapping(address => uint) public blnc;
    
        function mint(address add, uint val) public {
        supply += val;
        blnc[add] += val;
        }
    
        function burn(address add, uint val) public {
            if(blnc[add] >= val){
                supply -=val;
                blnc[add] -= val;
            }
        }
}
