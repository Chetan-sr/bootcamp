// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract RandomSelector {
    // List of items to choose from
    string[] public items;

    // Constructor runs once at deployment
    constructor() {
        // Preload items (no input required)
        items.push("Red");
        items.push("Blue");
        items.push("Green");
        items.push("Yellow");
        items.push("Purple");
    }

    // Generate a very simple pseudo-random number
    function randomIndex() public view returns (uint256) {
        // NOTE: this is NOT secure randomness, but good for learning
        return uint256(
            keccak256(
                abi.encodePacked(
                    block.timestamp,
                    msg.sender,
                    block.prevrandao
                )
            )
        ) % items.length;
    }

    // Return a random item from the list
    function pickRandom() external view returns (string memory) {
        uint256 index = randomIndex();
        return items[index];
    }
}

