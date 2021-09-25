---
title: Error-Objekt – Datenzugriffsobjekte (Data Access Objects, DAO)
TOCTitle: Error Object
ms:assetid: e2608bc9-bece-9b47-4562-7a2689601f75
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835711(v=office.15)
ms:contentKeyID: 48548289
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bf880aec98b2ee64961915a22adb5cd99a72e0c7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565429"
---
# <a name="error-object-dao"></a>Error-Objekt (DAO)


**Gilt für**: Access 2013, Office 2013

Das **Error**-Objekt enthält Details zu Datenzugriffsfehlern. Dabei bezieht sich jeder Fehler auf eine einzelne Operation, an der DAO beteiligt ist.

## <a name="remarks"></a>HinwBemerkungeneise

Jede Operation, an der DAO beteiligt ist, kann mindestens einen Fehler generieren. Beispielsweise kann ein Aufruf an einen ODBC-Server zu einem Fehler des Datenbankservers, einem Fehler von ODBC und einem DAO-Fehler führen. Sobald einer dieser Fehler auftritt, wird ein **Error**-Objekt in die **Errors**-Auflistung des **DBEngine**-Objekts aufgenommen. Ein einzelnes Ereignis kann somit mehrere **Error**-Objekte ergeben, die in der **Errors**-Auflistung anzeigt werden.

Generiert eine anschließende DAO-Operation einen Fehler, wird die **Errors**-Auflistung gelöscht, und die neuen **Error**-Objekte werden in die **Errors**-Auflistung aufgenommen. DAO-Operationen, die keinen Fehler generieren, wirken sich nicht auf die **Errors**-Auflistung aus.

Die Gruppe der **Error**-Objekte in der **Errors**-Auflistung beschreibt einen Fehler. Das erste **Error**-Objekt ist der Fehler der niedrigsten Ebene (der verursachende Fehler), das zweite Objekt ist der Fehler der nächsten Ebene usw. Wenn beispielsweise beim Öffnen eines **[Recordset-Objekts](recordset-object-dao.md)** ein ODBC-Fehler auftritt, enthält das erste **Error-Objekt** ( **Errors**(0)) den ODBC-Fehler der niedrigsten Ebene. Nachfolgende Fehler enthalten die ODBC-Fehler, die von den verschiedenen ODBC-Ebenen zurückgegeben werden. In diesem Fall geben der ODBC-Treibermanager und möglicherweise direkt der Treiber gesonderte **Error**-Objekte zurück. Das letzte **Error** -Objekt - **Errors.Count -** 1 - enthält den DAO-Fehler, der angibt, dass das Objekt nicht geöffnet werden konnte.

Das Auflisten der speziellen Fehler in der **Errors**-Auflistung ermöglicht den Fehlerbehandlungsroutinen eine präzisere Ermittlung der Fehlerursache und das Durchführen der richtigen Schritte zur Wiederherstellung. Sie können die Eigenschaften des **Error**-Objekts lesen, um die folgenden Details zu den einzelnen Fehlern zu erhalten:

  - Die **[Description](error-description-property-dao.md)** -Eigenschaft mit dem Text der Fehlermeldung, die beim Abfangen des Fehlers auf dem Bildschirm angezeigt wird.

  - The **[Number](error-number-property-dao.md)** property, which contains the Long integer value of the error constant.

  - Die **[Source](error-source-property-dao.md)** -Eigenschaft, die das Objekt identifiziert, das den Fehler verursacht hat. Das ist besonders nützlich, wenn sich nach einem Aufruf der ODBC-Datenquelle mehrere **Error**-Objekte in der **Errors**-Auflistung befinden.

  - Die Eigenschaften **HelpFile** und **HelpContext**, die jeweils die betreffende Microsoft Windows-Hilfedatei und das Hilfethema (sofern vorhanden) zu dem Fehler angeben.
    

    > [!NOTE]
    > Wenn Sie beim Programmieren in Microsoft Visual Basic for Applications (VBA) das **Schlüsselwort New** verwenden, um ein Objekt zu erstellen, das anschließend einen Fehler verursacht, bevor dieses Objekt an eine Auflistung angefügt wurde, enthält die **Errors-Auflistung** des **DBEngine-Objekts** keinen Eintrag für den Fehler dieses Objekts, da das neue Objekt nicht dem **DBEngine-Objekt** zugeordnet ist. Die Fehlerinformationen sind jedoch im VBA-Objekt **Err** verfügbar. Ihr VBA-Fehlerbehandlungscode sollte die **Errors-Auflistung** untersuchen, wenn Sie einen Datenzugriffsfehler erwarten. 
    > 
    > Wenn Sie einen zentralisierten Fehlerhandler schreiben, testen Sie das VBA **Err-Objekt,** um zu ermitteln, ob die Fehlerinformationen in der **Errors -Auflistung** gültig sind. Wenn die **Number-Eigenschaft** des letzten Elements der **Errors-Auflistung** (DBEngine.Errors.Count - 1) und der Wert des **Err-Objekts** übereinstimmen, können Sie eine Reihe von **Select Case-Anweisungen** verwenden, um den jeweiligen DAO-Fehler oder die aufgetretenen Fehler zu identifizieren. Wenn sie nicht übereinstimmen, verwenden Sie die [Refresh](errors-refresh-method-dao.md) -Methode für die **Errors -Auflistung.**



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
            "  " & .Description & vbCr 
         strError = strError & _ 
            "  (Source: " & .Source & ")" & vbCr 
         strError = strError & _ 
            "Press F1 to see topic " & .HelpContext & vbCr 
         strError = strError & _ 
            "  in the file " & .HelpFile & "." 
      End With 
      MsgBox strError 
   Next 
 
   Resume Next 
 
End Sub 
 
```

