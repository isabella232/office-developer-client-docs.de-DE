---
title: Ändern des Layouts einer elektronischen Visitenkarte
TOCTitle: Modify the layout of an electronic business card
ms:assetid: f387c4a7-59c5-4b6a-b33a-1bfa7d499bbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184653(v=office.15)
ms:contentKeyID: 55119838
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7f85324b31ae865c69e2c40806d9654a0b443f4b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722739"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a>Ändern des Layouts einer elektronischen Visitenkarte

Dieses Beispiel zeigt, wie das Layout einer elektronischen Visitenkarte mithilfe der [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\))-Eigenschaft der [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\))-Schnittstelle geändert wird.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Eine elektronische Visitenkarte enthält eine Ansicht eines Kontakts, in der bestimmte Informationen aus einem Kontakt erfasst sind. Die **ContactItem**-Schnittstelle bietet bestimmte Member, die elektronische Visitenkarten betreffen. Diese Member sind **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)), [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)), [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)), [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)), [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)) und [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)).

Im folgenden Codebeispiel ändert BusinessCardLayoutExample das Layout einer elektronischen Visitenkarte, indem zuerst ein angegebenes **ContactItem**-Objekt abgerufen wird. In diesem Fall stellt das **ContactItem**-Objekt einen Kontakt dar, dessen [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\))-Eigenschaft den Wert „Melissa MacBeth“ hat. Anschließend erstellt BusinessCardLayoutExample eine XML-Dokumentklasse [XmlDocument](https://msdn.microsoft.com/en-us/library/6kza7w4k) und ruft dann das Layoutattribut der Klasse in einer Zeichenfolge ab, wobei der **BusinessCardLayoutXML**-Wert für das **ContactItem-Objekt** verwendet wird. Das Kartenlayout wird dann von links- zu rechtsbündig geändert.

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

