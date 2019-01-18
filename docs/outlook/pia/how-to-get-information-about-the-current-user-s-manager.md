---
title: Abrufen von Informationen zum Vorgesetzten des aktuellen Benutzers
TOCTitle: Get information about the current user's manager
ms:assetid: 3a77fa51-e2e3-4544-849f-4267b1762270
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184603(v=office.15)
ms:contentKeyID: 55119846
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fd5b49a2b1f1e494a494cf1bea4e105fa261e053
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718126"
---
# <a name="get-information-about-the-current-users-manager"></a>Abrufen von Informationen zum Vorgesetzten des aktuellen Benutzers

Dieses Beispiel zeigt, wie Sie Informationen (z. B. Namen, berufliche Position und Telefonnummern) zum Vorgesetzten des aktuellen Benutzers abrufen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Im folgenden Verfahren ruft GetManagerInfo die [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\))-Methode auf, um ein[ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\))-Objekt abzurufen, das dem Vorgesetzten eines **ExchangeUser** in der Unternehmenshierarchie entspricht. Das Verfahren überprüft, ob der angemeldete Benutzer online ist, um sicherzustellen, dass **GetExchangeUserManager** ein **ExchangeUser**-Objekt zurückgeben kann. Wenn der Benutzer nicht online ist, gibt **GetExchangeUserManager** einen NULL-Verweis zurück. Durch GetManagerInfo werden dann die Informationen zum Vorgesetzten in die Ablaufverfolgungslistenern der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Sammlung geschrieben.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetManagerInfo()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Name: "
                + manager.Name);
            sb.AppendLine("STMP address: "
                + manager.PrimarySmtpAddress);
            sb.AppendLine("Title: "
                + manager.JobTitle);
            sb.AppendLine("Department: "
                + manager.Department);
            sb.AppendLine("Location: "
                + manager.OfficeLocation);
            sb.AppendLine("Business phone: "
                + manager.BusinessTelephoneNumber);
            sb.AppendLine("Mobile phone: "
                + manager.MobileTelephoneNumber);
            Debug.WriteLine(sb.ToString());
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Exchange-Benutzer](exchange-users.md)

