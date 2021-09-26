---
title: Erstellen eines E-Mail-Elements, Anfügen eines Berichts und Senden des E-Mail-Elements an den Vorgesetzten des Benutzers
TOCTitle: Create a mail item, attach a report, and send the mail item to the user's manager
ms:assetid: 15c26c3b-5e86-4e28-92c5-7389572521da
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644320(v=office.15)
ms:contentKeyID: 55119866
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 87fc89d1d15f5fed0de7cd798c08ba2fda350016
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629417"
---
# <a name="create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-users-manager"></a>Erstellen eines E-Mail-Elements, Anfügen eines Berichts und Senden des E-Mail-Elements an den Vorgesetzten des Benutzers

In diesem Beispiel wird ein E-Mail-Element mit einer Anlage erstellt und dann an den Vorgesetzten des Benutzers gesendet.

## <a name="example"></a>Beispiel

Dieses Beispiel kann nur mit einem Microsoft Exchange Server-Konto ordnungsgemäß ausgeführt werden. Im Active Directory-Verzeichnisdienst muss eine Vorgesetztenbeziehung für Benutzer eingerichtet werden. Im Beispiel wird anhand des [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) -Objekts durch Aufrufen der [GetExchangeUserManager](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) -Methode der Vorgesetzte des aktuellen Benutzers ermittelt.

Wenn Sie dieses Codebeispiel mit Visual Studio testen, müssen Sie beim Importieren des **Microsoft.Office.Interop.Outlook**-Namespace zuerst einen Verweis auf die Microsoft Outlook 15.0-Objektbibliothekskomponente hinzufügen und die Outlook-Variable angeben. Die **Imports**- oder **using**-Anweisung darf nicht direkt vor den Funktionen im Codebeispiel stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie der Import und die Zuweisung in Visual Basic und C\# ausgeführt werden.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SendSalesReport()
    Dim mail As Outlook.MailItem = CType(Application.CreateItem( _
        Outlook.OlItemType.olMailItem), Outlook.MailItem)
    mail.Subject = "Quarterly Sales Report FY06 Q4"
    Dim currentUser As Outlook.AddressEntry = _
        Application.Session.CurrentUser.AddressEntry
    If currentUser.Type = "EX" Then
        Dim manager As Outlook.ExchangeUser = _
            currentUser.GetExchangeUser().GetExchangeUserManager()
        ' Add recipient using display name, alias, or smtp address
        mail.Recipients.Add(manager.PrimarySmtpAddress)
        mail.Recipients.ResolveAll()
        mail.Attachments.Add("c:\sales reports\fy06q4.xlsx", _
            Outlook.OlAttachmentType.olByValue)
        mail.Send()
    End If
End Sub
```


```csharp
private void SendSalesReport()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Quarterly Sales Report FY06 Q4";
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        // Add recipient using display name, alias, or smtp address
        mail.Recipients.Add(manager.PrimarySmtpAddress);
        mail.Recipients.ResolveAll();
        mail.Attachments.Add(@"c:\sales reports\fy06q4.xlsx",
            Outlook.OlAttachmentType.olByValue, Type.Missing,
            Type.Missing);
        mail.Send();
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Mail](mail.md)

