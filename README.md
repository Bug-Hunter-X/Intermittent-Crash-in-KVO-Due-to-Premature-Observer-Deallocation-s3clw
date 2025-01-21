# Objective-C KVO Crash Bug

This repository demonstrates a subtle bug related to Key-Value Observing (KVO) in Objective-C. The bug occurs when an observer is deallocated before the observed object, leading to an intermittent crash. The crash is difficult to reproduce consistently, making debugging challenging.

## Bug Description
The bug is caused by the observed object attempting to notify a deallocated observer. This typically results in a crash, often masked by its inconsistent nature.

## Solution
The provided solution addresses the issue by ensuring proper memory management and using weak references for observers to prevent crashes.