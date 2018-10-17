---
title: Abrufen von Informationen zu Speichern in einem Profil
TOCTitle: Get information about stores in a profile
ms:assetid: e88222d2-e1b7-4393-aac4-5ce9d24d5d5b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184648(v=office.15)
ms:contentKeyID: 55119893
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 0229294cd6655f9017780ee0d9a7a23de76f2362
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406568"
---
# <a name="get-information-about-stores-in-a-profile"></a>Abrufen von Informationen zu Speichern in einem Profil

In diesem Beispiel wird veranschaulicht, wie Speicher in einem Profil abgerufen und aufgezählt werden.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Sie können die [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\))-Auflistung zum Aufzählen der Speicher für ein bestimmtes Profil verwenden. Die **Stores**-Auflistung enthält Elemente, die Informationen zu den einzelnen [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\))-Objekten verfügbar machen, z. B. wenn ein **Store**-Objekt hinzugefügt wurde oder wenn ein ** Store**-Objekt in dem aktuellen Profil entfernt werden soll. Im nachstehenden Codebeispiel ruft EnumerateStores das **Store**-Objekt ab, das Speicher im aktuellen Profil darstellt, und die Speicher werden aufgezählt. EnumerateStores prüft jedes **Store**-Objekt in der **Stores**-Auflistung. Wenn die [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\))-Eigenschaft **true** zurückgibt, wodurch angegeben wird, dass es sich um eine PST- oder OST-Datei handelt, so werden die Eigenschaften [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) und [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) in die Listener der Ablaufverfolgung in der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung geschrieben.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateStores()
{
    Outlook.Stores stores = Application.Session.Stores;
    foreach (Outlook.Store store in stores)
    {
        if (store.IsDataFileStore == true)
        {
            Debug.WriteLine(String.Format("Store: "
            + store.DisplayName
            + "\n" + "File Path: "
            + store.FilePath + "\n"));
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Spcicher](stores.md)

