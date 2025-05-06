---
title: Symbols Tools
description: Use Symbols tools in ASAP2 Editor to load ECU map files, access recent files, and apply enumerated states for clearer symbol array representation.
keywords: [ASAP2 Editor symbols, ECU map file import, ELF DWARF, IEEE-695, KEIL 166, OMF 166, TI COFF, symbol tree, Enum Association, symbol array naming, symbol tools]
sidebar_position: 4
sidebar_label: Symbols Tools
---

# Symbols Tools

The Symbols group (Figure 1) in the [main toolbar](/main-toolbar) contains tools for the [Symbol area](../symbol-tree) of the editor.  Refer to Table 1 for a brief description of each selection.

<div class="text--center">

<figure>

![SymbolsTools](../assets/SymbolsTools.gif "SymbolsTools")
<figcaption>Figure 1: The Symbols toolbar group.</figcaption>
</figure>
</div>

#### Table 1: Symbols Tools

| **Symbols Tool** | **Hotkey** | **Description**                                                                                                                                                                                                                                       |
|------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Load             | n/a        | Load all symbols from an ECU map file that is in one of these formats: <br/> • IEEE\-695 \(\*\.abs or \*\.695\) <br/> • ELF/DWARF \(\*\.elf\) <br/> • TI COFF/DWARF \(\*\.out\) <br/> • KEIL 166 \(\*\.m66\) <br/> • OMF 166 \(\*\.omf\)              |
| Recent Files     | n/a        | Load one of the 10 most recently opened ECU map files\.                                                                                                                                                                                               |
| Enum Association | Ctrl\+L    | Open dialog to apply enumerated states to symbol arrays\.  Please read below for further details\.                                                                                                                                                    |


Elements within symbol arrays are initially displayed with generic names and index numbers like that shown in Figure 2. The Enum Association tool applies more descriptive names to the symbol array elements.

<div class="text--center">

<figure>

![EnumAssociation](../assets/EnumAssociation.gif "EnumAssociation")
<figcaption>Figure 2: Apply the Enum Association tool to get descriptive names for array elements.</figcaption>
</figure>
</div>

**To Apply Enumerated States to Symbol Arrays**:

1. Click the Enum Association tool button to open the dialog.
2. Drag and drop the array branch \[#] from the Symbols tree onto the dialog.
3. Click in the Enum Name cell and select the desired enumeration declaration.
4. Click the Apply button.

Use the Cancel button to restore all symbol array elements back to their generic names and index numbers.