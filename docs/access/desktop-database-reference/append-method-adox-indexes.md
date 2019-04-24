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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297095"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="db0d4-102">Append-Methode (ADOX Indexes)</span><span class="sxs-lookup"><span data-stu-id="db0d4-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="db0d4-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="db0d4-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="db0d4-104">Fügt der [Indexes](index-object-adox.md)-Auflistung ein neues [Index](indexes-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="db0d4-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="db0d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="db0d4-105">Syntax</span></span>

<span data-ttu-id="db0d4-106">*Indizes*. Anfügen von*Index* \[,*Spalten*\]</span><span class="sxs-lookup"><span data-stu-id="db0d4-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="db0d4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="db0d4-107">Parameters</span></span>

|<span data-ttu-id="db0d4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="db0d4-108">Parameter</span></span>|<span data-ttu-id="db0d4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db0d4-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="db0d4-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="db0d4-110">*Index*</span></span> |<span data-ttu-id="db0d4-111">Das anzufügende **Index** -Objekt oder der Name des zu erstellenden und anzufügenden Indexes.</span><span class="sxs-lookup"><span data-stu-id="db0d4-111">The **Index** object to append or the name of the index to create and append.</span></span>|
|<span data-ttu-id="db0d4-112">*Columns*</span><span class="sxs-lookup"><span data-stu-id="db0d4-112">*Columns*</span></span> |<span data-ttu-id="db0d4-p101">Optional. Ein **Variant**-Wert, der den bzw. die Namen der zu indizierenden Spalte(n) angibt. Der *Columns*-Parameter entspricht dem Wert bzw. den Werten der [Name](name-property-adox.md)-Eigenschaft eines bzw. mehrerer [Column](column-object-adox.md)-Objekte.</span><span class="sxs-lookup"><span data-stu-id="db0d4-p101">Optional. A **Variant** value that specifies the name(s) of the column(s) to be indexed. The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>|

## <a name="remarks"></a><span data-ttu-id="db0d4-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db0d4-116">Remarks</span></span>

<span data-ttu-id="db0d4-117">Der *Columns*-Parameter kann entweder den Namen einer Spalte oder einen Array von Spaltennamen festlegen.</span><span class="sxs-lookup"><span data-stu-id="db0d4-117">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="db0d4-118">Wenn der Anbieter das Erstellen von Indizes nicht unterstützt, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="db0d4-118">An error will occur if the provider does not support creating indexes.</span></span>

