# Medical Data Validator

This repository contains a simple Python script that validates medical record data using predefined rules.

## Description

`Medical Data Validator.py` verifies that a list of medical records follows a consistent structure and value format. It checks each record for required fields, correct data types, and valid content patterns.

## What it validates

Each medical record must be a Python dictionary with these keys:

- `patient_id`
- `age`
- `gender`
- `diagnosis`
- `medications`
- `last_visit_id`

Validation rules:

- `patient_id` must be a string matching `p` followed by digits (case-insensitive).
- `age` must be an integer and at least 18.
- `gender` must be a string equal to `male` or `female` (case-insensitive).
- `diagnosis` must be a string or `None`.
- `medications` must be a list of strings.
- `last_visit_id` must be a string matching `v` followed by digits (case-insensitive).

## How it works

The script defines two main functions:

- `find_invalid_records(...)` - Checks a single record's fields and returns a list of invalid keys.
- `validate(data)` - Confirms the input is a list or tuple of dictionaries, checks required keys, and reports any invalid records.

At the bottom, the script runs validation on the sample `medical_records` list.

## Usage

Run the script with Python:

```bash
python "Medical Data Validator.py"
```

If the sample records pass validation, the script prints `Valid format.` Otherwise, it prints details for each invalid record.

## Notes

- This is a simple standalone validator meant for demonstration or basic data checking.
- You can replace or extend `medical_records` with your own dataset to validate additional records.
