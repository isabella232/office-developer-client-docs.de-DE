---
title: Geeignetes Festlegen von Bereichen für Variablen in Ereignishandlern
TOCTitle: Scoping variables appropriately in event handlers
ms:assetid: 95b71535-abfd-43f1-a471-2026b522eac1
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646475(v=office.15)
ms:contentKeyID: 55119788
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8a1a418a315167cc96be5b9b5f65a0f4cd9ce44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342252"
---
# <a name="scoping-variables-appropriately-in-event-handlers"></a>Geeignetes Festlegen von Bereichen für Variablen in Ereignishandlern

Ein häufiger Fehler beim Programmieren von Ereignishandlern besteht darin, den Ereignishandler mit einem Objekt zu verbinden, das mit einem zu begrenzten Bereich für die Behandlung des Ereignisses deklariert wurde. Die Lebensdauer des Objekts muss sich nicht über nur die Funktion erstrecken, die die Rückrufmethode als Ereignishandler mit dem Objekt verbindet, sondern auch über die Rückrufmethode selbst, in der das Ereignis tatsächlich behandelt wird. Andernfalls wird die Rückrufmethode nicht aufgerufen und das Ereignis nicht wie gewünscht behandelt, wenn das Objekt außerhalb des gültigen Bereichs liegt und in der Rückrufmethode nicht mehr definiert ist.

Im folgenden Beispiel wird versucht, die MyNewInspector-Rückrufmethode mit dem [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\))-Ereignis zu verbinden. Die Rückrufmethode ist in dem Codebeispiel jedoch mit dem NewInspector-Ereignis eines [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\))-Objekts verankert, dessen Bereich auf die Connect-Funktion beschränkt ist. Wenn die Rückrufmethode schließlich aufgerufen wird, wurde die Connect-Funktion bereits beendet und das Inspectors-Objekt wurde bereits von der Garbagecollection erfasst; somit wird MyNewInspector nie aufgerufen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

class MyClass
{
    private Outlook.Application MyApp;

    public MyClass(Outlook.Application appOutlook)
    {
        MyApp = appOutlook;
    }

    // Connects the NewInspector event to my callback method
    public void Connect()
    {
        MyApp.Inspectors.NewInspector += new Outlook.
            InspectorsEvents_NewInspectorEventHandler(
            MyNewInspector);
    }

    public void MyNewInspector(Outlook.Inspector inspector)
    {
        MessageBox.Show("
            My event handler caught a NewInspector event");
    }
}
```

<br/>

Die richtige Vorgehensweise besteht in diesem Fall darin, das Inspectors-Objekt in einer dauerhafteren Variable zu speichern, deren Lebensdauer sich über die gesamte MyClass-Klasse einschließlich der MyNewInspector-Rückrufmethode erstreckt. Im folgenden Beispiel besteht der Bereich von MyInspectors in der gesamten MyClass-Klasse. So ist sichergestellt, dass die Rückrufmethode während der gesamten Lebensdauer der Klasse verbunden ist.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

class MyClass
{
    private Outlook.Application MyApp;
    private Outlook.Inspectors MyInspectors;

    public MyClass(Outlook.Application appOutlook)
    {
        MyApp = appOutlook;
    }

    // Connects the NewInspector event to my callback method
    public void Connect()
    {
        MyInspectors = MyApp.Inspectors;
        MyInspectors.NewInspector += new Outlook.
            InspectorsEvents_NewInspectorEventHandler(
            MyNewInspector);
    }

    public void MyNewInspector(Outlook.Inspector inspector)
    {
        MessageBox.Show("
            My event handler caught a NewInspector event");
    }
}
```

<br/>

Aufgrund der syntaktischen Unterschiede bei der Verbindung von Ereignishandlern in verschiedenen Sprachen tritt das Problem in Sprachen wie Visual Basic, in denen Sie ein Ereignis durch Angeben einer Instanz des übergeordneten Objekts verbinden und gleichzeitig die Rückrufmethode definieren können, seltener auf. Im folgenden Beispiel in Visual Basic wird das Handles-Schlüsselwort verwendet, um die Region\_Expanded-Rückrufmethode mit dem [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\))-Ereignis zu verbinden. Der Bereich einer Instanz des übergeordneten Objekts, Region, erstreckt sich über MyClass einschließlich der Region\_Expanded-Rückrufmethode.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook

Public Class MyClass
    ' The Region object has a lifetime spanning the class 
    ' including the callback method Region_Expanded
    Private WithEvents Region As Outlook.FormRegion
    ...
    Private Sub Region_Expanded() Handles Region.Expanded
        MsgBox("My EventHandler caught an Expanded event.")
    End Sub
End Class
```

Da in dem Beispiel die Region\_Expanded-Rückrufmethode für die Lebensdauer der Klasse mit dem Expanded-Ereignis verbunden ist, wird die Rückrufmethode wie gewünscht aufgerufen.

## <a name="see-also"></a>Siehe auch

- [Verbinden mit benutzerdefinierten Ereignishandlern](connecting-to-custom-event-handlers.md)

