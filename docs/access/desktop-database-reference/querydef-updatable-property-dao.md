---
title: QueryDef.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ad761c2941cb556ce67c9f716247663220f753f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873691"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="87acd-102">QueryDef.Updatable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="87acd-102">QueryDef.Updatable Property (DAO)</span></span>


<span data-ttu-id="87acd-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="87acd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="87acd-p101">Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann. Schreibgeschützter **Boolean**-Wert.</span><span class="sxs-lookup"><span data-stu-id="87acd-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="87acd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="87acd-106">Syntax</span></span>

<span data-ttu-id="87acd-107">*Ausdruck* . Aktualisierbar</span><span class="sxs-lookup"><span data-stu-id="87acd-107">*expression* .Updatable</span></span>

<span data-ttu-id="87acd-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="87acd-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="87acd-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87acd-109">Remarks</span></span>

<span data-ttu-id="87acd-110">Die **Updatable**-Eigenschaft eines **QueryDef**-Objekts wird auf **True** gesetzt, wenn die Abfragedefinition aktualisiert werden kann, selbst wenn das sich ergebende **[Recordset](recordset-object-dao.md)** -Objekt nicht aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="87acd-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

