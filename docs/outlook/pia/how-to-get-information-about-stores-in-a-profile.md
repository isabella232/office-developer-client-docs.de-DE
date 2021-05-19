---
title: Abrufen von Informationen zu Speichern in einem Profil
TOCTitle: Get information about stores in a profile
ms:assetid: e88222d2-e1b7-4393-aac4-5ce9d24d5d5b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184648(v=office.15)
ms:contentKeyID: 55119893
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2044fc52370bdadd5c7f01debbd02c88dd881715
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349420"
---
# <a name="get-information-about-stores-in-a-profile"></a><span data-ttu-id="fdccf-102">Abrufen von Informationen zu Speichern in einem Profil</span><span class="sxs-lookup"><span data-stu-id="fdccf-102">Get information about stores in a profile</span></span>

<span data-ttu-id="fdccf-103">In diesem Beispiel wird veranschaulicht, wie Speicher in einem Profil abgerufen und aufgezählt werden.</span><span class="sxs-lookup"><span data-stu-id="fdccf-103">This example shows how to get and enumerate stores in a profile.</span></span>

## <a name="example"></a><span data-ttu-id="fdccf-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fdccf-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="fdccf-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="fdccf-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="fdccf-106">Sie können die [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\))-Auflistung zum Aufzählen der Speicher für ein bestimmtes Profil verwenden.</span><span class="sxs-lookup"><span data-stu-id="fdccf-106">You can use the [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) collection to enumerate the stores for a given profile.</span></span> <span data-ttu-id="fdccf-107">Die **Stores**-Auflistung enthält Elemente, die Informationen zu den einzelnen [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\))-Objekten verfügbar machen, z. B. wenn ein **Store**-Objekt hinzugefügt wurde oder wenn ein **Store**-Objekt in dem aktuellen Profil entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fdccf-107">The **Stores** collection provides members that expose information about each [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object, such as when a **Store** object has been added or when a **Store** object is about to be removed in the current profile.</span></span> <span data-ttu-id="fdccf-108">Im nachstehenden Codebeispiel ruft EnumerateStores das **Store**-Objekt ab, das Speicher im aktuellen Profil darstellt, und die Speicher werden aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="fdccf-108">In the following code example, EnumerateStores gets the **Stores** object that represents stores in the current profile, and enumerates the stores.</span></span> <span data-ttu-id="fdccf-109">EnumerateStores prüft jedes **Store**-Objekt in der **Stores**-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="fdccf-109">EnumerateStores examines each **Store** object in the **Stores** collection.</span></span> <span data-ttu-id="fdccf-110">Wenn die [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\))-Eigenschaft **true** zurückgibt, wodurch angegeben wird, dass es sich um eine PST- oder OST-Datei handelt, so werden die Eigenschaften [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) und [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) in die Listener der Ablaufverfolgung in der [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx)-Auflistung geschrieben.</span><span class="sxs-lookup"><span data-stu-id="fdccf-110">If the [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) property returns **true**, indicating that it is a .pst or .ost store, the [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) and [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) properties are written to the trace listeners in the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="fdccf-111">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="fdccf-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="fdccf-112">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fdccf-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="fdccf-113">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="fdccf-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="fdccf-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fdccf-114">See also</span></span>

- [<span data-ttu-id="fdccf-115">Stores</span><span class="sxs-lookup"><span data-stu-id="fdccf-115">Stores</span></span>](stores.md)

