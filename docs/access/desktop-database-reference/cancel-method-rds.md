---
title: Cancel-Methode (RDS)
TOCTitle: Cancel Method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8455496e8d426d26f56b902d9a089d236bde1a6a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868746"
---
# <a name="cancel-method-rds"></a><span data-ttu-id="978a3-102">Cancel-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="978a3-102">Cancel Method (RDS)</span></span>


<span data-ttu-id="978a3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="978a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="978a3-104">Bricht die Ausführung eines ausstehenden asynchronen Methodenaufrufs ab.</span><span class="sxs-lookup"><span data-stu-id="978a3-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="978a3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="978a3-105">Syntax</span></span>

<span data-ttu-id="978a3-106">*RDS*.</span><span class="sxs-lookup"><span data-stu-id="978a3-106">*RDS*.</span></span> <span data-ttu-id="978a3-107">*DataControl*. Abbrechen</span><span class="sxs-lookup"><span data-stu-id="978a3-107">*DataControl*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="978a3-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="978a3-108">Remarks</span></span>

<span data-ttu-id="978a3-109">Wenn Sie **Cancel** aufrufen, wird [ReadyState](readystate-property-rds.md) automatisch auf **adcReadyStateLoaded** festgelegt, und das [Recordset](recordset-object-ado.md)-Objekt ist leer.</span><span class="sxs-lookup"><span data-stu-id="978a3-109">When you call **Cancel**, [ReadyState](readystate-property-rds.md) is automatically set to **adcReadyStateLoaded**, and the [Recordset](recordset-object-ado.md) will be empty.</span></span>

