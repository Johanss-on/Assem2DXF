Assem2dxf.v3 SolidWorks Macro
Overview
Title: Assem2dxf.v3
Tooltip: Export Assembly as DXF
Author: Lucas Johansson
Year: 2024

This SolidWorks macro exports all sheet metal flat patterns from an assembly to DXF files, saved in a new folder named DXF within the assembly's root folder.

Features
Automated DXF Export: Exports flat patterns for all sheet metal components in an assembly or part.
File Naming: Customizable file naming using a template.
Configuration Handling: Supports multiple configurations within parts and assemblies.
Duplicate Handling: Avoids re-exporting existing DXF files if specified.
Installation
Download the macro file and save it to your local machine.
Open SolidWorks and go to Tools > Macro > Run....
Navigate to the saved macro file and select it.
Usage
Open the desired assembly or part document in SolidWorks.
Run the macro using Tools > Macro > Run... and select Assem2dxf.v3.
The macro will create a DXF folder in the root directory of the assembly and save the flat pattern DXF files there.
Configuration
Constants
SKIP_EXISTING_FILES: Set to True to avoid overwriting existing DXF files.
OUT_NAME_TEMPLATE: Template for naming output files. Tokens include:
_FileName_: Name of the sheet metal part file.
_FeatureName_: Name of the flat pattern feature.
_ConfName_: Configuration name.
_$CLPRP:Description_: Custom property Description from the cut list.
Flat Pattern Options
Customize the flat pattern export options using the SheetMetalOptions_e enumeration. The default options are:

ExportBendLines
ExportFlatPatternGeometry
To modify, adjust the FLAT_PATTERN_OPTIONS constant.

Error Handling
The macro includes basic error handling. If an error occurs, a message box will display the error description.

Example Output
If the assembly file is located at C:\Projects\MyAssembly.SLDASM and contains a sheet metal part Part1.SLDPRT with a flat pattern named Flat-Pattern1, the resulting DXF file might be named:

C:\Projects\DXFs\Part1_Flat-Pattern1_Default_.dxf
Code
The full code for the macro is provided for customization and debugging purposes. Advanced users can modify the code to fit specific requirements or add additional features.

License
GNU General Public License v3.0
This project is licensed under the GNU General Public License v3.0. For more details, see the LICENSE file.

Assem2dxf.v3 SolidWorks Macro
© Lucas Johansson 2024

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <https://www.gnu.org/licenses/>.
