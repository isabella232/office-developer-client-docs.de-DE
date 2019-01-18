---
title: QueryDef.CacheSize-Eigenschaft (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d826781bd668cff0a61c655e55834512a289c17
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701709"
---
# <a name="querydefcachesize-property-dao"></a><span data-ttu-id="adf70-102">QueryDef.CacheSize-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="adf70-102">QueryDef.CacheSize property (DAO)</span></span>


<span data-ttu-id="adf70-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="adf70-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="adf70-p101">Legt die Anzahl der von einer ODBC-Datenquelle abgefragten Datensätze fest, die lokal zwischengespeichert werden, oder gibt den betreffenden Wert zurück. **Long**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="adf70-p101">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="adf70-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="adf70-106">Syntax</span></span>

<span data-ttu-id="adf70-107">*Ausdruck* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="adf70-107">*expression* .CacheSize</span></span>

<span data-ttu-id="adf70-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="adf70-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="adf70-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="adf70-109">Remarks</span></span>

<span data-ttu-id="adf70-p102">Der Wert der **CacheSize**-Eigenschaft muss zwischen 5 und 1200 liegen, darf aber nicht größer als der verfügbare Speicherplatz sein. Ein typischer Wert ist 100. Bei der Einstellung 0 wird die Zwischenspeicherung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="adf70-p102">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow. A typical value is 100. A setting of 0 turns off caching.</span></span>

<span data-ttu-id="adf70-113">Das Microsoft Access-Datenbankmodul fordert Datensätze innerhalb des Cachebereichs aus dem Cache an, und es fordert Datensätze außerhalb des Cachebereichs vom Server an.</span><span class="sxs-lookup"><span data-stu-id="adf70-113">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="adf70-114">Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="adf70-114">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

