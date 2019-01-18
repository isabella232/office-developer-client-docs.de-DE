---
title: Item-Eigenschaft (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cc38101cb17c52bf2c8c08c08c14163c3772b2f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718560"
---
# <a name="item-property-ado"></a><span data-ttu-id="d3a58-102">Item-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="d3a58-102">Item property (ADO)</span></span>

<span data-ttu-id="d3a58-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3a58-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3a58-104">Gibt ein bestimmtes Element einer Auflistung nach Name oder Ordnungszahl an.</span><span class="sxs-lookup"><span data-stu-id="d3a58-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3a58-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3a58-105">Syntax</span></span>

<span data-ttu-id="d3a58-106">Legen Sie*Objekt* = *Auflistung*. Item (Index)</span><span class="sxs-lookup"><span data-stu-id="d3a58-106">Set*object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="d3a58-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3a58-107">Return value</span></span>

<span data-ttu-id="d3a58-108">Gibt einen Objektverweis zurück.</span><span class="sxs-lookup"><span data-stu-id="d3a58-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3a58-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3a58-109">Parameters</span></span>

|<span data-ttu-id="d3a58-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3a58-110">Parameter</span></span>|<span data-ttu-id="d3a58-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3a58-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d3a58-112">*Index*</span><span class="sxs-lookup"><span data-stu-id="d3a58-112">*Index*</span></span> |<span data-ttu-id="d3a58-113">Ein **Variant** -Ausdruck, der als Name oder Ordnungszahl eines Objekts in einer Auflistung ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="d3a58-113">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d3a58-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d3a58-114">Remarks</span></span>

<span data-ttu-id="d3a58-115">Verwenden Sie die **Item** -Eigenschaft, um ein bestimmtes Objekt in einer Auflistung zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="d3a58-115">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="d3a58-116">Wenn das **Element** ein Objekt in der Auflistung entspricht dem *Index* -Argument nicht finden kann, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="d3a58-116">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="d3a58-117">Darüber hinaus unterstützen einige Sammlungen nicht benannte Objekte; für diese Auflistungen müssen Sie die Ordnungszahl Verweise verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3a58-117">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="d3a58-118">Die **Item** -Eigenschaft ist die Standardeigenschaft für alle Auflistungen. Die folgenden Syntaxformen sind deshalb austauschbar:</span><span class="sxs-lookup"><span data-stu-id="d3a58-118">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
