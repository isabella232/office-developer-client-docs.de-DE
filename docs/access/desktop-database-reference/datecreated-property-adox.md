---
title: DateCreated-Eigenschaft (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 59b19ab3be6633daf7295a63a33a31a34b64fbd7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294421"
---
# <a name="datecreated-property-adox"></a><span data-ttu-id="79594-102">DateCreated-Eigenschaft (ADOX)</span><span class="sxs-lookup"><span data-stu-id="79594-102">DateCreated property (ADOX)</span></span>


<span data-ttu-id="79594-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="79594-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="79594-104">Gibt das Erstellungsdatum des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="79594-104">Indicates the date the object was created.</span></span>

## <a name="return-values"></a><span data-ttu-id="79594-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="79594-105">Return values</span></span>

<span data-ttu-id="79594-106">Diese Eigenschaft gibt einen **Variant**-Wert zurück, der das Erstellungsdatum angibt.</span><span class="sxs-lookup"><span data-stu-id="79594-106">Returns a **Variant** value specifying the date created.</span></span> <span data-ttu-id="79594-107">Der Wert ist Null, wenn **DateCreated** nicht vom Anbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="79594-107">The value is null if **DateCreated** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="79594-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79594-108">Remarks</span></span>

<span data-ttu-id="79594-p102">Die **DateCreated**-Eigenschaft ist Null für neu angefügte Objekte. Nach Anfügen eines neuen [View](view-object-adox.md)- oder [Procedure](procedure-object-adox.md)-Objekts, müssen Sie die [Refresh](refresh-method-ado.md)-Methode der [Views](views-collection-adox.md)- oder [Procedures](procedures-collection-adox.md)-Auflistung aufrufen, um Werte für die **DateCreated**-Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="79594-p102">The **DateCreated** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateCreated** property.</span></span>

