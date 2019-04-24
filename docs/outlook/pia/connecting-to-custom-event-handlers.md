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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351422"
---
# <a name="connecting-to-custom-event-handlers"></a>Verbinden mit benutzerdefinierten Ereignishandlern

Outlook löst Ereignisse aus, um Add-Ins über Vorgänge zu benachrichtigen, wie beispielsweise über den Vorgang eines neuen E-Mailelements im Postfach. Darüberhinaus können Add-ins Outlook gegenüber angeben, welche Aktionen ausgeführt werden sollen, wenn ein bestimmtes Ereignis eintritt. Diese Warnungs- und Rückrufmechanismen werden von Stellvertretungen des .NET Frameworks unterstützt. Die Outlook- PIA (Primary Interop Assembly) definiert Stelvertretungen mit denen Sie Rückrufmethoden verbinden können, um entsprechende Ereignisse zu verarbeiten. Dieses Thema beschreibt den Prozess des Definierens einer Rückrufmethode und ihre Verbindung als Ereignishandler mit dem Outlook-Objekt.

## <a name="creating-a-callback-method"></a>Erstellen einer Rückrufmethode

Bei einem Rückruf handelt es sich um eine Methode, die implementiert wird, um das Auftreten eines bestimmten Ereignisses zu verarbeiten, und die durch eine Benachrichtigungsquelle ausgelöst wird. In Outlook können Add-Ins Rückrufmethoden implementieren, um auf bestimmte von Outlook ausgelöst Ereignisse zu antworten. Dabei muss die Rückrufmethode mit der Stellvertretungssignatur des Ereignisses übereinstimmen. Um zum Beispiel einen Ereignishandler für das [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\))-Ereignis zu implementieren, müssen Sie die Rückrufmethode deklarieren, die mit der Signatur der entsprechenden Stellvertretung übereinstimmt:

```csharp
public delegate void ApplicationEvents_11_ItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Delegate Sub ApplicationEvents_11_ItemSendEventHandler(_
    ByVal Item As Object, ByRef Cancel As Boolean)
```

Ignorieren Sie beim Definieren der Rückrufmethode das **Delegate**-Schlüsselwort, durch das sonst ein anderer Stellvertreter definiert werden würde. Nachfolgend finden Sie eine einfache Rückrufmethode, und zwar **MyItemSendEventHandler**:

```csharp
public void MyItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Sub MyItemSendEventHandler (_
    ByVal Item As Object, ByRef Cancel As Boolean)
…
End Sub
```

## <a name="connecting-a-callback-method"></a>Verbinden einer Rückrufmethode

Nach der Implementation einer Rückrufmethode für ein Ereignis können Sie sie mit dem Outlook-Objekt verbinden, damit Outlook die Methode als Ereignishandler für das Ereignis aufrufen kann. Beachten Sie, dass ein Ereignis von mehr als einem Ereignishandler verarbeitet werden kann. Hier kommen dann die Stellvertretungen zum Zug, die den Ereignishandlern die Ereignisverarbeitung zuweisen.

Um mit dem letzten Beispiel für das Angeben eines Ereignishandlers für das **ItemSend**-Ereignis des **Application**-Objekts fortzufahren und **MyItemSendEventHandler** mit dem **Application**-Objekt in C\# zu verbinden, erstellen Sie eine Instanz des Stellverterterobjekts, übermitteln **MyItemSendEventHandler** an den Konstruktor des Stellvertreterobjekts und fügen dieses Stellvertreterobjekt dann zum **ItemSend**-Ereignis hinzu, indem Sie den Operator += verwenden:

```csharp
app.ItemSend += new ApplicationEvents_11_ItemSendEventHandler(MyItemSendEventHandler)
```

In Visual Basic, verwenden Sie die **AddHandler**-Anweisung, um das **ItemSend**-Ereignis mit dem **MyItemSendEventHandler**-Ereignishandler zu verknüpfen:

```vb
AddHandler app.ItemSend, AddressOf MyItemSendEventHandler
```

## <a name="see-also"></a>Siehe auch

- [Ereignisse in der Outlook-PIA](events-in-the-outlook-pia.md)
- [Objekte in der Outlook-PIA](objects-in-the-outlook-pia.md)

