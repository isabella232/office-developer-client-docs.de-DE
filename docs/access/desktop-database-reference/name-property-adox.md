---
title: Name-Eigenschaft (ADOX)
TOCTitle: Name Property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 51ea68718c7605df03ed8e4d44d4cb48011649fd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472927"
---
# <a name="name-property-adox"></a><span data-ttu-id="a8954-102">Name-Eigenschaft (ADOX)</span><span class="sxs-lookup"><span data-stu-id="a8954-102">Name Property (ADOX)</span></span>


<span data-ttu-id="a8954-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8954-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a8954-104">Gibt den Namen des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="a8954-104">Indicates the name of the object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a8954-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a8954-105">Settings and Return Values</span></span>

<span data-ttu-id="a8954-106">Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8954-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8954-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8954-107">Remarks</span></span>

<span data-ttu-id="a8954-108">Namen müssen innerhalb einer Auflistung nicht eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="a8954-108">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="a8954-p101">Die **Name** -Eigenschaft verfügt über Lese-/Schreibzugriff für [Column](column-object-adox.md)-, [Group](group-object-adox.md)-, [Key](key-object-adox.md)-, [Index](index-object-adox.md)-, [Table](table-object-adox.md)- und [User](user-object-adox.md)-Objekte. Die **Name** -Eigenschaft ist schreibgeschützt für [Catalog](catalog-object-adox.md)-, [Procedure](procedure-object-adox.md)- und [View](view-object-adox.md)-Objekte.</span><span class="sxs-lookup"><span data-stu-id="a8954-p101">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects. The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="a8954-111">Für Objekte mit Lese-/Schreibzugriff (**Column**-, **Group**-, **Key**-, **Index**-, **Table**- und **User**-Objekte) ist der Standardwert eine leere Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="a8954-111">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>


> [!NOTE]
> <P><span data-ttu-id="a8954-112">[!HINWEIS] Diese Eigenschaft ist schreibgeschützt für <STRONG>Key</STRONG> -Objekte, die bereits an eine Auflistung angefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="a8954-112">For keys, this property is read-only on <STRONG>Key</STRONG> objects already appended to a collection.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="a8954-113">[!HINWEIS] Diese Eigenschaft ist schreibgeschützt für <STRONG>Table</STRONG> -Objekte, die bereits an eine Auflistung angefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="a8954-113">For tables, this property is read-only for <STRONG>Table</STRONG> objects already appended to a collection.</span></span></P>


