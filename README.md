<!--START_SECTION:waka-->

```txt
From: 18 July 2022 - To: 18 April 2024

Total Time: 2,585 hrs 21 mins

Python                     907 hrs 1 min   ⣿⣿⣿⣿⣿⣿⣿⣿⣷⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   35.08 %
Go                         621 hrs 39 mins ⣿⣿⣿⣿⣿⣿⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   24.05 %
JavaScript                 343 hrs 5 mins  ⣿⣿⣿⣤⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   13.27 %
sh                         234 hrs 40 mins ⣿⣿⣤⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   09.08 %
Other                      183 hrs 2 mins  ⣿⣷⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   07.08 %
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
