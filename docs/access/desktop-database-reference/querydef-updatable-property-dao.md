---
title: QueryDef. aktualisierbare Eigenschaft (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5321e834f1dd5ed663033cacb530962d7beeb5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303332"
---
# <a name="querydefupdatable-property-dao"></a><span data-ttu-id="1f899-102">QueryDef. aktualisierbare Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="1f899-102">QueryDef.Updatable property (DAO)</span></span>


<span data-ttu-id="1f899-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f899-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f899-104">Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1f899-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="1f899-105">Schreibgeschützter **Boolean**-Wert.</span><span class="sxs-lookup"><span data-stu-id="1f899-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f899-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f899-106">Syntax</span></span>

<span data-ttu-id="1f899-107">*Ausdruck* . Aktualisierbar</span><span class="sxs-lookup"><span data-stu-id="1f899-107">*expression* .Updatable</span></span>

<span data-ttu-id="1f899-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1f899-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f899-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f899-109">Remarks</span></span>

<span data-ttu-id="1f899-110">Die **Updatable**-Eigenschaft eines **QueryDef**-Objekts wird auf **True** gesetzt, wenn die Abfragedefinition aktualisiert werden kann, selbst wenn das sich ergebende **[Recordset](recordset-object-dao.md)** -Objekt nicht aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1f899-110">The **Updatable** property of a **QueryDef** object is set to **True** if the query definition can be updated, even if the resulting **[Recordset](recordset-object-dao.md)** object isn't updatable.</span></span>

