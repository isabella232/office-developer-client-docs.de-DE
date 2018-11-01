---
title: Errors Collection (DAO)
TOCTitle: Errors Collection
ms:assetid: d42007b5-6410-14e9-baf9-9306fdef38f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834805(v=office.15)
ms:contentKeyID: 48547929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: debc3554fb63ab379bbc94bc8d44e2239eb32dd4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885752"
---
# <a name="errors-collection-dao"></a>Errors Collection (DAO)


**Betrifft**: Access 2013, Office 2013

Eine **Errors**-Auflistung enthält alle gespeicherten **Error**-Objekte, die sich jeweils auf eine einzelne DAO-Operation beziehen.

## <a name="remarks"></a>Bemerkungen

Jede Operation, die DAO-Objekte betrifft, kann Fehler generieren. Wenn ein Fehler auftritt, werden eines oder mehrere der **Error**-Objekte in der **Errors**-Auflistung des **DBEngine**-Objekts abgelegt. Wenn eine andere DAO-Operation einen Fehler generiert, wird die **Errors**-Auflistung gelöscht, und der neue Satz von **Error**-Objekten wird in der **Errors**-Auflistung abgelegt. Das Objekt mit der höchsten Zahl in der **Errors**-Auflistung (DBEngine.Errors.Count - 1) entspricht dem Fehler, der vom VBA-Objekt (Microsoft Visual Basic für Applikationen) **Err** gemeldet wird.

DAO-Operationen, die keinen Fehler verursachen, haben keine Auswirkung auf die **Errors**-Auflistung.

Im Gegensatz zu anderen Auflistungen werden an die **Errors**-Auflistung keine Elemente angefügt. Die **Errors**-Auflistung unterstützt daher nicht die Methoden **Append** und **Delete**.

Der Satz von **Error**-Objekten in der **Errors**-Auflistung beschreibt jeweils einen Fehler. Das erste **Error**-Objekt bezieht sich auf den Fehler unterster Ebene, das zweite Objekt auf die nächsthöhere Ebene usw. Wenn beispielsweise beim Versuch, ein **[Recordset](recordset-object-dao.md)** -Objekt zu öffnen, ein ODBC-Fehler auftritt, enthält das erste Fehlerobjekt den ODBC-Fehler der untersten Ebene. Nachfolgende Fehler enthalten die ODBC-Fehler, die von den verschiedenen ODBC-Ebenen zurückgegeben werden. In diesem Fall werden vom ODBC-Treibermanager und möglicherweise vom Treiber selbst separate **Error**-Objekte zurückgegeben. Das letzte **Error**-Objekt enthält den DAO-Fehler, der angibt, dass das Objekt nicht geöffnet werden konnte.

Dadurch, dass die genauen Fehler in der **Errors**-Auflistung aufgeführt werden, können die Fehlerbehandlungsroutinen die Fehlerursache genauer bestimmen und entsprechende Wiederherstellungsschritte einleiten.


> [!NOTE]
> [!HINWEIS] Wenn Sie das Objekt, das entweder vor oder während des Einfügens in die **Errors**-Auflistung einen Fehler verursacht, mit dem Schlüsselwort **New** erstellt haben, enthält die Auflistung keine Fehlerinformationen zu diesem Objekt, da das neue Objekt nicht dem **DBEngine**-Objekt zugeordnet ist. Die Fehlerinformationen sind jedoch im VBA-Objekt **Err** verfügbar.

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

