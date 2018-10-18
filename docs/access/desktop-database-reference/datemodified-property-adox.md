---
title: DateModified-Eigenschaft (ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ceafd13b33536a77a1d793e7167fe8042609be5e
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603329"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="79e09-102">DateModified-Eigenschaft (ADOX)</span><span class="sxs-lookup"><span data-stu-id="79e09-102">DateModified Property (ADOX)</span></span>


<span data-ttu-id="79e09-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="79e09-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="79e09-104">Gibt das Datum an, an dem das Objekt zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="79e09-104">Indicates the date the object was last modified.</span></span>

<span data-ttu-id="79e09-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="79e09-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="79e09-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79e09-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="79e09-107">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="79e09-107">Return values</span></span>
>>>>>>> <span data-ttu-id="79e09-108">master</span><span class="sxs-lookup"><span data-stu-id="79e09-108">master</span></span>

<span data-ttu-id="79e09-p101">Diese Eigenschaft gibt einen **Variant** -Wert zurück, der das Änderungsdatum angibt. Der Wert ist Null, wenn **DateModified** nicht vom Anbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="79e09-p101">Returns a **Variant** value specifying the date modified. The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="79e09-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="79e09-111">Remarks</span></span>

<span data-ttu-id="79e09-p102">Die **DateModified** -Eigenschaft ist Null für neu angefügte Objekte. Nach Anfügen eines neuen [View](view-object-adox.md)- oder [Procedure](procedure-object-adox.md)-Objekts, müssen Sie die [Refresh](refresh-method-ado.md)-Methode der [Views](views-collection-adox.md)- oder [Procedures](procedures-collection-adox.md)-Auflistung aufrufen, um Werte für die **DateModified** -Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="79e09-p102">The **DateModified** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>

