---
title: Append-Methode (ADOX Columns)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 12e79802587874aacb5b47a56387e331b8148069
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026372"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="b35df-102">Append-Methode (ADOX Columns)</span><span class="sxs-lookup"><span data-stu-id="b35df-102">Append method (ADOX Columns)</span></span>

<span data-ttu-id="b35df-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b35df-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b35df-104">Fügt der [Columns](column-object-adox.md)-Auflistung ein neues [Column](columns-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="b35df-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b35df-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b35df-105">Syntax</span></span>

<span data-ttu-id="b35df-106">*Spalten*.</span><span class="sxs-lookup"><span data-stu-id="b35df-106">*Columns*.</span></span> <span data-ttu-id="b35df-107">Fügen Sie die*Spalte* \[,*Typ* \] \[,*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="b35df-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="b35df-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b35df-108">Parameters</span></span>

|<span data-ttu-id="b35df-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b35df-109">Parameter</span></span>|<span data-ttu-id="b35df-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b35df-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b35df-111">*Column*</span><span class="sxs-lookup"><span data-stu-id="b35df-111">*Column*</span></span> |<span data-ttu-id="b35df-112">Das anzufügende **Column** -Objekt oder der Name der zu erstellenden und anzufügenden Spalte.</span><span class="sxs-lookup"><span data-stu-id="b35df-112">The **Column** object to append or the name of the column to create and append.</span></span>|
|<span data-ttu-id="b35df-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="b35df-113">*Type*</span></span> |<span data-ttu-id="b35df-114">Optional.</span><span class="sxs-lookup"><span data-stu-id="b35df-114">Optional.</span></span> <span data-ttu-id="b35df-115">Ein **Long** -Wert, der den Datentyp der Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="b35df-115">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="b35df-116">Die [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) -Eigenschaft ein **Column** -Objekt entspricht der *Type* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="b35df-116">The *Type* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property of a **Column** object.</span></span>|
|<span data-ttu-id="b35df-117">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="b35df-117">*DefinedSize*</span></span> |<span data-ttu-id="b35df-118">Optional.</span><span class="sxs-lookup"><span data-stu-id="b35df-118">Optional.</span></span> <span data-ttu-id="b35df-119">Ein **Long** -Wert, der die Größe einer Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="b35df-119">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="b35df-120">Der Parameter *DefinedSize* entspricht der [DefinedSize](definedsize-property-adox.md) -Eigenschaft eines **Column** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b35df-120">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>|


> [!NOTE]
> <span data-ttu-id="b35df-121">[!HINWEIS] Es tritt ein Fehler auf, wenn ein **Column** -Objekt an die **Columns** -Auflistung eines [Index](index-object-adox.md)-Objekts angefügt wird und das **Column** -Objekt nicht in einem [Table](table-object-adox.md)-Objekt vorhanden ist, das bereits an die [Tables](tables-collection-adox.md)-Auflistung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b35df-121">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


