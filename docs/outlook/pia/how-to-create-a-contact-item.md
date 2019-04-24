---
title: Erstellen eines Kontaktelements
TOCTitle: Create a Contact item
ms:assetid: b316294a-7f70-4e54-9375-4dc515e9fd11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184633(v=office.15)
ms:contentKeyID: 55119823
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11bfe40d29832577186712e269f9c0971e1e2be6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359675"
---
# <a name="create-a-contact-item"></a>Erstellen eines Kontaktelements

Dieses Beispiel zeigt, wie Sie ein Kontaktelement erstellen und verschiedene Eigenschaften für den Kontakt festlegen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Ein [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\))-Objekt von Outlook verfügt über mehr als 100 integrierte Eigenschaften, wie [Department](https://msdn.microsoft.com/library/bb610564\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)), [OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\)) und [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)). Sie können mit der [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\))-Auflistung benutzerdefinierte Eigenschaften hinzufügen, wenn eine integrierte Eigenschaft nicht verfügbar ist. Nachdem Sie ein **ContactItem** erstellt haben, können Sie seine Eigenschaften festlegen.

Im folgenden Codebeispiel erstellt CreateContactExample ein **ContactItem**-Objekt und legt häufig verwendete Eigenschaften für das Objekt fest. Dann wird die [ShowCheckPhoneDialog(OlContactPhoneNumber)](https://msdn.microsoft.com/library/bb646168\(v=office.15\))-Methode für das **ContactItem**-Objekt aufgerufen. Die **ShowCheckPhoneDialog**-Methode ermöglicht es dem Benutzer, eine Telefonnummer basierend auf den lokalen Konventionen für Telefonnummern aufzulösen.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateContactExample()
{
    Outlook.ContactItem contact = Application.CreateItem(
        Outlook.OlItemType.olContactItem) as Outlook.ContactItem;
    contact.FirstName = "Mellissa";
    contact.LastName = "MacBeth";
    contact.JobTitle = "Account Representative";
    contact.CompanyName = "Contoso Ltd.";
    contact.OfficeLocation = "36/2529";
    contact.BusinessTelephoneNumber = "4255551212 x432";
    contact.WebPage = "https://www.contoso.com";
    contact.BusinessAddressStreet = "1 Microsoft Way";
    contact.BusinessAddressCity = "Redmond";
    contact.BusinessAddressState = "WA";
    contact.BusinessAddressPostalCode = "98052";
    contact.BusinessAddressCountry =
        "United States of America";
    contact.Email1Address = "melissa@contoso.com";
    contact.Email1AddressType = "SMTP";
    contact.Email1DisplayName =
        "Melissa MacBeth (mellissa@contoso.com)";
    contact.Display(false);
    contact.ShowCheckPhoneDialog(
        Outlook.OlContactPhoneNumber.
        olContactPhoneBusiness);
}
```

## <a name="see-also"></a>Siehe auch

- [Kontakte](contacts.md)

