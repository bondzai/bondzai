<!--START_SECTION:waka-->

```txt
From: 18 July 2022 - To: 02 April 2024

Total Time: 2,505 hrs 1 min

Python                     875 hrs 36 mins ⣿⣿⣿⣿⣿⣿⣿⣿⣶⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   34.95 %
Go                         596 hrs 2 mins  ⣿⣿⣿⣿⣿⣿⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   23.79 %
JavaScript                 338 hrs 56 mins ⣿⣿⣿⣤⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   13.53 %
sh                         219 hrs 31 mins ⣿⣿⣄⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   08.76 %
Other                      182 hrs 52 mins ⣿⣷⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀⣀   07.30 %
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
