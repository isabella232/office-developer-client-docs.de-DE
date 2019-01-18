---
title: Verbinden mit benutzerdefinierten Ereignishandlern
TOCTitle: Connecting to custom event handlers
ms:assetid: 6e894c16-0fe9-4b86-b798-547b86f44cd8
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610520(v=office.15)
ms:contentKeyID: 55119783
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 58722b8b140f89f0fe29a3e52db578a423a0160a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711798"
---
# <a name="connecting-to-custom-event-handlers"></a><span data-ttu-id="25981-102">Verbinden mit benutzerdefinierten Ereignishandlern</span><span class="sxs-lookup"><span data-stu-id="25981-102">Connecting to custom event handlers</span></span>

<span data-ttu-id="25981-p101">Outlook löst Ereignisse aus, um Add-Ins über Vorgänge zu benachrichtigen, wie beispielsweise über den Vorgang eines neuen E-Mailelements im Postfach. Darüberhinaus können Add-ins Outlook gegenüber angeben, welche Aktionen ausgeführt werden sollen, wenn ein bestimmtes Ereignis eintritt. Diese Warnungs- und Rückrufmechanismen werden von Stellvertretungen des .NET Frameworks unterstützt. Die Outlook- PIA (Primary Interop Assembly) definiert Stelvertretungen mit denen Sie Rückrufmethoden verbinden können, um entsprechende Ereignisse zu verarbeiten. Dieses Thema beschreibt den Prozess des Definierens einer Rückrufmethode und ihre Verbindung als Ereignishandler mit dem Outlook-Objekt.</span><span class="sxs-lookup"><span data-stu-id="25981-p101">Outlook raises events to notify add-ins about something happening, such as the Inbox receiving a new mail item. Add-ins can specify to Outlook that upon the occurrence of a specific event, certain actions should take place. This alert and callback mechanism is supported by delegates of the .NET Framework. The Outlook Primary Interop Assembly (PIA) defines delegates to which you can connect callback methods to handle corresponding events. This topic describes this process of defining a callback method and connecting it as an event handler to the Outlook object.</span></span>

## <a name="creating-a-callback-method"></a><span data-ttu-id="25981-108">Erstellen einer Rückrufmethode</span><span class="sxs-lookup"><span data-stu-id="25981-108">Creating a Callback method</span></span>

<span data-ttu-id="25981-p102">Bei einem Rückruf handelt es sich um eine Methode, die implementiert wird, um das Auftreten eines bestimmten Ereignisses zu verarbeiten, und die durch eine Benachrichtigungsquelle ausgelöst wird. In Outlook können Add-Ins Rückrufmethoden implementieren, um auf bestimmte von Outlook ausgelöst Ereignisse zu antworten. Dabei muss die Rückrufmethode mit der Stellvertretungssignatur des Ereignisses übereinstimmen. Um zum Beispiel einen Ereignishandler für das [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\))-Ereignis zu implementieren, müssen Sie die Rückrufmethode deklarieren, die mit der Signatur der entsprechenden Stellvertretung übereinstimmt:</span><span class="sxs-lookup"><span data-stu-id="25981-p102">A callback is a method that is implemented to handle the occurrence of a specific event and is executed by a notification source. In Outlook, add-ins can implement callback methods to respond to certain events raised by Outlook. This callback method must match the signature of the delegate of that event. For example, to implement an event handler for the [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)) event, you must declare the callback method that matches the signature of the corresponding delegate:</span></span>

```csharp
public delegate void ApplicationEvents_11_ItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Delegate Sub ApplicationEvents_11_ItemSendEventHandler(_
    ByVal Item As Object, ByRef Cancel As Boolean)
```

<span data-ttu-id="25981-p103">Ignorieren Sie beim Definieren der Rückrufmethode das **Delegate**-Schlüsselwort, durch das sonst ein anderer Stellvertreter definiert werden würde. Nachfolgend finden Sie eine einfache Rückrufmethode, und zwar **MyItemSendEventHandler**:</span><span class="sxs-lookup"><span data-stu-id="25981-p103">When defining the callback method, ignore the **Delegate** keyword which otherwise would define another delegate. A sample callback method, **MyItemSendEventHandler**, is shown below:</span></span>

```csharp
public void MyItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Sub MyItemSendEventHandler (_
    ByVal Item As Object, ByRef Cancel As Boolean)
…
End Sub
```

## <a name="connecting-a-callback-method"></a><span data-ttu-id="25981-115">Verbinden einer Rückrufmethode</span><span class="sxs-lookup"><span data-stu-id="25981-115">Connecting a Callback method</span></span>

<span data-ttu-id="25981-p104">Nach der Implementation einer Rückrufmethode für ein Ereignis können Sie sie mit dem Outlook-Objekt verbinden, damit Outlook die Methode als Ereignishandler für das Ereignis aufrufen kann. Beachten Sie, dass ein Ereignis von mehr als einem Ereignishandler verarbeitet werden kann. Hier kommen dann die Stellvertretungen zum Zug, die den Ereignishandlern die Ereignisverarbeitung zuweisen.</span><span class="sxs-lookup"><span data-stu-id="25981-p104">After implementing a callback method for an event, you can connect it to the Outlook object so that Outlook knows to call the method as an event handler of that event. Note that an event can be handled by more than one event handler, and this is where delegates that assign event handling to event handlers come into play.</span></span>

<span data-ttu-id="25981-118">Um mit dem letzten Beispiel für das Angeben eines Ereignishandlers für das **ItemSend**-Ereignis des **Application**-Objekts fortzufahren und **MyItemSendEventHandler** mit dem **Application**-Objekt in C\# zu verbinden, erstellen Sie eine Instanz des Stellverterterobjekts, übermitteln **MyItemSendEventHandler** an den Konstruktor des Stellvertreterobjekts und fügen dieses Stellvertreterobjekt dann zum **ItemSend**-Ereignis hinzu, indem Sie den Operator += verwenden:</span><span class="sxs-lookup"><span data-stu-id="25981-118">Continuing with the last example of specifying a event handler for the **ItemSend** event of the **Application** object, to connect **MyItemSendEventHandler** to the **Application** object in C\#, create an instance of the delegate object, pass **MyItemSendEventHandler** to the constructor of the delegate object, and then add this delegate object to the **ItemSend** event using the += operator:</span></span>

```csharp
app.ItemSend += new ApplicationEvents_11_ItemSendEventHandler(MyItemSendEventHandler)
```

<span data-ttu-id="25981-119">In Visual Basic, verwenden Sie die **AddHandler**-Anweisung, um das **ItemSend**-Ereignis mit dem **MyItemSendEventHandler**-Ereignishandler zu verknüpfen:</span><span class="sxs-lookup"><span data-stu-id="25981-119">In Visual Basic, you use the **AddHandler** statement to associate the **ItemSend** event with the **MyItemSendEventHandler** event handler:</span></span>

```vb
AddHandler app.ItemSend, AddressOf MyItemSendEventHandler
```

## <a name="see-also"></a><span data-ttu-id="25981-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25981-120">See also</span></span>

- [<span data-ttu-id="25981-121">Ereignisse in der Outlook-PIA</span><span class="sxs-lookup"><span data-stu-id="25981-121">Events in the Outlook PIA</span></span>](events-in-the-outlook-pia.md)
- [<span data-ttu-id="25981-122">Objekte in der Outlook-PIA</span><span class="sxs-lookup"><span data-stu-id="25981-122">Objects in the Outlook PIA</span></span>](objects-in-the-outlook-pia.md)

