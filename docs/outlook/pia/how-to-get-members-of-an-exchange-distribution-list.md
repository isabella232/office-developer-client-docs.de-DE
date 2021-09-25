---
title: Abrufen der Mitglieder einer Exchange-Verteilerliste
TOCTitle: Get members of an Exchange distribution list
ms:assetid: 75b38e40-772c-400b-8df9-e3e385b87f9c
ms:mtpsurl: https://msdn.microsoft.com/library/Bb645998(v=office.15)
ms:contentKeyID: 55119837
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 9ddb7e2c89bd869909c27f25c34d3a01c7e9d66a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574664"
---
# <a name="get-members-of-an-exchange-distribution-list"></a>Abrufen der Mitglieder einer Exchange-Verteilerliste

In diesem Beispiel wird der Benutzer aufgefordert, eine Exchange-Verteilerliste aus dem Dialogfeld **Namen auswählen** auszuwählen, und die Verteilerliste wird so erweitert, dass die Mitglieder der Verteilerliste angezeigt werden.

## <a name="example"></a>Beispiel

In diesem Codebeispiel wird die [GetExchangeDistributionListMembers](https://msdn.microsoft.com/library/bb647622\(v=office.15\)) -Methode des [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) -Objekts aufgerufen, um die [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) -Sammlung mit allen Mitgliedern der Liste abzurufen. Weil Verteilerlisten in anderen Verteilerlisten verschachtelt sein können, kann die zurückgegebene **AddressEntries**-Sammlung jede Art von Exchange-[AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) -Objekt darstellen.


> [!NOTE]
> Das Erweitern von Verteilerlisten kann eine Leistungsbelastung für den Exchange-Server erzeugen. Verwenden Sie daher die **GetExchangeDistributionListMembers**-Methode vorsichtig. Rechnen Sie damit, dass Ihr Code verlangsamt wird, wenn er große Verteilerlisten erweitert.

Um die Mitglieder einer Verteilerliste abzurufen, muss der Benutzer mit einem Exchange-Server verbunden und online sein.

Wenn Sie dieses Codebeispiel mit Visual Studio testen, müssen Sie beim Importieren des **Microsoft.Office.Interop.Outlook**-Namespace zuerst einen Verweis auf die Microsoft Outlook 15.0-Objektbibliothekskomponente hinzufügen und die Outlook-Variable angeben. Die **Imports**- oder **using**-Anweisung darf nicht direkt vor den Funktionen im Codebeispiel stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie der Import und die Zuweisung in Visual Basic und C\# ausgeführt werden.

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

## <a name="see-also"></a>Siehe auch

- [Exchange-Benutzer](exchange-users.md)

