---
applicable: Exchange Server 2013, Exchange Server 2016, Exchange Online
schema: 2.0.0
---

# Get-PublicFolderMailboxDiagnostics

## SYNOPSIS
This cmdlet is available in on-premises Exchange and in the cloud-based service. Some parameters and settings may be exclusive to one environment or the other.

Use the Get-PublicFolderMailboxDiagnostics cmdlet to view event-level information about a public folder mailbox. This information can be used to troubleshoot public folder issues.

For information about the parameter sets in the Syntax section below, see Exchange cmdlet syntax (https://technet.microsoft.com/library/bb123552.aspx).

## SYNTAX

```
Get-PublicFolderMailboxDiagnostics [-Identity] <MailboxIdParameter> [-Confirm] [-DomainController <Fqdn>]
 [-IncludeDumpsterInfo] [-IncludeHierarchyInfo] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
!!! Exchange Server 2013

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Public folders" entry in the Sharing and collaboration permissions topic.

!!! Exchange Server 2016, Exchange Online

You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see Find the permissions required to run any Exchange cmdlet (https://technet.microsoft.com/library/mt432940.aspx).

## EXAMPLES

### Example 1 -------------------------- (Exchange Server 2013)
```
Get-PublicFolderMailboxDiagnostics -Identity "Customer Escalations"
```

This example returns the diagnostic information for the public folder mailbox Customer Escalations.

### Example 1 -------------------------- (Exchange Server 2016)
```
Get-PublicFolderMailboxDiagnostics -Identity "Customer Escalations"
```

This example returns the diagnostic information for the public folder mailbox Customer Escalations.

### Example 1 -------------------------- (Exchange Online)
```
Get-PublicFolderMailboxDiagnostics -Identity "Customer Escalations"
```

This example returns the diagnostic information for the public folder mailbox Customer Escalations.

### Example 2 -------------------------- (Exchange Server 2013)
```
Get-PublicFolderMailboxDiagnostics -Identity "Sales Forecasts" | Export-CSV C:\Diagnostics\SalesForecasts.csv
```

This example returns the diagnostic information for the public folder mailbox Sales Forecasts and exports the report to a CSV file.

### Example 2 -------------------------- (Exchange Server 2016)
```
Get-PublicFolderMailboxDiagnostics -Identity "Sales Forecasts" | Export-CSV C:\Diagnostics\SalesForecasts.csv
```

This example returns the diagnostic information for the public folder mailbox Sales Forecasts and exports the report to a CSV file.

### Example 2 -------------------------- (Exchange Online)
```
Get-PublicFolderMailboxDiagnostics -Identity "Sales Forecasts" | Export-CSV C:\Diagnostics\SalesForecasts.csv
```

This example returns the diagnostic information for the public folder mailbox Sales Forecasts and exports the report to a CSV file.

## PARAMETERS

### -Identity
The Identity parameter specifies the identity of the public folder mailbox. The public folder mailbox is where the content of the public folder resides.

```yaml
Type: MailboxIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: True
Position: 1
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -Confirm
The Confirm switch specifies whether to show or hide the confirmation prompt. How this switch affects the cmdlet depends on if the cmdlet requires confirmation before proceeding.

- Destructive cmdlets (for example, Remove-\* cmdlets) have a built-in pause that forces you to acknowledge the command before proceeding. For these cmdlets, you can skip the confirmation prompt by using this exact syntax: -Confirm:$false.

- Most other cmdlets (for example, New-\* and Set-\* cmdlets) don't have a built-in pause. For these cmdlets, specifying the Confirm switch without a value introduces a pause that forces you acknowledge the command before proceeding.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainController
This parameter is available only in on-premises Exchange.

The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.

```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeDumpsterInfo
The IncludeDumpsterInfo parameter specifies that diagnostic information for the \\NON\_IPM\_TREE\\DUMPSTER\_ROOT folder, which serves as the dumpster for public folder mailboxes, is included in the returned information.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeHierarchyInfo
!!! Exchange Server 2013

The IncludeHierarchyInfo switch specifies whether to include folder hierarchy information in the results. This includes the following information:

- TotalFolderCount The total number of public folders in the specified public folder mailbox.

- MaxFolderChildCount The largest number of child folders in the public folder hierarchy.

- HierarchyDepth The depth of the public folder hierarchy. The root folder is 0.

- CalendarFolderCount The number of calendar public folders.

- ContactFolderCount The number of calendar public folders.

- MailPublicFolderCount The number of mail-enabled public folders.

- NoteFolderCount The number of note public folders.

- StickyNoteFolderCount The number of sticky note public folders.

- TaskFolderCount The number of task public folders.

- OtherFolderCount The number of public folders that don't match any of the previously defined public folder types.



!!! Exchange Server 2016, Exchange Online

The IncludeHierarchyInfo switch specifies whether to include folder hierarchy information in the results. This includes the following information:

- TotalFolderCount: The total number of public folders in the specified public folder mailbox.

- MaxFolderChildCount: The largest number of child folders in the public folder hierarchy.

- HierarchyDepth: The depth of the public folder hierarchy. The root folder is 0.

- CalendarFolderCount: The number of calendar public folders.

- ContactFolderCount: The number of calendar public folders.

- MailPublicFolderCount: The number of mail-enabled public folders.

- NoteFolderCount: The number of note public folders.

- StickyNoteFolderCount: The number of sticky note public folders.

- TaskFolderCount: The number of task public folders.

- OtherFolderCount: The number of public folders that don't match any of the previously defined public folder types.



```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
The WhatIf switch simulates the actions of the command. You can use this switch to view the changes that would occur without actually applying those changes. You don't need to specify a value with this switch.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2013, Exchange Server 2016, Exchange Online

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
To see the input types that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?linkId=616387). If the Input Type field for a cmdlet is blank, the cmdlet doesn't accept input data.

## OUTPUTS

###  
To see the return types, which are also known as output types, that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?linkId=616387). If the Output Type field is blank, the cmdlet doesn't return data.

## NOTES

## RELATED LINKS

[Online Version](https://technet.microsoft.com/library/e780d809-a408-4799-8175-46946835bee4.aspx)

