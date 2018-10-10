---
title: DateModified-Eigenschaft (ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8465f97565d8519196b8221089121670ceedb275
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472980"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="35779-102">DateModified-Eigenschaft (ADOX)</span><span class="sxs-lookup"><span data-stu-id="35779-102">DateModified Property (ADOX)</span></span>


<span data-ttu-id="35779-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="35779-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="35779-104">Gibt das Datum an, an dem das Objekt zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="35779-104">Indicates the date the object was last modified.</span></span>

## <a name="return-values"></a><span data-ttu-id="35779-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="35779-105">Return Values</span></span>

<span data-ttu-id="35779-p101">Diese Eigenschaft gibt einen **Variant** -Wert zurück, der das Änderungsdatum angibt. Der Wert ist Null, wenn **DateModified** nicht vom Anbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="35779-p101">Returns a **Variant** value specifying the date modified. The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="35779-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="35779-108">Remarks</span></span>

<span data-ttu-id="35779-p102">Die **DateModified** -Eigenschaft ist Null für neu angefügte Objekte. Nach Anfügen eines neuen [View](view-object-adox.md)- oder [Procedure](procedure-object-adox.md)-Objekts, müssen Sie die [Refresh](refresh-method-ado.md)-Methode der [Views](views-collection-adox.md)- oder [Procedures](procedures-collection-adox.md)-Auflistung aufrufen, um Werte für die **DateModified** -Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="35779-p102">The **DateModified** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>

