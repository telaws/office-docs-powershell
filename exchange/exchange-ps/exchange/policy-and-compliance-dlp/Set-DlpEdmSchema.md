---
external help file: Microsoft.Exchange.TransportMailflow-Help.xml
applicable: Office 365 Security & Compliance Center
title: Set-DlpEdmSchema
schema: 2.0.0
author: chrisda
ms.author: chrisda
ms.reviewer:
monikerRange: "o365scc-ps"
---

# Set-DlpEdmSchema

## SYNOPSIS
This cmdlet is available only in the Office 365 Security & Compliance Center. For more information, see Office 365 Security & Compliance Center PowerShell (https://technet.microsoft.com/library/mt587091.aspx).

Use the Set-DlpEdmSchema cmdlet to modify exact data match (EDM) data loss prevention (DLP) schemas in the Security & Compliance Center.

For information about the parameter sets in the Syntax section below, see Exchange cmdlet syntax (https://technet.microsoft.com/library/bb123552.aspx).

## SYNTAX

```
Set-DlpEdmSchema [-FileData] <Byte[]>
 [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
For an explanation and example of the EDM schema, see Define the schema for your database of sensitive information
 (https://docs.microsoft.com/office365/securitycompliance/create-custom-sensitive-info-type-edm#define-the-schema-for-your-database-of-sensitive-information).

You need to be assigned permissions in the Office 365 Security & Compliance Center before you can use this cmdlet. For more information, see Permissions in Office 365 Security & Compliance Center (https://go.microsoft.com/fwlink/p/?LinkId=511920).

## EXAMPLES

### -------------------------- Example 1 --------------------------
```
$edmSchemaXml = Get-Content "C:\My Documents\edm.xml" -Encoding Byte -ReadCount 0; Set-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true
```

This example modifies a DLP EDM schema. The first command reads the schema in the XML file to a variable, and the second command uses that information to modify the DLP EDM schema.

## PARAMETERS

### -FileData
The FileData parameter specifies the DLP EDM schema that you want to import.

A valid value for this parameter requires you to read the file to a byte-encoded object using the Get-Content cmdlet. For example, \(\[Byte\[\]\]\(Get-Content -Encoding Byte -Path "C:\\My Documents\\\<filename\>" -ReadCount 0\)\).

```yaml
Type: Byte[]
Parameter Sets: (All)
Aliases:
Applicable: Office 365 Security & Compliance Center
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
The Confirm switch specifies whether to show or hide the confirmation prompt. How this switch affects the cmdlet depends on if the cmdlet requires confirmation before proceeding.

- Destructive cmdlets (for example, Remove-\* cmdlets) have a built-in pause that forces you to acknowledge the command before proceeding. For these cmdlets, you can skip the confirmation prompt by using this exact syntax: -Confirm:$false.

- Most other cmdlets (for example, New-\* and Set-\* cmdlets) don't have a built-in pause. For these cmdlets, specifying the Confirm switch without a value introduces a pause that forces you acknowledge the command before proceeding.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Applicable: Office 365 Security & Compliance Center
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
The WhatIf switch doesn't work in the Office 365 Security & Compliance Center.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Applicable: Office 365 Security & Compliance Center
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  

## OUTPUTS

###  

## NOTES

## RELATED LINKS

[Online Version](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Set-DlpEdmSchema)

[Create custom sensitive information types with Exact Data Match based classification](https://docs.microsoft.com/office365/securitycompliance/create-custom-sensitive-info-type-edm)
