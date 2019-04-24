---
title: DateModified-Eigenschaft (ADOX)
TOCTitle: DateModified property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: daf72804d51c18b5875e607ce5fdb0dfe20f406c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294407"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="44555-102">DateModified-Eigenschaft (ADOX)</span><span class="sxs-lookup"><span data-stu-id="44555-102">DateModified property (ADOX)</span></span>


<span data-ttu-id="44555-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="44555-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="44555-104">Gibt das Datum an, an dem das Objekt zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="44555-104">Indicates the date the object was last modified.</span></span>

## <a name="return-values"></a><span data-ttu-id="44555-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="44555-105">Return values</span></span>

<span data-ttu-id="44555-106">Diese Eigenschaft gibt einen **Variant** -Wert zurück, der das Änderungsdatum angibt.</span><span class="sxs-lookup"><span data-stu-id="44555-106">Returns a **Variant** value specifying the date modified.</span></span> <span data-ttu-id="44555-107">Der Wert ist Null, wenn **DateModified** nicht vom Anbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="44555-107">The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="44555-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44555-108">Remarks</span></span>

<span data-ttu-id="44555-p102">Die **DateModified**-Eigenschaft ist Null für neu angefügte Objekte. Nach Anfügen eines neuen [View](view-object-adox.md)- oder [Procedure](procedure-object-adox.md)-Objekts, müssen Sie die [Refresh](refresh-method-ado.md)-Methode der [Views](views-collection-adox.md)- oder [Procedures](procedures-collection-adox.md)-Auflistung aufrufen, um Werte für die **DateModified**-Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="44555-p102">The **DateModified** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>

