---
title: Abrufen der Mitglieder einer Exchange-Verteilerliste
TOCTitle: Get members of an Exchange distribution list
ms:assetid: 75b38e40-772c-400b-8df9-e3e385b87f9c
ms:mtpsurl: https://msdn.microsoft.com/library/Bb645998(v=office.15)
ms:contentKeyID: 55119837
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: d5c615eb811d5dc4a0f4170bfe432179acaa4666
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726057"
---
# <a name="get-members-of-an-exchange-distribution-list"></a><span data-ttu-id="15c20-102">Abrufen der Mitglieder einer Exchange-Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="15c20-102">Get members of an Exchange distribution list</span></span>

<span data-ttu-id="15c20-103">In diesem Beispiel wird der Benutzer aufgefordert, eine Exchange-Verteilerliste aus dem Dialogfeld **Namen auswählen** auszuwählen, und die Verteilerliste wird so erweitert, dass die Mitglieder der Verteilerliste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="15c20-103">This example prompts the user to select an Exchange distribution list from the **Select Names** dialog box and expands the distribution list to display its members.</span></span>

## <a name="example"></a><span data-ttu-id="15c20-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="15c20-104">Example</span></span>

<span data-ttu-id="15c20-p101">In diesem Codebeispiel wird die [GetExchangeDistributionListMembers](https://msdn.microsoft.com/library/bb647622\(v=office.15\)) -Methode des [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) -Objekts aufgerufen, um die [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) -Sammlung mit allen Mitgliedern der Liste abzurufen. Weil Verteilerlisten in anderen Verteilerlisten verschachtelt sein können, kann die zurückgegebene **AddressEntries**-Sammlung jede Art von Exchange-[AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) -Objekt darstellen.</span><span class="sxs-lookup"><span data-stu-id="15c20-p101">This code sample calls the [GetExchangeDistributionListMembers](https://msdn.microsoft.com/library/bb647622\(v=office.15\)) method of the [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) object to get an [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) collection that contains all the members of the list. Because distribution lists can be nested inside another distribution list, the returned **AddressEntries** collection can represent any type of Exchange [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object.</span></span>


> [!NOTE]
> <span data-ttu-id="15c20-p102">Das Erweitern von Verteilerlisten kann eine Leistungsbelastung für den Exchange-Server erzeugen. Verwenden Sie daher die **GetExchangeDistributionListMembers**-Methode vorsichtig. Rechnen Sie damit, dass Ihr Code verlangsamt wird, wenn er große Verteilerlisten erweitert.</span><span class="sxs-lookup"><span data-stu-id="15c20-p102">Expanding distribution lists can create a performance burden on an Exchange server, so use the **GetExchangeDistributionListMembers** method cautiously. Expect that your code will be slow when it expands large distribution lists.</span></span>

<span data-ttu-id="15c20-109">Um die Mitglieder einer Verteilerliste abzurufen, muss der Benutzer mit einem Exchange-Server verbunden und online sein.</span><span class="sxs-lookup"><span data-stu-id="15c20-109">To obtain the members of a distribution list, the user must be connected to an Exchange server and online.</span></span>

<span data-ttu-id="15c20-110">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="15c20-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="15c20-111">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="15c20-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="15c20-112">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="15c20-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub GetDistributionListMembers()
    Dim snd As Outlook.SelectNamesDialog = _
        Application.Session.GetSelectNamesDialog()
    Dim addrLists As Outlook.AddressLists = _
        Application.Session.AddressLists
    For Each addrList As Outlook.AddressList In addrLists
        If addrList.Name = "All Groups" Then
            snd.InitialAddressList = addrList
            Exit For
        End If
    Next
    snd.NumberOfRecipientSelectors = _
        Outlook.OlRecipientSelectors.olShowTo
    snd.ToLabel = "D/L"
    snd.ShowOnlyInitialAddressList = True
    snd.AllowMultipleSelection = False
    snd.Display()
    If (snd.Recipients.Count > 0) Then
        Dim addrEntry As Outlook.AddressEntry = _
            snd.Recipients(1).AddressEntry
        If (addrEntry.AddressEntryUserType = _
            Outlook.OlAddressEntryUserType. _
            olExchangeDistributionListAddressEntry) Then
            Dim exchDL As Outlook.ExchangeDistributionList = _
                addrEntry.GetExchangeDistributionList()
            Dim addrEntries As Outlook.AddressEntries = _
                exchDL.GetExchangeDistributionListMembers()
            If Not (addrEntries Is Nothing) Then
                For Each exchDLMember As _
                    Outlook.AddressEntry In addrEntries
                    Debug.WriteLine(exchDLMember.Name)
                Next
            End If
         End If
    End If
End Sub
```


```csharp
private void GetDistributionListMembers()
{
    Outlook.SelectNamesDialog snd =
        Application.Session.GetSelectNamesDialog();
    Outlook.AddressLists addrLists =
        Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        if (addrList.Name == "All Groups")
        {
            snd.InitialAddressList = addrList;
            break;
        }
    }
    snd.NumberOfRecipientSelectors =
        Outlook.OlRecipientSelectors.olShowTo;
    snd.ToLabel = "D/L";
    snd.ShowOnlyInitialAddressList = true;
    snd.AllowMultipleSelection = false;
    snd.Display();
    if (snd.Recipients.Count > 0)
    {
        Outlook.AddressEntry addrEntry =
            snd.Recipients[1].AddressEntry;
        if (addrEntry.AddressEntryUserType ==
            Outlook.OlAddressEntryUserType.
            olExchangeDistributionListAddressEntry)
        {
            Outlook.ExchangeDistributionList exchDL =
                addrEntry.GetExchangeDistributionList();
            Outlook.AddressEntries addrEntries =
                exchDL.GetExchangeDistributionListMembers();
            if (addrEntries != null)
                foreach (Outlook.AddressEntry exchDLMember
                    in addrEntries)
                {
                    Debug.WriteLine(exchDLMember.Name);
                }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="15c20-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15c20-113">See also</span></span>

- [<span data-ttu-id="15c20-114">Exchange-Benutzer</span><span class="sxs-lookup"><span data-stu-id="15c20-114">Exchange users</span></span>](exchange-users.md)

