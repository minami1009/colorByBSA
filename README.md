# colorByBSA
This script parses an XML file containing amino acid sequences and their corresponding indices, including the BURIEDSURFACEAREA value for each residue. It then uses PyMOL to color these residues based on their BURIEDSURFACEAREA values.

## Requirements
- Python 3.x
- PyMOL
- xml.etree.ElementTree (standard library)

## Usage
Open your PDB file on PyMOL and execute this by "Run Script"

### Modify the script to point to your XML file:

    tree = ET.parse('/path/to/residue1.xml')  # Update this line with your XML file path


### Color Mapping
The get_color function maps BURIEDSURFACEAREASCORE values to RGB colors, creating a gradient from blue to red.

### Deal with XML file format
        ### depend on the format of XML file, set correctly ###
        if chain == 'z':
            resi = parts[1]
        else:
            if len(parts) == 3:
                resi = parts[2]  # before 999
            else:
                resi = parts[1][1:]  # after 1000
        #######################################################

## License
This project is licensed under the MIT License.

