---
title: Abrufen des Kontos für einen Ordner
TOCTitle: Get the account for a folder
ms:assetid: 3706be15-f746-4d0d-9ffe-d6f46b2004dc
ms:contentKeyID: 55119793
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8f56f866e71b1080d5b7a6a33fb17e3e71ab9199
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320216"
---
# <a name="get-the-account-for-a-folder"></a><span data-ttu-id="3706a-102">Abrufen des Kontos für einen Ordner</span><span class="sxs-lookup"><span data-stu-id="3706a-102">Get the account for a folder</span></span>

<span data-ttu-id="3706a-103">In diesem Beispiel wird das Konto abgerufen, das einem Ordner in der aktuellen Sitzung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3706a-103">This example gets the account that is associated with a folder in the current session.</span></span>

## <a name="example"></a><span data-ttu-id="3706a-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3706a-104">Example</span></span>

<span data-ttu-id="3706a-105">Im nachstehenden Codebeispiel ruft die DisplayAccountForCurrentFolder-Funktion die GetAccountForFolder-Funktion auf, um das Konto zu identifizieren, dessen Standardzustellspeicher den aktuellen Ordner beinhaltet, und zeigt dann den Namen des Ordners an.</span><span class="sxs-lookup"><span data-stu-id="3706a-105">In the following code example, the DisplayAccountForCurrentFolder function calls the GetAccountForFolder function to identify the account whose default delivery store hosts the current folder, and then displays the name of the folder.</span></span> <span data-ttu-id="3706a-106">GetAccountForFolder gleicht den Speicher des aktuellen Ordners (abgerufen durch die [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))-Eigenschaft) mit dem Standardzustellspeicher aller Konten (abgerufen durch die [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))-Eigenschaft) ab, die in der [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\))-Sammlung für die Sitzung definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="3706a-106">GetAccountForFolder matches the store of the current folder (obtained from the [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) property) with the default delivery store of each account (obtained with the [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) property) that is defined in the [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) collection for the session.</span></span> <span data-ttu-id="3706a-107">GetAccountForFolder gibt das [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\))-Objekt ab, wenn eine Übereinstimmung gefunden wird; andernfalls wird ein Nullverweis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3706a-107">GetAccountForFolder returns the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object if a match is found; otherwise, it returns a null reference.</span></span>

<span data-ttu-id="3706a-p102">In einer Microsoft Outlook-Sitzung mit mehreren im Profil definierten Konten muss sich der im aktiven Explorer angezeigte Ordner nicht notwendigerweise im Standardspeicher der Sitzung befinden. Stattdessen kann er sich auch auf einem der den verschiedenen Konten zugeordneten Speichern befinden. Dieses Thema beschreibt, wie das Konto, dessen Standardzustellspeicher dem Speicher entspricht, der als Host für den Ordner fungiert, identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3706a-p102">In a Microsoft Outlook session that has multiple accounts defined in the profile, the folder that is displayed in the active explorer does not necessarily reside on the default store for that session; instead, it can reside on one of the multiple stores associated with the multiple accounts. This topic shows how to identify the account whose default delivery store is the same store that hosts the folder.</span></span>

<span data-ttu-id="3706a-110">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="3706a-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3706a-111">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3706a-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3706a-112">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="3706a-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="3706a-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3706a-113">See also</span></span>

- [<span data-ttu-id="3706a-114">Accounts</span><span class="sxs-lookup"><span data-stu-id="3706a-114">Accounts</span></span>](accounts.md)

