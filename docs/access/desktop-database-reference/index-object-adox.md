---
title: Index-Objekt (ADOX)
TOCTitle: Index Object (ADOX)
ms:assetid: fe368ab1-e396-4684-d930-18b0ba58a925
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250304(v=office.15)
ms:contentKeyID: 48548929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 682811352f1b218633cf4a925d4468322d9386d3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870639"
---
# <a name="index-object-adox"></a><span data-ttu-id="8bc9b-102">Index-Objekt (ADOX)</span><span class="sxs-lookup"><span data-stu-id="8bc9b-102">Index Object (ADOX)</span></span>

<span data-ttu-id="8bc9b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8bc9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8bc9b-104">Stellt einen Index aus einer Datenbanktabelle dar.</span><span class="sxs-lookup"><span data-stu-id="8bc9b-104">Represents an index from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bc9b-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8bc9b-105">Remarks</span></span>

<span data-ttu-id="8bc9b-106">Mit dem folgenden Code wird ein neues **Index** -Objekt erstellt:</span><span class="sxs-lookup"><span data-stu-id="8bc9b-106">The following code creates a new **Index**:</span></span>

`Dim obj As New Index`

<span data-ttu-id="8bc9b-107">Die Eigenschaften und Auflistungen eines **Index** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8bc9b-107">With the properties and collections of an **Index** object, you can:</span></span>

  - <span data-ttu-id="8bc9b-108">Identifizieren des Indexes, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="8bc9b-108">Identify the index with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="8bc9b-109">Zugreifen auf die Datenbankspalten des Indexes, indem Sie die [Columns](columns-collection-adox.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="8bc9b-109">Access the database columns of the index with the [Columns](columns-collection-adox.md) collection.</span></span>

  - <span data-ttu-id="8bc9b-110">Angeben, ob die Indexschlüssel eindeutig sein müssen, indem Sie die [Unique](unique-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="8bc9b-110">Specify whether the index keys must be unique with the [Unique](unique-property-adox.md) property.</span></span>

  - <span data-ttu-id="8bc9b-111">Angeben, ob der Index den Primärschlüssel einer Tabelle darstellt, indem Sie die [PrimaryKey](primarykey-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="8bc9b-111">Specify whether the index is the primary key for a table with the [PrimaryKey](primarykey-property-adox.md) property.</span></span>

  - <span data-ttu-id="8bc9b-112">Angeben, ob Datensätze mit Nullwerten im Indexfeld über Indexeinträge verfügen, indem Sie die [IndexNulls](indexnulls-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="8bc9b-112">Specify whether records that have null values in their index fields have index entries with the [IndexNulls](indexnulls-property-adox.md) property.</span></span>

  - <span data-ttu-id="8bc9b-113">Angeben, ob der Index gruppiert ist, indem Sie die [Clustered](clustered-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="8bc9b-113">Specify whether the index is clustered with the [Clustered](clustered-property-adox.md) property.</span></span>

  - <span data-ttu-id="8bc9b-114">Zugreifen auf anbieterspezifische Indexeigenschaften mit der [Properties](properties-collection-ado.md)-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="8bc9b-114">Access provider-specific index properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="8bc9b-115">[!HINWEIS] Es tritt ein Fehler auf, wenn ein [Column](column-object-adox.md)-Objekt an die **Columns** -Auflistung eines **Index** -Objekts angefügt wird und das **Column** -Objekt nicht in einem [Table](table-object-adox.md)-Objekt vorhanden ist, das bereits an die [Tables](tables-collection-adox.md)-Auflistung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="8bc9b-115">An error will occur when appending a [Column](column-object-adox.md) to the **Columns** collection of an **Index** if the **Column** does not exist in a [Table](table-object-adox.md) object already appended to the [Tables](tables-collection-adox.md) collection.</span></span>

<span data-ttu-id="8bc9b-p101">Möglicherweise werden nicht alle Eigenschaften für **Index** -Objekte von Ihrem Datenprovider unterstützt. Wenn Sie einen Wert für eine Eigenschaft festlegen, die nicht vom Provider unterstützt wird, tritt ein Fehler auf. Bei neuen **Index** -Objekten tritt der Fehler auf, wenn das Objekt der Auflistung hinzugefügt wird. Bei vorhandenen Objekten tritt der Fehler auf, wenn die Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8bc9b-p101">Your data provider may not support all properties of **Index** objects. An error will occur if you have set a value for a property that is not supported by the provider. For new **Index** objects, the error will occur when the object is appended to the collection. For existing objects, the error will occur when setting the property.</span></span>

<span data-ttu-id="8bc9b-p102">Beim Erstellen von **Index** -Objekten gewährleistet das Vorhandensein eines entsprechenden Standardwerts für eine optionale Eigenschaft nicht, dass diese Eigenschaft vom Provider unterstützt wird. Weitere Informationen zu den vom Provider unterstützten Eigenschaften finden Sie in der Providerdokumentation.</span><span class="sxs-lookup"><span data-stu-id="8bc9b-p102">When creating **Index** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property. For more information about which properties your provider supports, see your provider documentation.</span></span>

