---
title: WechselnZu-Makroaktion
TOCTitle: BrowseTo Macro Action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 15009ca039d5df06bc732f4b58c066ad8f8d67c9
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603763"
---
# <a name="browseto-macro-action"></a>WechselnZu-Makroaktion

**Betrifft**: Access 2013 | Office 2013

Mit der **WechselnZu** -Aktion können Sie zwischen Objekten an ihrem Ort wechseln. Zudem können Sie das Quellobjekt eines Unterformular-Steuerelements ändern, indem Sie das Argument Path to Subform Control angeben. Verwenden Sie **WechselnZu**, um von Formular1 zu Formular2 zu wechseln, ohne ein neues Fenster zu öffnen.

## <a name="setting"></a>Einstellung

Die **WechselnZu** -Aktion wird mit den folgenden Argumenten verwendet.

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
<td><p>Der Typ des Objekts, zu dem gewechselt werden soll.</p></td>
</tr>
<tr class="even">
<td><p>Objektname</p></td>
<td><p>Das Objekt, das in dem Unterformular-Steuerelement geladen wird, auf das das Argument Pfad zu Unterformular-Steuerelement verweist.</p></td>
</tr>
<tr class="odd">
<td><p>Pfad zu Unterformular-Steuerelement</p></td>
<td><p>Wenn angegeben, der Pfad vom Hauptformular der Anwendung zum Unterformular steuern, lädt das Objekt, das durch das Argument Objektname angegeben.</p></td>
</tr>
<tr class="even">
<td><p>Where Condition</p></td>
<td><p>Ersetzt, wenn angegeben, die Bedingung der Datensatzquelle des Objekts.</p></td>
</tr>
<tr class="odd">
<td><p>Page</p></td>
<<<<<<< Kopf
<td><p>Legt, wenn angegeben, die Seite des Endlosformulars fest, die als aktuelle Seite festgelegt wird. Dieses Argument gilt nur für die Webverwendung.</p></td>
=======
<td><p>Legt, wenn angegeben, die Seite des Endlosformulars fest, die als aktuelle Seite festgelegt wird. Dieses Argument ist nur Web.</p></td>
>>>>>>>Master-Shape
</tr>
<tr class="even">
<td><p>Data Mode</p></td>
<td><p>Wenn angegeben, der Dateneingabemodus des Formulars.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Das Argument PathToSubFormControl muss mit der Syntax im folgenden Codebeispiel wird angegeben werden:

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

In diesem Beispiel bildet das Hauptformular in der Access-Clientanwendung das Formular der obersten Ebene. Der Pfad zum Formularsteuerelement Sub-Argument muss auch angeben und Unterformular Steuerelementnamen führende aus dem Hauptformular auf das Unterformular-Steuerelement, das den Container des Objekts, das durch das Argument Objektname angegeben ist. Jedes angegebene Unterformular-Steuerelement muss ein Steuerelement für das Formular darstellen, das ihm vorangestellt ist. Der Pfad muss mit einem Unterformular-Steuerelement enden.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt, wie Sie die BrowseTo-Aktion zum Öffnen eines Berichts in einem Unterformular-Steuerelement oder in einem Navigationssteuerelement verwenden.

**Beispielcode von** der [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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



