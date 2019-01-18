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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708137"
---
# <a name="scoping-variables-appropriately-in-event-handlers"></a><span data-ttu-id="c7c01-102">Geeignetes Festlegen von Bereichen für Variablen in Ereignishandlern</span><span class="sxs-lookup"><span data-stu-id="c7c01-102">Scoping variables appropriately in event handlers</span></span>

<span data-ttu-id="c7c01-p101">Ein häufiger Fehler beim Programmieren von Ereignishandlern besteht darin, den Ereignishandler mit einem Objekt zu verbinden, das mit einem zu begrenzten Bereich für die Behandlung des Ereignisses deklariert wurde. Die Lebensdauer des Objekts muss sich nicht über nur die Funktion erstrecken, die die Rückrufmethode als Ereignishandler mit dem Objekt verbindet, sondern auch über die Rückrufmethode selbst, in der das Ereignis tatsächlich behandelt wird. Andernfalls wird die Rückrufmethode nicht aufgerufen und das Ereignis nicht wie gewünscht behandelt, wenn das Objekt außerhalb des gültigen Bereichs liegt und in der Rückrufmethode nicht mehr definiert ist.</span><span class="sxs-lookup"><span data-stu-id="c7c01-p101">A common mistake in programming event handlers is connecting the event handler to an object that has been declared with a scope too limited for the purpose of handling the event. The object must have a life that spans not just over the function that connects the callback method as an event handler of the object, but also over the callback method itself where the event is actually handled. Otherwise, if the object is out of scope and is no longer defined in the callback method, the callback method is not called and the event is not handled as desired.</span></span>

<span data-ttu-id="c7c01-106">Im folgenden Beispiel wird versucht, die MyNewInspector-Rückrufmethode mit dem [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\))-Ereignis zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="c7c01-106">The following example attempts to connect the MyNewInspector callback method to the [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)) event.</span></span> <span data-ttu-id="c7c01-107">Die Rückrufmethode ist in dem Codebeispiel jedoch mit dem NewInspector-Ereignis eines [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\))-Objekts verankert, dessen Bereich auf die Connect-Funktion beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="c7c01-107">However, the callback method is hooked up in the code sample to the NewInspector event of an [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) object that has a scope limited to the Connect function.</span></span> <span data-ttu-id="c7c01-108">Wenn die Rückrufmethode schließlich aufgerufen wird, wurde die Connect-Funktion bereits beendet und das Inspectors-Objekt wurde bereits von der Garbagecollection erfasst; somit wird MyNewInspector nie aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c7c01-108">When the callback method is eventually called, the Connect function has already exited, the Inspectors object has already been garbage collected, and so MyNewInspector is never called.</span></span>

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

<span data-ttu-id="c7c01-p103">Die richtige Vorgehensweise besteht in diesem Fall darin, das Inspectors-Objekt in einer dauerhafteren Variable zu speichern, deren Lebensdauer sich über die gesamte MyClass-Klasse einschließlich der MyNewInspector-Rückrufmethode erstreckt. Im folgenden Beispiel besteht der Bereich von MyInspectors in der gesamten MyClass-Klasse. So ist sichergestellt, dass die Rückrufmethode während der gesamten Lebensdauer der Klasse verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c7c01-p103">The correct thing to do in this case is to store the Inspectors object in a more permanent variable whose lifetime spans over the entire MyClass, including the MyNewInspector callback method. In the following example, MyInspectors has a scope of the entire MyClass and ensures that the callback method is connected for the lifetime of the class.</span></span>

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

<span data-ttu-id="c7c01-111">Aufgrund der syntaktischen Unterschiede bei der Verbindung von Ereignishandlern in verschiedenen Sprachen tritt das Problem in Sprachen wie Visual Basic, in denen Sie ein Ereignis durch Angeben einer Instanz des übergeordneten Objekts verbinden und gleichzeitig die Rückrufmethode definieren können, seltener auf.</span><span class="sxs-lookup"><span data-stu-id="c7c01-111">By virtue of the syntactic differences in how various languages connect event handlers, this issue is less common in languages such as Visual Basic where you can connect an event specifying an instance of the parent object, and define the callback method at the same time.</span></span> <span data-ttu-id="c7c01-112">Im folgenden Beispiel in Visual Basic wird das Handles-Schlüsselwort verwendet, um die Region\_Expanded-Rückrufmethode mit dem [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\))-Ereignis zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="c7c01-112">The following example in Visual Basic uses the Handles keyword to connect the Region\_Expanded callback method to the [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\)) event.</span></span> <span data-ttu-id="c7c01-113">Der Bereich einer Instanz des übergeordneten Objekts, Region, erstreckt sich über MyClass einschließlich der Region\_Expanded-Rückrufmethode.</span><span class="sxs-lookup"><span data-stu-id="c7c01-113">An instance of the parent object, Region, has a scope that spans MyClass including the Region\_Expanded callback method.</span></span>

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

<span data-ttu-id="c7c01-114">Da in dem Beispiel die Region\_Expanded-Rückrufmethode für die Lebensdauer der Klasse mit dem Expanded-Ereignis verbunden ist, wird die Rückrufmethode wie gewünscht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c7c01-114">In this example, because the Region\_Expanded callback method is connected to the Expanded event for the lifetime of the class, the callback method is called as appropriate.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7c01-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7c01-115">See also</span></span>

- [<span data-ttu-id="c7c01-116">Verbinden mit benutzerdefinierten Ereignishandlern</span><span class="sxs-lookup"><span data-stu-id="c7c01-116">Connecting to custom event handlers</span></span>](connecting-to-custom-event-handlers.md)

