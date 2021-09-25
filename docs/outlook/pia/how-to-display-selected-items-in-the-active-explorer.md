---
title: Anzeigen von ausgewählten Elementen im aktiven Explorer
TOCTitle: Display selected items in the active Explorer
ms:assetid: 31bb217b-8b45-4b50-942e-b6c2a7f13c83
ms:mtpsurl: https://msdn.microsoft.com/library/Dn292517(v=office.15)
ms:contentKeyID: 55119844
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 414bf56410311a960e79cd27b49459787490ce08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590758"
---
# <a name="display-selected-items-in-the-active-explorer"></a>Anzeigen von ausgewählten Elementen im aktiven Explorer

Dieses Beispiel zeigt, wie Sie mit der OutlookItem-Hilfsklasse problemlos alle im aktiven Explorer-Fenster ausgewählten anzeigen.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Das [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\))-Objekt enthält die Gruppe von Outlook-Elementen, die aktuell im aktiven Outlook-Explorer ausgewählt sind. Weder der aktive Explorer, der durch [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)) dargestellt ist, noch die Gruppe der ausgewählten Elementen gibt den Typ der ausgewählten Elemente an. In der Regel müssen Sie zunächst den Elementtyp identifizieren und dann die spezifische **Display**-Methode für diesen Typ aufrufen. Da die **Display**-Methode für alle Outlook-Elementobjekte gleich ist und die OutlookItem-Hilfsklasse diese Methode enthält, können Sie die Hilfsklasse nutzen, indem Sie eine Instanz des OutlookItem-Objekts (myItem) deklarieren und myItem.Display zum Anzeigen der jeweiligen Elemente in der Auswahl verwenden. Informationen zur Implementierung der OutlookItem-Hilfsklasse finden Sie unter [Erstellen einer Hilfsklasse zum Zugriff auf allgemeine Member von Outlook-Elementen](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySelectedItems()
{
    Outlook.Selection selection =
        Application.ActiveExplorer().Selection;
    for (int i = 1; i <= selection.Count; i++)
    {
        OutlookItem myItem = new OutlookItem(selection[i]);
        myItem.Display();
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Erstellen einer Hilfsklasse zum Zugriff auf allgemeine Member von Outlook-Elementen](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [Allgemeine Outlook-Elemente](general-outlook-items.md)

