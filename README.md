# Simple-Reputation-System-Owner-Adds-Points-
Simple Reputation System (Owner Adds Points)
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/access/Ownable.sol";

contract Reputation is Ownable {
    mapping(address => uint256) public score;

    function addPoint(address user) public onlyOwner {
        score[user]++;
    }
}
