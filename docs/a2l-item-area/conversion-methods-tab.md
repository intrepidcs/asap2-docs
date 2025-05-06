---
title: Conversion Methods Tab
description: Define and manage COMPU_METHOD entries in the Conversion Methods tab. Supports formulas, interpolation tables, and rational functions for A2L-based data conversion.
keywords: [Conversion Methods tab, COMPU_METHOD, A2L conversion, ASAP2 editor, RAT_FUNC, FORM, TAB_INTP, TAB_VERB, ECU calibration, conversion formula, interpolation]
sidebar_position: 23
sidebar_label: Conversion Methods Tab
---

# Conversion Methods Tab

Conversion Methods are formulas and tables applied to [Measurements](../measurements-tab), [Characteristics](../characteristics-tab), and [Axis Pts](../axis-pts-tab).  They are declared with the keyword COMPU\_METHOD within the A2L file.\
\
The Conversion Methods tab has a table to display all A2L file Conversion Method items and their properties.  Each row (below the 1st filtering row) defines a Conversion Method and each column is a property.  The default column configuration is shown in Figure 1.

<div class="text--center">

<figure>

![ConMethodsTab](../assets/ConMethodsTab.gif "ConMethodsTab")
<figcaption>Figure 1: The Conversion Methods tab in the A2L file item area.</figcaption>
</figure>
</div>

Columns in the table can be filtered, reorganized, added, and hidden.  These [table features](/a2l-item-area) are common across all tabs in this area.\
\
To add items to the table you can:

* Use the [Create](../../main-toolbar/edit-tools/) tool or [right click menu](../a2l-item-right-click-menu) selection.
* [Import](../../main-toolbar/asap2-tools/) an existing A2L file.

To edit items already in the table with the [Edit Conversion Methods](../../main-toolbar/edit-tools/create-edit-conversion-methods) dialog you can:

* Double click on a cell in the table.
* Use the [Edit](../../main-toolbar/edit-tools/) tool or [right click menu](../a2l-item-right-click-menu) selection.

Refer to Table 1 below for a description of each column on the Conversion Methods tab.

#### Table 1: Column Descriptions for the Conversion Methods Tab

| Default Columns | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name            | Unique identifier of the Conversion Method.<br/><br/>Here are the main requirements for this field:<br/><br/><ul><li>Max overall length = 1024 characters.</li></ul><ul><li>Max partial string length = 128 characters.</li></ul><ul><li>Allowed characters: A - Z, a - z, 0 - 9, underscores, periods, and brackets [ ].</li></ul><ul><li>Must NOT contain spaces.</li></ul><ul><li>First character must be a letter or an underscore.</li></ul><ul><li>Any brackets must occur in pairs at the end of a partial string.</li></ul><ul><li>Any bracket pairs must surround a number or string.</li></ul><ul><li>Name is case sensitive. (i.e. "b" and "B" are considered unique)</li></ul><br/><br/>If in doubt about valid names, please refer to the ASAM specifications. |
| Type            | The ASAP2 Editor supports 5 types of conversions:<br/><br/><ul><li>TAB_INTP - table with interpolation.<br/><br/></li></ul><ul><li>TAB_NOINTP - table without interpolation.<br/><br/></li></ul><ul><li>TAB_VERB - verbal conversion table.<br/><br/></li></ul><ul><li>RAT_FUNC - fractional rational function f(x)=(axx + bx + c)/(dxx + ex + f), where coefficients 'a' through 'f' are specified properties.<br/><br/></li></ul><ul><li>FORM - formula as specified in the Formula property.</li></ul>                                                                                                                                                                                                                                                                      |
| Format          | Display formatting applied to numerical values.  This Format will be overridden by any Format properties specific to [Measurements](../../main-toolbar/edit-tools/create-edit-measurements), [Characteristics](../../main-toolbar/edit-tools/create-edit-characteristics), and [Axis Pts](../../main-toolbar/edit-tools/create-edit-axis-pts).<br/><br/>The syntax for this field is: %Length.Layout<br/><br/><ul><li>Length = overall length</li></ul><ul><li>Layout = number of decimal places</li></ul>                                                                                                                                                                                                                                    |
| Unit            | A physical unit label like Volts, RPM, kph, etc.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Formula         | Formula specified as a function of x. <br/><br/>Multiple references use syntax X1, X2, X3, etc where X1 references the first input, X2 the second, etc.  If there is only one reference in the formula then X can be used instead of X1.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Coeffs          | Coefficient values for the Conversion Type = RAT_FUNC.<br/>f(x)=(axx + bx + c)/(dxx + ex + f)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| RefTable        | Table used for the TAB\_x conversion types.  Dropdown selections come from the [Verbal Conversion Tables](../../a2l-item-area/verbal-conversion-tables-tab) tab.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

| Hidden Columns | Description             |
| -------------- | ----------------------- |
| LongIdentifier | Comment or description. |