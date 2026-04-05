# EventLogger-8
 EventLogger.sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract EventLogger {
    event NewMessage(address indexed from, string message, uint256 timestamp);

    function logMessage(string memory _message) public {
        emit NewMessage(msg.sender, _message, block.timestamp);
    }
}
