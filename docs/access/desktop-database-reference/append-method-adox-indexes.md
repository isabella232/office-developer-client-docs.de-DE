---
title: Append-Methode (ADOX Indexes)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41eb1cc67dd5a2058f9c5673db381f0bc9067454
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921481"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="5bbaf-102">Append-Methode (ADOX Indexes)</span><span class="sxs-lookup"><span data-stu-id="5bbaf-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="5bbaf-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5bbaf-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="5bbaf-104">Fügt der [Indexes](index-object-adox.md)-Auflistung ein neues [Index](indexes-collection-adox.md)-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="5bbaf-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bbaf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bbaf-105">Syntax</span></span>

<span data-ttu-id="5bbaf-106">*Indizes*. Fügen Sie*Index* \[,*Spalten*\]</span><span class="sxs-lookup"><span data-stu-id="5bbaf-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="5bbaf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bbaf-107">Parameters</span></span>

  - <span data-ttu-id="5bbaf-108">*Index*</span><span class="sxs-lookup"><span data-stu-id="5bbaf-108">*Index*</span></span>

  - <span data-ttu-id="5bbaf-109">Das anzufügende **Index** -Objekt oder der Name des zu erstellenden und anzufügenden Indexes.</span><span class="sxs-lookup"><span data-stu-id="5bbaf-109">The **Index** object to append or the name of the index to create and append.</span></span>

  - <span data-ttu-id="5bbaf-110">*Columns*</span><span class="sxs-lookup"><span data-stu-id="5bbaf-110">*Columns*</span></span>

  - <span data-ttu-id="5bbaf-111">Optional.</span><span class="sxs-lookup"><span data-stu-id="5bbaf-111">Optional.</span></span> <span data-ttu-id="5bbaf-112">Ein **Variant** -Wert, der die Namen der zu indizierenden Spalte(n) angibt.</span><span class="sxs-lookup"><span data-stu-id="5bbaf-112">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="5bbaf-113">Die Werte der [Name](name-property-adox.md) -Eigenschaft des ein [Column](column-object-adox.md) -Objekt oder Objekte entspricht der *Columns* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="5bbaf-113">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bbaf-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5bbaf-114">Remarks</span></span>

<span data-ttu-id="5bbaf-115">Der *Columns* -Parameter kann entweder den Namen einer Spalte oder ein Array von Spaltennamen dauern.</span><span class="sxs-lookup"><span data-stu-id="5bbaf-115">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="5bbaf-116">Wenn der Anbieter das Erstellen von Indizes nicht unterstützt, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="5bbaf-116">An error will occur if the provider does not support creating indexes.</span></span>

