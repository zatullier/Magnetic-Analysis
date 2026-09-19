# Magnet and Hall Sensor Engineering Package

This repository contains the calculation workbook, engineering package, electrical drawings, fixture CAD, printable models, and verification notes for the Magnet and Hall sensor study.

Open **Magnet_Hall_Calculator.xlsx** first. Begin with Read me, then replace the yellow example measurements in Inputs and Calibration. The file contains native formula-driven charts and has no macros or required add-ins.

**Engineering_Package.pdf** contains 22 pages: the workbook/build guide (1-3), assembly and manufactured-part drawings (4-16), sensor circuit and breadboard layouts (17-18), and calibration procedure/electrical purchase list (19-22).

## Files

- `fixture/step/`: 11 individual printed-part variants and one assembled STEP model. The models are in millimetres; COTS components in the assembly are simplified reference envelopes.
- `fixture/stl/`: matching printable parts and one assembly-reference STL. Print quantities are listed in the BOM. Do not print the assembly-reference STL. Reorient and place individual parts on the print bed in the slicer.
- `fixture/drawings/`: 13 manufacturing/assembly drawings in genuine AutoCAD 2018 DWG and editable DXF.
- `fixture/Mechanical_BOM.csv`: quantities, McMaster part numbers and source links. Default inner-face spacing is 3 mm; 1 mm and 6 mm printed alternatives are included.
- `electrical/`: two genuine DWG/DXF circuit and breadboard drawings, a connection schedule, and a blank calibration log.

## Model limits that affect the results

The distance calculation assumes centered axial motion toward each outward south face. A sideways pass needs measured field-versus-position data or an off-axis field model. Inputs can flag Lateral or Unknown so axial conclusions are suppressed. Dimensions, travel, surface readings and operating temperature are editable; the supplied CAD fits the specified 6.35 x 1.5875 mm magnets and 55100 sensor.

No actual magnet or sensor measurements were provided. Numerical example outputs are not acceptance results for your assembly. Input uncertainty allowances and the Hall active-plane depth require measurement or justification.

Grade, surface gauss and temperature alone do not establish time to failure. Lifetime remains undetermined until aging retention and duration are entered. The implemented logarithmic model assumes both magnets retain the same fraction of their initial source strength at a fixed temperature; do not use it for unequal loss. The B-H chart shows a linear recoil approximation based on assumed effective permeance coefficients, not measured lot curves or an intrinsic demagnetization knee.

The fixture is a room-temperature bench prototype. Digital checks do not establish printing accuracy or thermal stability. Its 0.01 mm micrometer graduation is not the fixture's distance uncertainty. Measure the actual zero, gap, alignment and repeatability.

## Verification performed

- Workbook: 11 in-memory boundary/reference checks, final formula-error scan, rendered sheet review, XLSX re-import, and dynamic X/Y chart-reference checks.
- Models: 11 valid individual STEP solids and watertight corresponding meshes; assembly interference checks at gaps of 0.5, 6.9125 and 13.4 mm.
- Drawings: all 15 DWGs converted with the official ODA converter and read back to DXF; entity geometry and text match the source drawings. DWG signature AC1032 (AutoCAD 2018).
- Electrical: separate output nets, 24 unique breadboard connection holes, pull-up current/power check, drawing readback and PDF visual review.

No physical build, gaussmeter measurement, lifetime test or supplier material certification was performed. Source links are in the workbook, PDF and mechanical BOM.
