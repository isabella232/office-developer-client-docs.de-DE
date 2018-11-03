---
title: Name-Eigenschaft (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a65bad49c7b9b7a7af91403b1119923b62daa04a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931246"
---
# <a name="name-property-adox"></a><span data-ttu-id="4a399-102">Name-Eigenschaft (ADOX)</span><span class="sxs-lookup"><span data-stu-id="4a399-102">Name property (ADOX)</span></span>


<span data-ttu-id="4a399-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a399-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a399-104">Gibt den Namen des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="4a399-104">Indicates the name of the object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4a399-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4a399-105">Settings and return values</span></span>

<span data-ttu-id="4a399-106">Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4a399-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a399-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4a399-107">Remarks</span></span>

<span data-ttu-id="4a399-108">Namen müssen innerhalb einer Auflistung nicht eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="4a399-108">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="4a399-p101">Die **Name** -Eigenschaft verfügt über Lese-/Schreibzugriff für [Column](column-object-adox.md)-, [Group](group-object-adox.md)-, [Key](key-object-adox.md)-, [Index](index-object-adox.md)-, [Table](table-object-adox.md)- und [User](user-object-adox.md)-Objekte. Die **Name** -Eigenschaft ist schreibgeschützt für [Catalog](catalog-object-adox.md)-, [Procedure](procedure-object-adox.md)- und [View](view-object-adox.md)-Objekte.</span><span class="sxs-lookup"><span data-stu-id="4a399-p101">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects. The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="4a399-111">Für Objekte mit Lese-/Schreibzugriff (**Column**-, **Group**-, **Key**-, **Index**-, **Table**- und **User**-Objekte) ist der Standardwert eine leere Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="4a399-111">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>


> [!NOTE]
> <P><span data-ttu-id="4a399-112">[!HINWEIS] Diese Eigenschaft ist schreibgeschützt für <STRONG>Key</STRONG> -Objekte, die bereits an eine Auflistung angefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="4a399-112">For keys, this property is read-only on <STRONG>Key</STRONG> objects already appended to a collection.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="4a399-113">[!HINWEIS] Diese Eigenschaft ist schreibgeschützt für <STRONG>Table</STRONG> -Objekte, die bereits an eine Auflistung angefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="4a399-113">For tables, this property is read-only for <STRONG>Table</STRONG> objects already appended to a collection.</span></span></P>


