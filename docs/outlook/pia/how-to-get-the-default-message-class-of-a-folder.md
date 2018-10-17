---
title: Abrufen der Standardnachrichtenklasse eines Ordners
TOCTitle: Get the default message class of a folder
ms:assetid: 1c5faefd-b180-4114-a955-3fc524210317
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184594(v=office.15)
ms:contentKeyID: 55119860
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: c03e0737a3dd2e74f39d90ffbac31bb134d16348
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407219"
---
# <a name="get-the-default-message-class-of-a-folder"></a><span data-ttu-id="0b03e-102">Abrufen der Standardnachrichtenklasse eines Ordners</span><span class="sxs-lookup"><span data-stu-id="0b03e-102">Get the default message class of a folder</span></span>

<span data-ttu-id="0b03e-103">In diesem Beispiel wird gezeigt, wie die [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\))-Eigenschaft verwendet wird, um die Standardnachrichtenklasse eines Ordners abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0b03e-103">This example shows how to use the [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) property to obtain the default message class of a folder.</span></span>

## <a name="example"></a><span data-ttu-id="0b03e-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0b03e-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="0b03e-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="0b03e-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="0b03e-106">Verwenden Sie die **DefaultMessageClass**-Eigenschaft des [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\))-Objekts, um die Standardnachrichtenklasse eines Ordners abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0b03e-106">To obtain the default message class for a folder, use the **DefaultMessageClass** property of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object.</span></span> <span data-ttu-id="0b03e-107">Ein [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekt mit der **DefaultMessageClass** „IPM.Contact“ bedeutet beispielsweise, dass es einen Ordner „Kontakte“ darstellt.</span><span class="sxs-lookup"><span data-stu-id="0b03e-107">For example, a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object that has a **DefaultMessageClass** of IPM.Contact means that it represents a Contact folder.</span></span> <span data-ttu-id="0b03e-108">Wenn der Ordner jedoch ein benutzerdefiniertes Formular aufweist oder ein Ersatzformular ein Standardformular aufweist, müssen Sie das [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\))-Objekt verwenden, um die Nachrichtenklasse des Standardformulars zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="0b03e-108">However, if the folder has a custom form or a replacement form as a default form, you must use the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object to determine the message class of the default form.</span></span> <span data-ttu-id="0b03e-109">Die **DefaultMessageClass**-Eigenschaft gibt nicht die Nachrichtenklasse des Standardformulars für den Ordner zurück.</span><span class="sxs-lookup"><span data-stu-id="0b03e-109">The **DefaultMessageClass** property does not return the message class of the default form for the folder.</span></span>

<span data-ttu-id="0b03e-110">Im folgenden Codebeispiel ermittelt die GetDefaultMessageClass-Prozedur anhand der **PropertyAccessor**-Klasse das Standardformular für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="0b03e-110">In the following code example, the   procedure uses the PropertyAccessor to determine the default form of a folder.</span></span> <span data-ttu-id="0b03e-111">Wenn die Ordnereigenschaft **PR\_DEF\_POST\_MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) nicht gefunden wird und in Outlook ein Fehler ausgelöst wird, gibt der**try…catch**-Block die **DefaultMessageClass**-Eigenschaft für das **Folder**-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="0b03e-111">If the folder property PR_DEF_POST_MSGCLASS (PidTagDefaultPostMessageClass) is not found and Outlook raises an error, the try…catch block returns the DefaultMessageClass property for the Folder.</span></span>

<span data-ttu-id="0b03e-112">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="0b03e-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="0b03e-113">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0b03e-113">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="0b03e-114">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="0b03e-114">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetDefaultMessageClass(Outlook.Folder folder)
{
    if (folder == null)
        throw new ArgumentNullException();
    try
    {
        const string PR_DEF_POST_MSGCLASS =
            @"https://schemas.microsoft.com/mapi/proptag/0x36E5001E";
        string messageClass =
            folder.PropertyAccessor.GetProperty(
            PR_DEF_POST_MSGCLASS).ToString();
        return messageClass;
    }
    catch
    {
        return folder.DefaultMessageClass;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="0b03e-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b03e-115">See also</span></span>

- [<span data-ttu-id="0b03e-116">Ordner</span><span class="sxs-lookup"><span data-stu-id="0b03e-116">Folders</span></span>](folders.md)

