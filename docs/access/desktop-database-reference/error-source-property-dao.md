---
title: Error.Source-Eigenschaft (DAO)
TOCTitle: Source Property
ms:assetid: 3c101cac-278e-025e-55a4-8a9d1ee7db3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192677(v=office.15)
ms:contentKeyID: 48544302
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053360
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 6d8b672d20e4bbf82acbe2dd2850c2a5be256e94
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589575"
---
# <a name="errorsource-property-dao"></a>Error.Source-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013


Gibt den Namen des Objekts zurück, das den Fehler ursprünglich erzeugt hat.

## <a name="syntax"></a>Syntax

*Ausdruck* . Quelle

*expression* Eine Variable, die ein **Error**-Objekt darstellt.

## <a name="remarks"></a>Hinweise

Der Wert der **Source**-Eigenschaft ist gewöhnlich der Klassenname oder die Programm-ID des Objekts. Mit der **Source**-Eigenschaft können Sie dem Benutzer Informationen darüber liefern, ob der Code Fehler behandeln kann, die von einem Objekt in einer anderen Anwendung erzeugt wurden.

Wenn Sie beispielsweise auf Microsoft Excel zugreifen und der Fehler "Division durch Null" generiert, legt Microsoft Excel **Error.Number** auf den Microsoft Excel-Code für diesen Fehler fest und legt die **Source-Eigenschaft** auf Excel fest. Anwendung. Wenn ein Fehler von einem anderen von Microsoft Excel aufgerufenen Objekt erzeugt wird, fängt Microsoft Excel den Fehler ab und setzt **Error.Number** dennoch auf den Microsoft Excel-Code. Die anderen Eigenschaften des **Error**-Objekts (einschließlich **Source**) behalten jedoch ihre Werte, die von dem Objekt festgelegt wurden, das den Fehler erzeugt hat. Die **Source**-Eigenschaft enthält immer den Namen des Objekts, das den Fehler ursprünglich erzeugt hat.

Basierend auf der gesamten Fehlerdokumentation können Sie Code schreiben, der den Fehler angemessen behandelt. Wenn Ihre Fehlerbehandlung fehlschlägt, können Sie den Fehler mithilfe der Informationen des **[Error](error-object-dao.md)** -Objekts für den Benutzer beschreiben. Hierzu können Sie die **Source**-Eigenschaft und die anderen **Error**-Eigenschaften verwenden, um den Benutzer darüber zu informieren, welches Objekt den Fehler ursprünglich verursacht hat, eine Fehlerbeschreibung zu liefern usw.


> [!NOTE]
> Das **On Error Resume Next**-Konstrukt ist möglicherweise **On Error GoTo** vorzuziehen, wenn Fehler behandelt werden, die während des Zugriffs auf andere Objekte erzeugt wurden. Wenn das **Error**-Objekt nach jeder Interaktion mit einem Objekt überprüft wird, kann jeder Zweifel darüber aus dem Weg geräumt werden, auf welches Objekt der Code beim Auftreten des Fehlers zugegriffen hat. Auf diese Weise wissen Sie, welches Objekt den Fehlercode in **Error.Number** geschrieben und welches Objekt den Fehler ursprünglich erzeugt hat (**Error.Source**).

## <a name="example"></a>Beispiel

Dieses Beispiel löst einen Fehler aus, fängt ihn auf und zeigt die Eigenschaften **Description**, **Number**, **Source**, **HelpContext** und **HelpFile** des resultierenden **Error**-Objekts an.

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
