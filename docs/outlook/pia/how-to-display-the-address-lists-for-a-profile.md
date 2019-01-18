---
title: Anzeigen der Adresslisten für ein Profil
TOCTitle: Display the address lists for a profile
ms:assetid: ced8230b-110b-4ccb-a699-588798144154
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184643(v=office.15)
ms:contentKeyID: 55119802
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b69ed930241dc058b22b75c6ccc9121f8856d28f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703720"
---
# <a name="display-the-address-lists-for-a-profile"></a>Anzeigen der Adresslisten für ein Profil

In diesem Beispiel wird gezeigt, wie die Adresslisten für das aktuelle Profil angezeigt werden.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Das aktuelle Profil enthält Adresslisten, die durch die [AddressLists](https://msdn.microsoft.com/library/bb611894\(v=office.15\)) -Auflistung dargestellt werden. Zum Abrufen einer Instanz der AddressLists-Auflistung verwenden Sie die [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) -Eigenschaft des [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) -Objekts.

Im folgenden Codebeispiel zählt EnumerateAddressLists zunächst alle [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\))-Objekte in der AddressLists-Auflistung mithilfe einer foreach-Anweisung auf. Anschließend wird im Beispiel eine Zeichenfolge erstellt, die die Werte der Eigenschaften [Name](https://msdn.microsoft.com/library/bb609849\(v=office.15\)), [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)), [IsReadOnly](https://msdn.microsoft.com/library/bb612676\(v=office.15\)) und [IsInitialAddressList](https://msdn.microsoft.com/library/bb646646\(v=office.15\)) enthält. Zuletzt schreibt EnumerateAddressLists die Zeichenfolge in die Listener der Ablaufverfolgung der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung. Dadurch wird die Adressliste für das aktuelle Profil angezeigt.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateAddressLists()
{
    Outlook.AddressLists addrLists =
         Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Display Name: " + addrList.Name);
        sb.AppendLine("Resolution Order: "
            + addrList.ResolutionOrder.ToString());
        sb.AppendLine("Read-only : "
            + addrList.IsReadOnly.ToString());
        sb.AppendLine("Initial Address List: "
            + addrList.IsInitialAddressList.ToString());
        sb.AppendLine("");
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Adressbuch](address-book.md)

