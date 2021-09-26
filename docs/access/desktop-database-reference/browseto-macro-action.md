---
title: BrowseTo-Makroaktion
TOCTitle: BrowseTo macro action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 53cc7fd0b085efee9b52d53371b08e338ccd4665
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607080"
---
# <a name="browseto-macro-action"></a>BrowseTo-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **WechselnZu** -Aktion können Sie zwischen Objekten an ihrem Ort wechseln. Zudem können Sie das Quellobjekt eines Unterformular-Steuerelements ändern, indem Sie das Argument Path to Subform Control angeben. Verwenden Sie **WechselnZu**, um von Formular1 zu Formular2 zu wechseln, ohne ein neues Fenster zu öffnen.

## <a name="setting"></a>Einstellung

Die **WechselnZu**-Aktion wird mit den folgenden Argumenten verwendet.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktionsargument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objekttyp</p></td>
<td><p>Der Objekttyp, zu dem navigiert werden soll.</p></td>
</tr>
<tr class="even">
<td><p>Objektname</p></td>
<td><p>Das Objekt, das innerhalb des Unterformular-Steuerelements geladen wird, auf das durch das Argument Path to Subform Control verwiesen wird.</p></td>
</tr>
<tr class="odd">
<td><p>Path to Subform Control</p></td>
<td><p>Wenn angegeben, der Pfad vom Hauptformular der Anwendung zum Zielunterformular-Steuerelement, das das durch das Argument Objektname angegebene Objekt lädt.</p></td>
</tr>
<tr class="even">
<td><p>Bedingung</p></td>
<td><p>Ersetzt die WHERE-Bedingung (sofern angegeben) der Objektdatenquelle.</p></td>
</tr>
<tr class="odd">
<td><p>Seite</p></td>
<td><p>Legt die Seite des Endlosformulars fest, die als aktuelle Seite bestimmt wird. Dieses Argument ist nur web.</p></td>
</tr>
<tr class="even">
<td><p>Datenmodus</p></td>
<td><p>Der Dateneingabemodus des Formulars (sofern angegeben).</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Das PathToSubFormControl-Argument muss mithilfe der Syntax im folgenden Codebeispiel angegeben werden:

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

In this example, the Main Form is the top level form in the Access client application. Das Argument Path to Sub Form Control muss alternativ Formular- und Unterformular-Steuerelementnamen angeben, die vom Hauptformular zum Unterformular-Steuerelement führen, bei dem es sich um den Container des objekts handelt, das durch das Argument Objektname angegeben wird. Each subform control specified must be a control on the form that precedes it. Der Pfad muss mit einem Unterformular-Steuerelement enden.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie Sie die BrowseTo-Aktion zum Öffnen eines Berichts in einem Unterformular-Steuerelement oder in einem Navigationssteuerelement verwenden.

**Der Beispielcode stammt von:**[Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OnError
        Go to Next
        Macro Name
    
    /* Try to load the report in the host form (frmAuthorsParameter)    */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
    
    /* if this fails, try to load it in the navigation subform     */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmMain.NavigationSubform>frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
```



