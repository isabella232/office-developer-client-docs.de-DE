---
title: QueryDef.CacheSize Property (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1ecddf9a9972c6ded5e28748822169c2c60edc44
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472820"
---
# <a name="querydefcachesize-property-dao"></a><span data-ttu-id="1b6cf-102">QueryDef.CacheSize Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="1b6cf-102">QueryDef.CacheSize Property (DAO)</span></span>


<span data-ttu-id="1b6cf-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b6cf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1b6cf-p101">Legt die Anzahl der von einer ODBC-Datenquelle abgefragten Datensätze fest, die lokal zwischengespeichert werden, oder gibt den betreffenden Wert zurück. **Long**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1b6cf-p101">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b6cf-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b6cf-106">Syntax</span></span>

<span data-ttu-id="1b6cf-107">*Ausdruck* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="1b6cf-107">*expression* .CacheSize</span></span>

<span data-ttu-id="1b6cf-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1b6cf-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b6cf-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b6cf-109">Remarks</span></span>

<span data-ttu-id="1b6cf-p102">Der Wert der **CacheSize**-Eigenschaft muss zwischen 5 und 1200 liegen, darf aber nicht größer als der verfügbare Speicherplatz sein. Ein typischer Wert ist 100. Bei der Einstellung 0 wird die Zwischenspeicherung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1b6cf-p102">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow. A typical value is 100. A setting of 0 turns off caching.</span></span>

<span data-ttu-id="1b6cf-113">Das Microsoft Access-Datenbankmodul fordert Datensätze innerhalb des Cachebereichs aus dem Cache an, und es fordert Datensätze außerhalb des Cachebereichs vom Server an.</span><span class="sxs-lookup"><span data-stu-id="1b6cf-113">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="1b6cf-114">Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="1b6cf-114">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

