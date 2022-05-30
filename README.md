# Shopify-FE-Question




```
const provinces = [
  {
    name:"ON",
    starters:["k","L","M","N","H"]
  },
  {
    name:"MB",
    starters:["R"]
  },
  {
    name:"NT",
    starters:["X0E","X0G","X0H"]
  },
  {
    name:"NU",
    starters:["X0A","X0B","X0C"]
  }
]

const postal_for = (postal)=>{
      let province=null
      
  for(let i=0;i<provinces.length;i++){
    const charLength = postal.charAt(0)==="X"? 3 : 1
        
      if(provinces[i].starters.includes(postal.substring(0,charLength))){
        province= provinces[i].name
        break;
      }
  }
  
  return province
}

console.log(postal_for("N2E 4K4")
//expected output = "ON"


const valid_for = (postal,province)=>{
  
  if(postal_for(postal)===province){
    return true
  }
  else{
    return false
  }
}

console.log(valid_for("H0A 4K4","ON"))
//expected output = true
```
