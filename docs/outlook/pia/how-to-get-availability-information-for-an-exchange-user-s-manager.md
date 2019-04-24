---
title: Abrufen von Verfügbarkeitsinformationen für den Vorgesetzten eines Exchange-Benutzers
TOCTitle: Get availability information for an Exchange user's manager
ms:assetid: b59dd875-50c2-4f24-ba91-24429abf1b72
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646996(v=office.15)
ms:contentKeyID: 55119849
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df3779a3b92368af75d152e662eedec1a30a97bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349483"
---
# <a name="get-availability-information-for-an-exchange-users-manager"></a><span data-ttu-id="a2ed7-102">Abrufen von Verfügbarkeitsinformationen für den Vorgesetzten eines Exchange-Benutzers</span><span class="sxs-lookup"><span data-stu-id="a2ed7-102">Get availability information for an Exchange user's manager</span></span>

<span data-ttu-id="a2ed7-103">In diesem Beispiel wird das nächste freie 60-minütige Zeitfenster für den Vorgesetzten eines Benutzers im Kalender angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a2ed7-103">This example displays the next free 60-minute time slot in the calendar for a user's manager.</span></span>

## <a name="example"></a><span data-ttu-id="a2ed7-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a2ed7-104">Example</span></span>

<span data-ttu-id="a2ed7-105">Das Codebeispiel überprüft, ob es sich beim aktuellen Benutzer um einen Exchange-Benutzer handelt.</span><span class="sxs-lookup"><span data-stu-id="a2ed7-105">This code sample checks whether the current user is an Exchange user.</span></span> <span data-ttu-id="a2ed7-106">Ist dies der Fall und verfügt der aktuelle Benutzer über einen Manager, werden die Informationen des Managers durch einen Aufruf der [GetExchangeUser](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) -Methode des [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) -Objekts und der [GetExchangeUserManager](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) -Methode des [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) -Objekts abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a2ed7-106">If so, and if the current user has a manager, it obtains the manager's information by calling the [GetExchangeUser](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) method of the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object and the [GetExchangeUserManager](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method of the [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object.</span></span> <span data-ttu-id="a2ed7-107">Die Informationen des Managers sind in einem **ExchangeUser**-Objekt enthalten, das den Frei/Gebucht-Zeitplan des Managers umfasst.</span><span class="sxs-lookup"><span data-stu-id="a2ed7-107">The manager's information is contained in an **ExchangeUser** object that includes the manager's Free/Busy schedule.</span></span>

<span data-ttu-id="a2ed7-108">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="a2ed7-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="a2ed7-109">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a2ed7-109">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a2ed7-110">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="a2ed7-110">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub GetManagerOpenInterval()
    Const slotLength As Integer = 60
    Dim addrEntry As Outlook.AddressEntry = _
        Application.Session.CurrentUser.AddressEntry
    If addrEntry.Type = "EX" Then
        Dim manager As Outlook.ExchangeUser = _
            Application.Session.CurrentUser. _
            AddressEntry.GetExchangeUser(). _
            GetExchangeUserManager()
        If Not (manager Is Nothing) Then
            Dim freeBusy As String = _
            manager.GetFreeBusy(DateTime.Now, slotLength, True)
            For i As Integer = 1 To freeBusy.Length - 1
                If (freeBusy.Substring(i, 1) = "0") Then
                    ' Get number of minutes into
                    ' the day for free interval
                    Dim busySlot As Double = (i - 1) * slotLength
                    ' Get an actual date/time
                    Dim dateBusySlot As DateTime = _
                        DateTime.Now.Date.AddMinutes(busySlot)
                    If (dateBusySlot.TimeOfDay >= _
                        DateTime.Parse("8:00 AM").TimeOfDay And _
                        dateBusySlot.TimeOfDay <= _
                        DateTime.Parse("5:00 PM").TimeOfDay And _
                        Not (dateBusySlot.DayOfWeek = _
                        DayOfWeek.Saturday Or _
                        dateBusySlot.DayOfWeek = DayOfWeek.Sunday))Then
                        Dim sb As StringBuilder = New StringBuilder()
                        sb.AppendLine( _
                            manager.Name & " first open interval:")
                        sb.AppendLine(dateBusySlot.ToString("f"))
                        Debug.WriteLine(sb.ToString())
                    End If
                End If
            Next
        End If
    End If
End Sub
```


```csharp
private void GetManagerOpenInterval()
{
    const int slotLength = 60;
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            string freeBusy = manager.GetFreeBusy(
                DateTime.Now, slotLength, true);
            for (int i = 1; i < freeBusy.Length; i++)
            {
                if (freeBusy.Substring(i, 1) == "0")
                {
                    // Get number of minutes into
                    // the day for free interval
                    double busySlot = (i - 1) * slotLength;
                    // Get an actual date/time
                    DateTime dateBusySlot =
                        DateTime.Now.Date.AddMinutes(busySlot);
                    if (dateBusySlot.TimeOfDay >=
                        DateTime.Parse("8:00 AM").TimeOfDay &
                        dateBusySlot.TimeOfDay <=
                        DateTime.Parse("5:00 PM").TimeOfDay &
                        !(dateBusySlot.DayOfWeek == 
                        DayOfWeek.Saturday |
                        dateBusySlot.DayOfWeek == DayOfWeek.Sunday))
                    {
                        StringBuilder sb = new StringBuilder();
                        sb.AppendLine(manager.Name
                            + " first open interval:");
                        sb.AppendLine(dateBusySlot.ToString("f"));
                        Debug.WriteLine(sb.ToString());
                    }
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="a2ed7-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2ed7-111">See also</span></span>

- [<span data-ttu-id="a2ed7-112">Exchange-Benutzer</span><span class="sxs-lookup"><span data-stu-id="a2ed7-112">Exchange users</span></span>](exchange-users.md)

