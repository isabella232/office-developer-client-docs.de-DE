---
title: Abrufen des Kontos für einen Ordner
TOCTitle: Get the account for a folder
ms:assetid: 3706be15-f746-4d0d-9ffe-d6f46b2004dc
ms:contentKeyID: 55119793
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b681e8cdac2f915dcf2e5c74419fb7f4ac6c6752
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590637"
---
# <a name="get-the-account-for-a-folder"></a>Abrufen des Kontos für einen Ordner

In diesem Beispiel wird das Konto abgerufen, das einem Ordner in der aktuellen Sitzung zugeordnet ist.

## <a name="example"></a>Beispiel

Im nachstehenden Codebeispiel ruft die DisplayAccountForCurrentFolder-Funktion die GetAccountForFolder-Funktion auf, um das Konto zu identifizieren, dessen Standardzustellspeicher den aktuellen Ordner beinhaltet, und zeigt dann den Namen des Ordners an. GetAccountForFolder gleicht den Speicher des aktuellen Ordners (abgerufen durch die [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))-Eigenschaft) mit dem Standardzustellspeicher aller Konten (abgerufen durch die [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))-Eigenschaft) ab, die in der [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\))-Sammlung für die Sitzung definiert wurden. GetAccountForFolder gibt das [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\))-Objekt ab, wenn eine Übereinstimmung gefunden wird; andernfalls wird ein Nullverweis zurückgegeben.

In einer Microsoft Outlook-Sitzung mit mehreren im Profil definierten Konten muss sich der im aktiven Explorer angezeigte Ordner nicht notwendigerweise im Standardspeicher der Sitzung befinden. Stattdessen kann er sich auch auf einem der den verschiedenen Konten zugeordneten Speichern befinden. Dieses Thema beschreibt, wie das Konto, dessen Standardzustellspeicher dem Speicher entspricht, der als Host für den Ordner fungiert, identifiziert werden kann.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void DisplayAccountForCurrentFolder()
{
    Outlook.Folder myFolder = Application.ActiveExplorer().CurrentFolder 
        as Outlook.Folder;
    string msg = "Account for Current Folder:" + "\n" +
        GetAccountForFolder(myFolder).DisplayName;
    MessageBox.Show(msg,
        "GetAccountForFolder",
        MessageBoxButtons.OK,
        MessageBoxIcon.Information);
}

Outlook.Account GetAccountForFolder(Outlook.Folder folder)
{
    // Obtain the store on which the folder resides.
    Outlook.Store store = folder.Store;

    // Enumerate the accounts defined for the session.
    foreach (Outlook.Account account in Application.Session.Accounts)
    {
        // Match the DefaultStore.StoreID of the account
        // with the Store.StoreID for the currect folder.
        if (account.DeliveryStore.StoreID  == store.StoreID)
        {
            // Return the account whose default delivery store
            // matches the store of the given folder.
            return account;
        }
     }
     // No account matches, so return null.
     return null;
}
```

## <a name="see-also"></a>Siehe auch

- [Accounts](accounts.md)

