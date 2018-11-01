---
title: Item-Eigenschaft (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 73e6240b92a34a6ff1d215cd3211a844f10fe766
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868309"
---
# <a name="item-property-ado"></a><span data-ttu-id="768a1-102">Item-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="768a1-102">Item property (ADO)</span></span>

<span data-ttu-id="768a1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="768a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="768a1-104">Gibt ein bestimmtes Element einer Auflistung nach Name oder Ordnungszahl an.</span><span class="sxs-lookup"><span data-stu-id="768a1-104">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="768a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="768a1-105">Syntax</span></span>

<span data-ttu-id="768a1-106">Legen Sie*Objekt* = *Auflistung*. Item (Index)</span><span class="sxs-lookup"><span data-stu-id="768a1-106">Set*object* = *collection*.Item ( Index )</span></span>

## <a name="return-value"></a><span data-ttu-id="768a1-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="768a1-107">Return value</span></span>

<span data-ttu-id="768a1-108">Gibt einen Objektverweis zurück.</span><span class="sxs-lookup"><span data-stu-id="768a1-108">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="768a1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="768a1-109">Parameters</span></span>

- <span data-ttu-id="768a1-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="768a1-110">*Index*</span></span>

- <span data-ttu-id="768a1-111">Ein **Variant** -Ausdruck, der als Name oder Ordnungszahl eines Objekts in einer Auflistung ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="768a1-111">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="768a1-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="768a1-112">Remarks</span></span>

<span data-ttu-id="768a1-113">Verwenden Sie die **Item** -Eigenschaft, um ein bestimmtes Objekt in einer Auflistung zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="768a1-113">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="768a1-114">Wenn das **Element** ein Objekt in der Auflistung entspricht dem *Index* -Argument nicht finden kann, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="768a1-114">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="768a1-115">Darüber hinaus unterstützen einige Sammlungen nicht benannte Objekte; für diese Auflistungen müssen Sie die Ordnungszahl Verweise verwenden.</span><span class="sxs-lookup"><span data-stu-id="768a1-115">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="768a1-116">Die **Item** -Eigenschaft ist die Standardeigenschaft für alle Auflistungen. Die folgenden Syntaxformen sind deshalb austauschbar:</span><span class="sxs-lookup"><span data-stu-id="768a1-116">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
