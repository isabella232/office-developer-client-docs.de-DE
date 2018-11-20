---
title: Table-Objekt (ADOX)
TOCTitle: Table object (ADOX)
ms:assetid: 53a3e2f9-4ec0-8fed-d482-4f995921587b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249273(v=office.15)
ms:contentKeyID: 48544874
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 19f30bec624a43bc1b821d8bef01afa166b0c544
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026428"
---
# <a name="table-object-adox"></a><span data-ttu-id="9360a-102">Table-Objekt (ADOX)</span><span class="sxs-lookup"><span data-stu-id="9360a-102">Table object (ADOX)</span></span>

<span data-ttu-id="9360a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9360a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9360a-104">Stellt eine Datenbanktabelle dar, einschließlich Spalten, Indizes und Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="9360a-104">Represents a database table including columns, indexes, and keys.</span></span>

## <a name="remarks"></a><span data-ttu-id="9360a-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9360a-105">Remarks</span></span>

<span data-ttu-id="9360a-106">Mit dem folgenden Code wird ein neues **Table** -Objekt erstellt:</span><span class="sxs-lookup"><span data-stu-id="9360a-106">The following code creates a new **Table**:</span></span>

`Dim obj As New Table`

<span data-ttu-id="9360a-107">Die Eigenschaften und Auflistungen eines **Table** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9360a-107">With the properties and collections of a **Table** object, you can:</span></span>

- <span data-ttu-id="9360a-108">Identifizieren der Tabelle, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="9360a-108">Identify the table with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="9360a-109">Bestimmen des Tabellentyps, indem Sie die [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="9360a-109">Determine the type of table with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox) property.</span></span>

- <span data-ttu-id="9360a-110">Zugreifen auf die Datenbankspalten der Tabelle, indem Sie die [Columns](columns-collection-adox.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="9360a-110">Access the database columns of the table with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="9360a-111">Zugreifen auf die Indizes der Tabelle, indem Sie die [Indexes](indexes-collection-adox.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="9360a-111">Access the indexes of the table with the [Indexes](indexes-collection-adox.md) collection.</span></span>

- <span data-ttu-id="9360a-112">Zugreifen auf die Schlüssel der Tabelle, indem Sie die [Keys](keys-collection-adox.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="9360a-112">Access the keys of the table with the [Keys](keys-collection-adox.md) collection.</span></span>

- <span data-ttu-id="9360a-113">Angeben des [Catalog](catalog-object-adox.md)-Objekts, das im Besitz der Tabelle ist, indem Sie die [ParentCatalog](parentcatalog-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="9360a-113">Specify the [Catalog](catalog-object-adox.md) that owns the table with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

- <span data-ttu-id="9360a-114">Zurückgeben von Datumsinformationen, indem Sie die Eigenschaften [DateCreated](datecreated-property-adox.md) und [DateModified](datemodified-property-adox.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="9360a-114">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

- <span data-ttu-id="9360a-115">Zugreifen auf anbieterspezifische Tabelleneigenschaften mit der [Properties](properties-collection-ado.md)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="9360a-115">Access provider-specific table properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="9360a-p101">[!HINWEIS] Möglicherweise werden nicht alle Eigenschaften für **Table** -Objekte von Ihrem Datenprovider unterstützt. Wenn Sie einen Wert für eine Eigenschaft festlegen, die nicht vom Provider unterstützt wird, tritt ein Fehler auf. Bei neuen **Table** -Objekten tritt der Fehler auf, wenn das Objekt der Auflistung hinzugefügt wird. Bei vorhandenen Objekten tritt der Fehler auf, wenn die Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="9360a-p101">Your data provider may not support all properties of **Table** objects. An error will occur if you have set a value for a property that the provider does not support. For new **Table** objects, the error will occur when the object is appended to the collection. For existing objects, the error will occur when setting the property.</span></span>

<span data-ttu-id="9360a-p102">Beim Erstellen von **Table** -Objekten gewährleistet das Vorhandensein eines entsprechenden Standardwerts für eine optionale Eigenschaft nicht, dass diese Eigenschaft vom Provider unterstützt wird. Weitere Informationen zu den vom Provider unterstützten Eigenschaften finden Sie in der Providerdokumentation.</span><span class="sxs-lookup"><span data-stu-id="9360a-p102">When creating **Table** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property. For more information about which properties your provider supports, see your provider documentation.</span></span>

