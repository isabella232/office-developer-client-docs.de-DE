---
title: Name-Eigenschaft (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c7021c6f97d1aaa9c82e65eab98a3259d6eb87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288651"
---
# <a name="name-property-adox"></a><span data-ttu-id="a75ab-102">Name-Eigenschaft (ADOX)</span><span class="sxs-lookup"><span data-stu-id="a75ab-102">Name property (ADOX)</span></span>

<span data-ttu-id="a75ab-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a75ab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a75ab-104">Gibt den Namen des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="a75ab-104">Indicates the name of the object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a75ab-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a75ab-105">Settings and return values</span></span>

<span data-ttu-id="a75ab-106">Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a75ab-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a75ab-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a75ab-107">Remarks</span></span>

<span data-ttu-id="a75ab-108">Namen müssen innerhalb einer Auflistung nicht eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="a75ab-108">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="a75ab-p101">Die **Name** -Eigenschaft verfügt über Lese-/Schreibzugriff für [Column](column-object-adox.md)-, [Group](group-object-adox.md)-, [Key](key-object-adox.md)-, [Index](index-object-adox.md)-, [Table](table-object-adox.md)- und [User](user-object-adox.md)-Objekte. Die **Name** -Eigenschaft ist schreibgeschützt für [Catalog](catalog-object-adox.md)-, [Procedure](procedure-object-adox.md)- und [View](view-object-adox.md)-Objekte.</span><span class="sxs-lookup"><span data-stu-id="a75ab-p101">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects. The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="a75ab-111">Für Objekte mit Lese-/Schreibzugriff (**Column**-, **Group**-, **Key**-, **Index**-, **Table**- und **User**-Objekte) ist der Standardwert eine leere Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="a75ab-111">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>

> [!NOTE]
> - <span data-ttu-id="a75ab-112">Diese Eigenschaft ist schreibgeschützt für **Key**-Objekte, die bereits an eine Auflistung angefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="a75ab-112">For keys, this property is read-only on **Key** objects already appended to a collection.</span></span>
> - <span data-ttu-id="a75ab-113">[!HINWEIS] Diese Eigenschaft ist schreibgeschützt für **Table** -Objekte, die bereits an eine Auflistung angefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="a75ab-113">For tables, this property is read-only for **Table** objects already appended to a collection.</span></span>


