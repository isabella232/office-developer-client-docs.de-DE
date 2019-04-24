---
title: QueryDef. CacheSize-Eigenschaft (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d826781bd668cff0a61c655e55834512a289c17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301092"
---
# <a name="querydefcachesize-property-dao"></a><span data-ttu-id="504c1-102">QueryDef. CacheSize-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="504c1-102">QueryDef.CacheSize property (DAO)</span></span>


<span data-ttu-id="504c1-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="504c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="504c1-104">Mit dieser Eigenschaft wird die Anzahl von Datensätzen, die aus einer ODBC-Datenquelle abgerufen und lokal gespeichert werden, festgelegt oder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="504c1-104">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="504c1-105">**Long**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="504c1-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="504c1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="504c1-106">Syntax</span></span>

<span data-ttu-id="504c1-107">*Ausdruck* . CacheSize</span><span class="sxs-lookup"><span data-stu-id="504c1-107">*expression* .CacheSize</span></span>

<span data-ttu-id="504c1-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="504c1-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="504c1-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="504c1-109">Remarks</span></span>

<span data-ttu-id="504c1-p102">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow. A typical value is 100. A setting of 0 turns off caching.</span><span class="sxs-lookup"><span data-stu-id="504c1-p102">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow. A typical value is 100. A setting of 0 turns off caching.</span></span>

<span data-ttu-id="504c1-113">Das Microsoft Access-Datenbankmodul fordert Datensätze innerhalb des Cachebereichs aus dem Cache an, und es fordert Datensätze außerhalb des Cachebereichs vom Server an.</span><span class="sxs-lookup"><span data-stu-id="504c1-113">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="504c1-114">Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="504c1-114">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

