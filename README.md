<!--START_SECTION:waka-->

```txt
From: 18 July 2022 - To: 29 March 2024

Total Time: 2,490 hrs 11 mins

Python                     870 hrs 34 mins ⣿⣿⣿⣿⣿⣿⣿⣿⣶⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   34.96 %
Go                         592 hrs 12 mins ⣿⣿⣿⣿⣿⣿⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   23.78 %
JavaScript                 338 hrs 24 mins ⣿⣿⣿⣤⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   13.59 %
sh                         215 hrs 5 mins  ⣿⣿⣄⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   08.64 %
Other                      182 hrs 51 mins ⣿⣷⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   07.34 %
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
