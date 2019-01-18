---
title: Append-Methode (ADOX Indexes)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0b541512de9748e94d033bb56f27dd0941c7f5a7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707556"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="c9dad-102">Append-Methode (ADOX Indexes)</span><span class="sxs-lookup"><span data-stu-id="c9dad-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="c9dad-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9dad-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="c9dad-104">Fügt der [Indexes](index-object-adox.md)-Auflistung ein neues [Index](indexes-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9dad-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9dad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9dad-105">Syntax</span></span>

<span data-ttu-id="c9dad-106">*Indizes*. Fügen Sie*Index* \[,*Spalten*\]</span><span class="sxs-lookup"><span data-stu-id="c9dad-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="c9dad-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9dad-107">Parameters</span></span>

|<span data-ttu-id="c9dad-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9dad-108">Parameter</span></span>|<span data-ttu-id="c9dad-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9dad-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c9dad-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="c9dad-110">*Index*</span></span> |<span data-ttu-id="c9dad-111">Das anzufügende **Index** -Objekt oder der Name des zu erstellenden und anzufügenden Indexes.</span><span class="sxs-lookup"><span data-stu-id="c9dad-111">The **Index** object to append or the name of the index to create and append.</span></span>|
|<span data-ttu-id="c9dad-112">*Columns*</span><span class="sxs-lookup"><span data-stu-id="c9dad-112">*Columns*</span></span> |<span data-ttu-id="c9dad-113">Optional.</span><span class="sxs-lookup"><span data-stu-id="c9dad-113">Optional.</span></span> <span data-ttu-id="c9dad-114">Ein **Variant** -Wert, der die Namen der zu indizierenden Spalte(n) angibt.</span><span class="sxs-lookup"><span data-stu-id="c9dad-114">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="c9dad-115">Die Werte der [Name](name-property-adox.md) -Eigenschaft des ein [Column](column-object-adox.md) -Objekt oder Objekte entspricht der *Columns* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="c9dad-115">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c9dad-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9dad-116">Remarks</span></span>

<span data-ttu-id="c9dad-117">Der *Columns* -Parameter kann entweder den Namen einer Spalte oder ein Array von Spaltennamen dauern.</span><span class="sxs-lookup"><span data-stu-id="c9dad-117">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="c9dad-118">Wenn der Anbieter das Erstellen von Indizes nicht unterstützt, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="c9dad-118">An error will occur if the provider does not support creating indexes.</span></span>

