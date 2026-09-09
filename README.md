# Log file analysis

The program reads a network log file, uses regular expressions (regex) to identify error codes, and counts how frequently each unique error pattern occurs. Results are then sorted from most to least frequent.

## Features
Reads and processes network log files
Uses Python re for pattern matching
Identifies unique error codes such as ERR404 and ERR500
Counts the frequency of each error
Sorts results by frequency
Technologies
Python
Regular Expressions (Regex)
File Handling
Dictionaries
Sorting & Data Processing
How It Works

The analyse_log() function:

Opens the specified log file
Reads each line
Searches for patterns using regex
Records the number of occurrences of each match
Returns the results as a dictionary

The program then sorts the results by frequency and displays the most common patterns first.
## Example

Given a log containing:

ERR404
ERR500
ERR404
ERR404
ERR500

The program outputs:

ERR404 3
ERR500 2

## What I Learned
This project gave me practical experience with:

Python programming
Processing and analysing log data
Regular expressions
Automating repetitive data analysis
Working with network-related data
Problem-solving in a software development environment

## Context

This project was completed as part of my 2024 work experience at CellXion Networking Company, where I gained exposure to GSM network architecture and software analysis.
