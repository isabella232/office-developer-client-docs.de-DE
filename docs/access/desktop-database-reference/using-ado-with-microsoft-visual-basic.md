---
title: Verwenden von ADO mit Microsoft Visual Basic
TOCTitle: Using ADO with Microsoft Visual Basic
ms:assetid: 5e0fb2ec-42aa-e181-386f-099607ac7400
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249338(v=office.15)
ms:contentKeyID: 48545130
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a405189f3130a24c98112f0b0d9f31c7bfa4c217
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997749"
---
# <a name="using-ado-with-microsoft-visual-basic"></a>Verwenden von ADO mit Microsoft Visual Basic

**Betrifft**: Access 2013, Office 2013

Das Einrichten eines ADO-Projekts und das Schreiben von ADO-Code verläuft bei Verwendung von Visual Basic und Visual Basic für Applikationen ähnlich. In diesem Thema wird die Verwendung von ADO mit Visual Basic und mit Visual Basic für Applikationen behandelt, und etwaige Unterschiede werden genannt.

## <a name="referencing-the-ado-library"></a>Verweisen auf die ADO-Bibliothek

Durch das Projekt muss auf die ADO-Bibliothek verwiesen werden.

### <a name="to-reference-ado-from-microsoft-visual-basic"></a>So verweisen Sie aus Microsoft Visual Basic auf ADO

1. Wählen Sie in Visual Basic im Menü **Projekt** die Option **Verweise** aus.

2. Wählen Sie **Microsoft ActiveX Data Objects x.x Library** aus der Liste aus. Überprüfen Sie, ob mindestens die folgenden Bibliotheken ebenfalls ausgewählt sind:
   
   - Visual Basic für Applikationen
   - Visual Basic-Laufzeitobjekte und -Prozeduren
   - Visual Basic-Objekte und -Prozeduren
   - OLE-Automatisierung

3. Klicken Sie auf **OK**.

Sie können ADO genauso problemlos mit Visual Basic für Applikationen verwenden, z. B. mit Microsoft Access.

### <a name="to-reference-ado-from-microsoft-access"></a>So verweisen Sie aus Microsoft Access auf ADO

1. Wählen Sie in Microsoft Access ein Modul auf der Registerkarte **Module** im Fenster **Datenbank** aus.

2. Wählen Sie im Menü **Extras** die Option **Verweise** aus.

3. Wählen Sie **Microsoft ActiveX Data Objects x.x Library** aus der Liste aus. Überprüfen Sie, ob mindestens die folgenden Bibliotheken ebenfalls ausgewählt sind:
    
   - Visual Basic für Applikationen
   - Microsoft Access 11.0-Objektbibliothek (oder höher)

4. Klicken Sie auf **OK**.

## <a name="creating-ado-objects-in-visual-basic"></a>Erstellen von ADO-Objekten in Visual Basic

Zum Erstellen einer Automatisierungsvariablen und einer Instanz eines Objekts für diese Variable können Sie zwei Methoden verwenden: **Dim** oder **CreateObject**.

### <a name="dim"></a>Dim

Sie können das **New** -Schlüsselwort mit **Dim** zum Deklarieren und Instanziieren von ADO-Objekten in einem einzigem Schritt verwenden:

```vb 
 
Dim conn As New ADODB.Connection 
```

Alternativ können die **Dim** -Anweisungsdeklaration und die Objektinstanziierung in zwei Schritten erfolgen:

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```

> [!NOTE]
> Es ist nicht erforderlich, das progid ADODB explizit zu verwenden, mit der **Dim** -Anweisung, vorausgesetzt, dass Sie ordnungsgemäß auf die ADO-Bibliothek in Ihrem Projekt verwiesen haben. Ihre Verwendung stellt jedoch sicher, dass keine Namenskonflikte mit anderen Bibliotheken auftreten.
> 
> Wenn Sie z. B. im gleichen Projekt Verweise auf ADO und auf DAO einschließen, schließen Sie wie im folgenden Code einen Qualifizierer ein, um anzugeben, welches Objektmodell beim Instanziieren von **Recordset** -Objekten verwendet werden soll:  
> 
> `Dim adoRS As ADODB.Recordset`  
>   
> `Dim daoRS As DAO.Recordset`

### <a name="createobject"></a>CreateObject

Bei der **CreateObject** -Methode müssen Deklaration und Objektinstanziierung in zwei getrennten Schritten erfolgen:

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

Mit **CreateObject** instanziierte Objekte sind spät gebunden, d. h., sie sind nicht stark typisiert, und die Vervollständigung von Befehlszeilen ist deaktiviert. Sie können jedoch die Verweise auf die ADO-Bibliothek aus dem Projekt überspringen und bestimmte Versionen von Objekten instanziieren. Beispiel:

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

Sie können dies auch erreichen, indem Sie ausdrücklich einen Verweis auf die Typbibliothek von ADO, Version 2.0, erstellen und das Objekt erstellen.

Das Instanziieren von Objekten mit der **CreateObject** -Methode ist normalerweise langsamer als die Verwendung der **Dim** -Anweisung.

## <a name="handling-events"></a>Behandeln von Ereignissen

Zum Behandeln von ADO-Ereignisse in Microsoft Visual Basic müssen Sie eine Variable auf Modulebene mithilfe des **WithEvents** -Schlüsselworts deklarieren. Die Variable kann nur als Teil eines Klassenmoduls deklariert werden und muss auf der Modulebene deklariert werden. Eine ausführlichere Erläuterung der ADO-Ereignisse behandeln, finden Sie unter [Kapitel 7: Behandeln von ADO-Ereignisse](chapter-7-handling-ado-events.md).

## <a name="visual-basic-examples"></a>Visual Basic-Beispiele

In der ADO-Dokumentation sind viele Visual Basic-Beispiele enthalten. Weitere Informationen finden Sie unter [ADO-Codebeispiele in Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).

