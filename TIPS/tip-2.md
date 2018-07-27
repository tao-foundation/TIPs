---
tip: 2
title: TETHash 
status: Draft
type: Core
author: trustfarm
        https://github.com/tao-foundation/TIPs/blob/master/TIPS/tip-2.md
created: 2017-7-27
---

## TETHash Proposal.

Prevent ETHash ASIC , EIP-959 Discussion Threads, Proposal on Keccak / MIX change on ETHash for Prevent ASIC Mining.
## TIP Rationale

[github issue discussion](https://github.com/trustfarm/teo-material/issues/2)

Original Link : [ethereum/EIPs#958 (comment)](https://github.com/ethereum/EIPs/issues/958#issuecomment-377849594)
```
@pipermerriam Your proposal doesn't prevent ASIC.most of algorithm is ASIC Friendly . so, multiple algorithm in ASIC then, It is not helpful prevent asic.

@AirSquirrels good analysis of FPGA and ASIC.But, I guess Antminer F3 is not a rumors, It may be realized now.

I've heard rumors from 3Month ago,
Basically, I don't like ASIC comprehensive mining, because there's 1~2 sole vendors provide Asic miners.
If there's several many vendors and types of miner product. it may be distributed and decentralized mining in view of device using.

Recent days, I also changing the thinking, GPU only mining.becasue all GPU has dramaticcally increased prices and miner's have spent their earns for GPU and electricity fees.

@Arachnid ,
If ethash makes the ASIC resistance and prevent future ASIC attacks,I think 1st things is changing keccak to other algorithms, and change MIX algorithm to modify diffrently.

And then, modified ethash will resistants asic mining for some times.
and Next things apply and check rum-time update of newer hash algorithm. 
http://doi.org/10.8080/1020160054419 
Basic idea is dynamic updates.
please check it.
changing block format and add meta selector fields for new hash algorithms for prevent centralized hash.
If it looks good , I have mind on contributions for fair use and blockchain innovations.
```


## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
