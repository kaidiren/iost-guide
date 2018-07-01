# 转账

1. 编写转账合约 示例 send.lua

   ```lua
   --- main 合约主入口
   -- 转账
   -- @gas_limit 100000
   -- @gas_price 0
   -- @param_cnt 0
   -- @return_cnt 0
   function main()
   
   -- Transfer 参数顺序 from, to, value
       Transfer("hsvEwxJtrymgVtMsXZR2ChAtWpPAozXpSW2jTjEJPKu1","2BibFrAhc57FAd3sDJFbPqjwskBJb5zPDtecPWVRJ1jxW",1.000000)
   end--f
   ```

2. `./build/iwallet compile send.lua` 

3. `./build/iwallet sign send.sc`
4. `./build/iwallet publish send.sc send.sig`

