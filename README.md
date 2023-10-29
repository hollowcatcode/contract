# Contract

- Chain: Polygon (MATIC)
- Contract: 0x7c56e5555cc5bfe8a17b744adebf81d11aa0dce5
- Total: 200000000000000000
- Burnable: Yes
- Minted: No

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts@4.9.3/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts@4.9.3/token/ERC20/extensions/ERC20Burnable.sol";

contract HollowCat is ERC20, ERC20Burnable {
    constructor() ERC20("HollowCat", "HOLE") {
        _mint(msg.sender, 200000000000000000 * 10 ** decimals());
    }
        function decimals() public view virtual override returns (uint8) {
        return 8;
    }
}
```
