---
title: Erstellen eines E-Mail-Elements, Anfügen eines Berichts und Senden des E-Mail-Elements an den Vorgesetzten des Benutzers
TOCTitle: Create a mail item, attach a report, and send the mail item to the user's manager
ms:assetid: 15c26c3b-5e86-4e28-92c5-7389572521da
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644320(v=office.15)
ms:contentKeyID: 55119866
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 5d07424635959fec41c266592da15214eace8b3e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407282"
---
# <a name="create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-users-manager"></a><span data-ttu-id="f3ece-102">Erstellen eines E-Mail-Elements, Anfügen eines Berichts und Senden des E-Mail-Elements an den Vorgesetzten des Benutzers</span><span class="sxs-lookup"><span data-stu-id="f3ece-102">Create a mail item, attach a report, and send the mail item to the user's manager</span></span>

<span data-ttu-id="f3ece-103">In diesem Beispiel wird ein E-Mail-Element mit einer Anlage erstellt und dann an den Vorgesetzten des Benutzers gesendet.</span><span class="sxs-lookup"><span data-stu-id="f3ece-103">This example creates a mail item that has an attachment, and then sends the mail item to the user's manager.</span></span>

## <a name="example"></a><span data-ttu-id="f3ece-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f3ece-104">Example</span></span>

<span data-ttu-id="f3ece-p101">Dieses Beispiel kann nur mit einem Microsoft Exchange Server-Konto ordnungsgemäß ausgeführt werden. Im Active Directory-Verzeichnisdienst muss eine Vorgesetztenbeziehung für Benutzer eingerichtet werden. Im Beispiel wird anhand des [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) -Objekts durch Aufrufen der [GetExchangeUserManager](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) -Methode der Vorgesetzte des aktuellen Benutzers ermittelt.</span><span class="sxs-lookup"><span data-stu-id="f3ece-p101">This example runs correctly only against a Microsoft Exchange Server account. A manager relationship for users must be established in the Active Directory directory service. The example uses the [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object to determine the current user's manager by calling the [GetExchangeUserManager](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method.</span></span>

<span data-ttu-id="f3ece-108">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="f3ece-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="f3ece-109">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f3ece-109">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="f3ece-110">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="f3ece-110">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="f3ece-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3ece-111">See also</span></span>

- [<span data-ttu-id="f3ece-112">Mail</span><span class="sxs-lookup"><span data-stu-id="f3ece-112">Mail</span></span>](mail.md)

