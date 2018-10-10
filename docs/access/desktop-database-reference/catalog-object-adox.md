---
title: Catalog-Objekt (ADOX)
TOCTitle: Catalog Object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 04622cd636d73beaf3124cda2584299443467973
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473147"
---
# <a name="catalog-object-adox"></a><span data-ttu-id="9abf6-102">Catalog-Objekt (ADOX)</span><span class="sxs-lookup"><span data-stu-id="9abf6-102">Catalog Object (ADOX)</span></span>


<span data-ttu-id="9abf6-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9abf6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9abf6-104">Enthält Auflistungen ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md) und [Procedures](procedures-collection-adox.md)), die den Schemakatalog einer Datenquelle beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9abf6-104">Contains collections ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md), and [Procedures](procedures-collection-adox.md)) that describe the schema catalog of a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="9abf6-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9abf6-105">Remarks</span></span>

<span data-ttu-id="9abf6-p101">Sie können das **Catalog** -Objekt ändern, indem Sie Objekte hinzufügen oder entfernen oder vorhandene Objekte bearbeiten. Einige Anbieter unterstützen möglicherweise nicht alle **Catalog** -Objekte oder sie unterstützen nur das Anzeigen von Schemainformationen.</span><span class="sxs-lookup"><span data-stu-id="9abf6-p101">You can modify the **Catalog** object by adding or removing objects or by modifying existing objects. Some providers may not support all of the **Catalog** objects or may support only viewing schema information.</span></span>

<span data-ttu-id="9abf6-108">Die Eigenschaften und Methoden eines **Catalog** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9abf6-108">With the properties and methods of a **Catalog** object, you can:</span></span>

  - <span data-ttu-id="9abf6-109">Öffnen des Katalogs, indem Sie für die [ActiveConnection](activeconnection-property-adox.md)-Eigenschaft ein [Connection](connection-object-ado.md)-ADO-Objekt oder eine gültige Verbindungszeichenfolge festlegen.</span><span class="sxs-lookup"><span data-stu-id="9abf6-109">Open the catalog by setting the [ActiveConnection](activeconnection-property-adox.md) property to an ADO [Connection](connection-object-ado.md) object or a valid connection string.</span></span>

  - <span data-ttu-id="9abf6-110">Erstellen eines neuen Katalogs, indem Sie die [Create](create-method-adox.md)-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="9abf6-110">Create a new catalog with the [Create](create-method-adox.md) method.</span></span>

  - <span data-ttu-id="9abf6-111">Bestimmen der Besitzer von Objekten in einem **Catalog** -Objekt, indem Sie die Methoden [GetObjectOwner](getobjectowner-method-adox.md) und [SetObjectOwner](https://msdn.microsoft.com/library/jj249006\(v=office.15\)) verwenden.</span><span class="sxs-lookup"><span data-stu-id="9abf6-111">Determine the owners of the objects in a **Catalog** with the [GetObjectOwner](getobjectowner-method-adox.md) and [SetObjectOwner](https://msdn.microsoft.com/library/jj249006\(v=office.15\)) methods.</span></span>

