# Capability Map

## Purpose

A capability map, sometimes referred to as a feature map or city map, is a diagram that shows the current and future capabilities of the system. The capabilities are decomposed as a layer or block diagram where the outermost container is the problem domain and the innermost blocks are lower-level features. The capabilities in a capability map help decompose the problem domain into manageable pieces that can be developed and delivered incrementally priortized by business value.

## Electivity

This artifact is considered:  **Mandatory**

## Online Banking Capability Map

In addition to the illustration below, occasionally a textual description or inventory of the capability map is useful especially when the capabilities are not self-explanatory.

<div style="width:100%; text-align: center; border-style: solid;">

[![Banking Capability Map](/CapabilityMap/OBS_Capability_Map.svg)](https://lucid.app/lucidchart/bcabb1c2-a06f-459a-86b2-12a14fe0a01f/edit?viewport_loc=-11%2C-11%2C2027%2C1027%2C0_0&invitationId=inv_fcc2415b-1e7b-4978-88ab-28a4bf24b74b)

</div>

The latest version of Mermaid provides block diagrams that can be used to create capability maps.  The diagram below is an example of a capability map for an online banking system done with Mermaid.

<div style="width:100%; text-align: center; border-style: solid;">
<br/>

```mermaid
block-beta
    columns 1
    block:domain1
        columns 4
        block:l1num1
            columns 1
            l1title1["Account Management"]
            style l1title1 fill:#ddf5ff,stroke:#ddf5ff,color:#000;
            l2num1("Details") l2num2("Statements") l2num3("History")
        end
        block:l1num2
            columns 1
            l1title2["Transactions"]
            style l1title2 fill:#f4ffdd,stroke:#f4ffdd,color:#000;
            l2num4("Transfers") l2num5("ACH") l2num6("Wires")
        end
        block:l1num3
            columns 1
            l1title3["Bill Payment"]
            style l1title3 fill:#ffddf4,stroke:#ffddf4,color:#000;
            l2num7("Payees") l2num8("Schedule") l2num9("History")
        end
        block:l1num4
            columns 1
            l1title4["Profile Management"]
            style l1title4 fill:#ddf5ff,stroke:#ddf5ff,color:#000;
            l2num10("Preferences") l2num11("Address") l2num12("Beneficiaries")
        end
    end

    classDef l2 fill:#fff;
    classDef AvailCaps fill:#ddf5ff;
    classDef UnDevCaps fill:#f4ffdd;
    classDef FutureCaps fill:#ffddf4;
    class l2num1,l2num2,l2num3,l2num4,l2num5,l2num6,l2num7,l2num8,l2num9,l2num10,l2num11,l2num12 l2
    class l1num1,l1num4 AvailCaps
    class l1num2 UnDevCaps
    class l1num3 FutureCaps
```

<br/>
</div>
