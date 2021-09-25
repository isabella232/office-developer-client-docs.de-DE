---
title: Ändern des Layouts einer elektronischen Visitenkarte
TOCTitle: Modify the layout of an electronic business card
ms:assetid: f387c4a7-59c5-4b6a-b33a-1bfa7d499bbf
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-modify-the-layout-of-an-electronic-business-card?redirectedfrom=MSDN
ms:contentKeyID: 55119838
ms.date: 12/03/2019
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b94119b0625793a2eac80c2ae58a924fb8ed3c35
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574643"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a>Ändern des Layouts einer elektronischen Visitenkarte

Dieses Beispiel zeigt, wie das Layout einer elektronischen Visitenkarte mithilfe der [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\))-Eigenschaft der [ContactItem](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.contactitem?redirectedfrom=MSDN&view=outlook-pia)-Schnittstelle geändert wird.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Eine elektronische Visitenkarte enthält eine Ansicht eines Kontakts, in der bestimmte Informationen aus einem Kontakt erfasst sind. Die **ContactItem**-Schnittstelle bietet bestimmte Member, die elektronische Visitenkarten betreffen. Diese Member sind **BusinessCardLayoutXml**, [BusinessCardType](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.businesscardtype?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_BusinessCardType), [AddBusinessCardLogoPicture(String)](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.addbusinesscardlogopicture?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_AddBusinessCardLogoPicture_System_String_), [ForwardAsBusinessCard()](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.forwardasbusinesscard?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_ForwardAsBusinessCard), [ResetBusinessCard()](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.resetbusinesscard?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_ResetBusinessCard), [SaveBusinessCardImage(String)](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.savebusinesscardimage?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_SaveBusinessCardImage_System_String_) und [ShowBusinessCardEditor()](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.showbusinesscardeditor?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_ShowBusinessCardEditor).

Im folgenden Codebeispiel ändert BusinessCardLayoutExample das Layout einer elektronischen Visitenkarte, indem zuerst ein angegebenes **ContactItem**-Objekt abgerufen wird. In diesem Fall stellt das **ContactItem**-Objekt einen Kontakt dar, dessen [Subject](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.subject?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_Subject)-Eigenschaft den Wert „Melissa MacBeth“ hat. Anschließend erstellt BusinessCardLayoutExample eine XML-Dokumentklasse [XmlDocument](https://msdn.microsoft.com/library/6kza7w4k) und ruft dann das Layoutattribut der Klasse in einer Zeichenfolge ab, wobei der **BusinessCardLayoutXML**-Wert für das **ContactItem-Objekt** verwendet wird. Das Kartenlayout wird dann von links- zu rechtsbündig geändert.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void BusinessCardLayoutExample()
{
    Outlook.ContactItem contact =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find(
        "[Subject] = Melissa MacBeth'")
        as Outlook.ContactItem;
    if (contact != null)
    {
        XmlDocument doc = new XmlDocument();
        doc.LoadXml(contact.BusinessCardLayoutXml);
        XmlElement root = doc.DocumentElement;
        string layoutValue = root.GetAttribute("layout");
        if (layoutValue == "left")
        {
            root.SetAttribute("layout", "right");
            contact.BusinessCardLayoutXml = doc.OuterXml;
            contact.Save();
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Elektronische Visitenkarten](electronic-business-cards.md)

