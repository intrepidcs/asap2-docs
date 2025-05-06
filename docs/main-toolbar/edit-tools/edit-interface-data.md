---
title: Edit Interface Data
description: Edit Interface Data for Measurements, Characteristics, and Axis Pts in A2L files. Link to Identifiers and enter MCD-2MC metalanguage content for tool and device setup.
keywords: [A2L interface data, IF_DATA editing, ASAP2 Editor, Measurement interface data, Characteristic interface data, Axis Point interface data, ASAM MCD-2MC, Interface Identifier]
sidebar_position: 17
sidebar_label: Edit Interface Data
---

# Edit Interface Data

MCD systems, test tools, and other interfaces may require unique data to function properly.  This interface data can describe things such as database commands, device driver information, or setup details for serial communications.  Interface Data is declared with the keyword IF\_DATA within the A2L file.\
\
The ASAP2 Editor supports interface data for [Measurements](./../create-edit-measurements), [Characteristics](./../create-edit-characteristics), and [Axis Pts](./../create-edit-axis-pts).  The data can be changed by using the Interface Data tab found in the edit dialogs for each of those A2L item types.  The Interface Data tab will appear similar to Figure 1.

<div class="text--center">

<figure>

![EditInterfaceData](../../assets/EditInterfaceData.gif "EditInterfaceData")
<figcaption>Figure 1: Example of the Interface Data tab and its edit dialog.</figcaption>
</figure>
</div>

Interface data must be linked to an Identifier created on the Interface Identifier tab on the [Project Settings](../../asap2-tools/project-settings) dialog.  After an Identifier is created, come back to the Interface Data tab and click the Append button.  An edit dialog will open to let you select an Identifier and enter interface data in the Content area.  All interface data in the Content area must use the same ASAM MCD-2MC metalanguage that is used in the A2L file.\
\
Use the OK buttons to close the dialog and save any changes.  Use the Cancel buttons to close the dialog without saving any changes.