---
title: Column-Objekt (ADOX)
TOCTitle: Column object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 188f70d32237385cd82979589aecb989f18748b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296248"
---
# <a name="column-object-adox"></a><span data-ttu-id="55654-102">Column-Objekt (ADOX)</span><span class="sxs-lookup"><span data-stu-id="55654-102">Column object (ADOX)</span></span>


<span data-ttu-id="55654-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="55654-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="55654-104">Stellt eine Spalte aus einer Tabelle, einem Index oder einem Schlüssel dar.</span><span class="sxs-lookup"><span data-stu-id="55654-104">Represents a column from a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="55654-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55654-105">Remarks</span></span>

<span data-ttu-id="55654-106">Mit dem folgenden Code wird ein neues **Column**-Objekt erstellt:</span><span class="sxs-lookup"><span data-stu-id="55654-106">The following code creates a new **Column**:</span></span>

`Dim obj As New Column`

<span data-ttu-id="55654-107">Die Eigenschaften und Auflistungen eines **Column** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="55654-107">With the properties and collections of a **Column** object, you can:</span></span>

  - <span data-ttu-id="55654-108">Identifizieren der Spalte, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="55654-108">Identify the column with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="55654-109">Angeben des Datentyps für die Spalte, indem Sie die [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="55654-109">Specify the data type of the column with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property.</span></span>

  - <span data-ttu-id="55654-110">Bestimmen, ob die Spalte eine feste Länge hat oder ob sie Nullwerte enthalten kann, indem Sie die [Attributes](attributes-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="55654-110">Determine if the column is fixed-length, or if it can contain null values with the [Attributes](attributes-property-adox.md) property.</span></span>

  - <span data-ttu-id="55654-111">Angeben der maximalen Spaltengröße, indem Sie die [DefinedSize](definedsize-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="55654-111">Specify the maximum size of the column with the [DefinedSize](definedsize-property-adox.md) property.</span></span>

  - <span data-ttu-id="55654-112">Für numerische Datenwerte: Angeben der Skalierung, indem Sie die [NumericScale](numericscale-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="55654-112">For numeric data values, specify the scale with the [NumericScale](numericscale-property-adox.md) property.</span></span>

  - <span data-ttu-id="55654-113">Für numerische Datenwerte: Angeben der höchsten Genauigkeit, indem Sie die [Precision](precision-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="55654-113">For numeric data value, specify the maximum precision with the [Precision](precision-property-adox.md) property.</span></span>

  - <span data-ttu-id="55654-114">Angeben des [Catalog](catalog-object-adox.md)-Objekts, das im Besitz der Spalte ist, indem Sie die [ParentCatalog](parentcatalog-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="55654-114">Specify the [Catalog](catalog-object-adox.md) that owns the column with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

  - <span data-ttu-id="55654-115">Für Schlüsselspalten: Angeben des Namens der verwandten Spalte in der verwandten Tabelle, indem Sie die [RelatedColumn](relatedcolumn-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="55654-115">For key columns, specify the name of the related column in the related table with the [RelatedColumn](relatedcolumn-property-adox.md) property.</span></span>

  - <span data-ttu-id="55654-116">Für Indexspalten: Angeben, ob die Daten auf- oder absteigend sortiert werden, indem Sie die [SortOrder](sortorder-property-adox.md)-Eigenschaften verwenden.</span><span class="sxs-lookup"><span data-stu-id="55654-116">For index columns, specify whether the sort order is ascending or descending with the [SortOrder](sortorder-property-adox.md) property.</span></span>

  - <span data-ttu-id="55654-117">Zugreifen auf anbieterspezifische Eigenschaften mit der [Properties](properties-collection-ado.md)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="55654-117">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="55654-p101">[!HINWEIS] Möglicherweise werden nicht alle Eigenschaften für **Column** -Objekte von Ihrem Datenprovider unterstützt. Wenn Sie einen Wert für eine Eigenschaft festlegen, die nicht vom Provider unterstützt wird, tritt ein Fehler auf. Bei neuen **Column** -Objekten tritt der Fehler auf, wenn das Objekt der Auflistung hinzugefügt wird. Bei vorhandenen Objekten tritt der Fehler auf, wenn die Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="55654-p101">Not all properties of **Column** objects may be supported by your data provider. An error will occur if you have set a value for a property that the provider does not support. For new **Column** objects, the error will occur when the object is appended to the collection. For existing objects, the error will occur when setting the property.</span></span>
> 
> <span data-ttu-id="55654-p102">Beim Erstellen von **Column** -Objekten gewährleistet das Vorhandensein eines entsprechenden Standardwerts für eine optionale Eigenschaft nicht, dass diese Eigenschaft vom Provider unterstützt wird. Weitere Informationen zu den vom Provider unterstützten Eigenschaften finden Sie in der Providerdokumentation.</span><span class="sxs-lookup"><span data-stu-id="55654-p102">When creating **Column** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property. For more information about which properties your provider supports, see your provider documentation.</span></span>

