---
title: Item-Eigenschaft (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4afbb31fb95aeea66d9cf93624b95c8796e2d25
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949362"
---
# <a name="item-property-ado"></a><span data-ttu-id="bae79-102">Item-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="bae79-102">Item property (ADO)</span></span>

<span data-ttu-id="bae79-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bae79-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bae79-104">Gibt ein bestimmtes Element einer Auflistung nach Name oder Ordnungszahl an.</span><span class="sxs-lookup"><span data-stu-id="bae79-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="bae79-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bae79-105">Syntax</span></span>

<span data-ttu-id="bae79-106">Legen Sie*Objekt* = *Auflistung*. Item (Index)</span><span class="sxs-lookup"><span data-stu-id="bae79-106">Set*object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="bae79-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bae79-107">Return value</span></span>

<span data-ttu-id="bae79-108">Gibt einen Objektverweis zurück.</span><span class="sxs-lookup"><span data-stu-id="bae79-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="bae79-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bae79-109">Parameters</span></span>

|<span data-ttu-id="bae79-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bae79-110">Parameter</span></span>|<span data-ttu-id="bae79-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bae79-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="bae79-112">*Index*</span><span class="sxs-lookup"><span data-stu-id="bae79-112">*Index*</span></span> |<span data-ttu-id="bae79-113">Ein **Variant** -Ausdruck, der als Name oder Ordnungszahl eines Objekts in einer Auflistung ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="bae79-113">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="bae79-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bae79-114">Remarks</span></span>

<span data-ttu-id="bae79-115">Verwenden Sie die **Item** -Eigenschaft, um ein bestimmtes Objekt in einer Auflistung zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="bae79-115">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="bae79-116">Wenn das **Element** ein Objekt in der Auflistung entspricht dem *Index* -Argument nicht finden kann, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="bae79-116">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="bae79-117">Darüber hinaus unterstützen einige Sammlungen nicht benannte Objekte; für diese Auflistungen müssen Sie die Ordnungszahl Verweise verwenden.</span><span class="sxs-lookup"><span data-stu-id="bae79-117">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="bae79-118">Die **Item** -Eigenschaft ist die Standardeigenschaft für alle Auflistungen. Die folgenden Syntaxformen sind deshalb austauschbar:</span><span class="sxs-lookup"><span data-stu-id="bae79-118">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
