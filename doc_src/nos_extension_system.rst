Nos Dual Extension System
========================

The nos shell implements a dual extension system that allows for files with either `.fish` or `.nos` extensions. This system is designed to ensure compatibility with the fish shell ecosystem while allowing for independent evolution of the nos shell.

Implementation Details
---------------------

The dual extension system operates through a file extension abstraction layer that:

1. Recognizes both `.fish` and `.nos` file extensions
2. Prioritizes `.nos` files when both exist for the same command
3. Falls back to `.fish` files when no `.nos` equivalent exists
4. Uses the same parsing engine for both file types

Usage Guidelines
---------------

This system provides several advantages:

- **Gradual Migration**: Users can selectively override fish functionalities with nos-specific enhancements
- **Backward Compatibility**: All existing fish scripts remain functional in the nos environment
- **Forward Innovation**: New nos features can be developed without modifying fish code
- **Risk Mitigation**: If fish development were to slow down, nos could continue evolving independently

The dual extension system is fundamental to the nos design philosophy of preserving value while enabling innovation.

Licensing
--------

All components of this system, including the original fish code and the nos-specific extensions, are licensed under the GNU General Public License, version 2, as described in the main license documentation.

For more information about how the dual extension system works, please see the README.md file in the nos repository.
