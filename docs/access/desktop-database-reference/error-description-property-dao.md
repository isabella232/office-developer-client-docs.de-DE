---
title: Error.Description-Eigenschaft (DAO)
TOCTitle: Description Property
ms:assetid: 47a84bec-3258-f2c7-e1af-239da39844dc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193218(v=office.15)
ms:contentKeyID: 48544601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053358
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8f4783ee1a8c54727ef0ea5995c14b2cec960ede
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920235"
---
# <a name="errordescription-property-dao"></a>Error.Description-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013
 

Gibt eine beschreibenden String-Wert zurück, der einem Fehler zugeordnet ist. Das ist die Standardeigenschaft für das Error-Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* . Beschreibung

*Ausdruck* Eine Variable, die ein **Error** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Die **Description**-Eigenschaft umfasst eine kurze Beschreibung zu einem Fehler. Weisen Sie mit dieser Eigenschaft den Benutzer auf einen Fehler hin, den Sie nicht behandeln können oder möchten.

## <a name="example"></a>Beispiel

Dieses Beispiel löst einen Fehler aus, fängt ihn auf und zeigt die Eigenschaften **Description**, **Number**, **Source**, **HelpContext** und **HelpFile** des resultierenden Error-Objekts an.

```vb 
Sub DescriptionX() 
 
 Dim dbsTest As Database 
 
 On Error GoTo ErrorHandler 
 
 ' Intentionally trigger an error. 
 Set dbsTest = OpenDatabase("NoDatabase") 
 
 Exit Sub 
 
ErrorHandler: 
 Dim strError As String 
 Dim errLoop As Error 
 
 ' Enumerate Errors collection and display properties of 
 ' each Error object. 
 For Each errLoop In Errors 
 With errLoop 
 strError = _ 
 "Error #" & .Number & vbCr 
 strError = strError & _ 
 " " & .Description & vbCr 
 strError = strError & _ 
 " (Source: " & .Source & ")" & vbCr 
 strError = strError & _ 
 "Press F1 to see topic " & .HelpContext & vbCr 
 strError = strError & _ 
 " in the file " & .HelpFile & "." 
 End With 
 MsgBox strError 
 Next 
 
 Resume Next 
 
End Sub 
 
```

