<!--START_SECTION:waka-->

```txt
From: 18 July 2022 - To: 14 April 2024

Total Time: 2,572 hrs 34 mins

Python                     904 hrs 15 mins ⣿⣿⣿⣿⣿⣿⣿⣿⣷⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   35.15 %
Go                         617 hrs 18 mins ⣿⣿⣿⣿⣿⣿⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   24.00 %
JavaScript                 340 hrs 1 min   ⣿⣿⣿⣤⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   13.22 %
sh                         232 hrs 20 mins ⣿⣿⣤⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   09.03 %
Other                      183 hrs 1 min   ⣿⣷⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   07.11 %
```

<!--END_SECTION:waka-->
```cpp
CAmount GetBlockSubsidy(int nHeight, const Consensus::Params& consensusParams)
{
    int halvings = nHeight / consensusParams.nSubsidyHalvingInterval;

    if (halvings >= 64)
        return 0;

    CAmount nSubsidy = 50 * COIN;

    nSubsidy >>= halvings;

    return nSubsidy;
}
```
