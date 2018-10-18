---
title: Abrufen von Informationen über den aktuellen Benutzer
TOCTitle: Get information about the current user
ms:assetid: 3802523a-3ccf-4cca-a348-abe2645a0d9c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184601(v=office.15)
ms:contentKeyID: 55119840
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 7ac10c01d205f4f4590183bcef8006e8f1344cbd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406974"
---
# <a name="get-information-about-the-current-user"></a>Abrufen von Informationen über den aktuellen Benutzer

Dieses Beispiel zeigt, wie Sie Informationen des aktuellen Benutzers, z. B. Name, berufliche Position und Telefonnummer, abrufen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Um ein [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\))-Objekt aus einem [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\))-Objekt abzurufen, rufen Sie die [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\))-Methode im **AddressEntry**-Objekt auf. Im folgenden Verfahren ruft GetCurrentUserInfo die [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\))-Eigenschaft für das [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\))-Objekt mithilfe der [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\))-Eigenschaft ab. Wenn das **AddressEntry**-Objekt dem Benutzer eines Exchange-Postfachs entspricht, ruft GetCurrentUserInfo die **GetExchangeUser**-Methode auf, und es wird ein **ExchangeUser**-Objekt zurückgegeben. Die Eigenschaften [Name](https://msdn.microsoft.com/library/bb622941\(v=office.15\)), [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)), [JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\)), [Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\)), [OfficeLocation](https://msdn.microsoft.com/library/bb611429\(v=office.15\)), [BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\)) und [MobileTelephoneNumber](https://msdn.microsoft.com/library/bb609292\(v=office.15\)) werden in den Ablaufverfolgungslistenern der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung aufgelistet.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserInfo()
{
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser currentUser =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser();
        if (currentUser != null)
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Name: "
                + currentUser.Name);
            sb.AppendLine("STMP address: "
                + currentUser.PrimarySmtpAddress);
            sb.AppendLine("Title: "
                + currentUser.JobTitle);
            sb.AppendLine("Department: "
                + currentUser.Department);
            sb.AppendLine("Location: "
                + currentUser.OfficeLocation);
            sb.AppendLine("Business phone: "
                + currentUser.BusinessTelephoneNumber);
            sb.AppendLine("Mobile phone: "
                + currentUser.MobileTelephoneNumber);
            Debug.WriteLine(sb.ToString());
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Exchange-Benutzer](exchange-users.md)

