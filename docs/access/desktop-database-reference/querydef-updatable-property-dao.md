---
title: QueryDef.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ca30e86bd61bc5459a552423bd451c7b158996d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472919"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="6ff50-102">QueryDef.Updatable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="6ff50-102">QueryDef.Updatable Property (DAO)</span></span>


<span data-ttu-id="6ff50-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ff50-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6ff50-p101">Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann. Schreibgeschützter **Boolean**-Wert.</span><span class="sxs-lookup"><span data-stu-id="6ff50-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ff50-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ff50-106">Syntax</span></span>

<span data-ttu-id="6ff50-107">*Ausdruck* . Aktualisierbar</span><span class="sxs-lookup"><span data-stu-id="6ff50-107">*expression* .Updatable</span></span>

<span data-ttu-id="6ff50-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6ff50-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ff50-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ff50-109">Remarks</span></span>

<span data-ttu-id="6ff50-110">Die **Updatable**-Eigenschaft eines **QueryDef**-Objekts wird auf **True** gesetzt, wenn die Abfragedefinition aktualisiert werden kann, selbst wenn das sich ergebende **[Recordset](recordset-object-dao.md)** -Objekt nicht aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6ff50-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

