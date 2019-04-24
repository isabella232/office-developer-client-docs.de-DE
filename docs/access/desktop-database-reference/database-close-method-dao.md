---
title: Database. Schließ-Methode (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 190b47b59bd9781553912f91156c74a3fd09c2d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295023"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="ccc5b-102">Database. Schließ-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="ccc5b-102">Database.Close method (DAO)</span></span>


<span data-ttu-id="ccc5b-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ccc5b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ccc5b-104">Schließt ein geöffnetes **Database**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ccc5b-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccc5b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccc5b-105">Syntax</span></span>

<span data-ttu-id="ccc5b-106">*Ausdruck* . Schließen</span><span class="sxs-lookup"><span data-stu-id="ccc5b-106">*expression* .Close</span></span>

<span data-ttu-id="ccc5b-107">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="ccc5b-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccc5b-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ccc5b-108">Remarks</span></span>

<span data-ttu-id="ccc5b-109">Ist das **Database**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="ccc5b-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="ccc5b-110">Eine Alternative zur **Schließ** -Methode besteht darin, den Wert einer Objektvariable auf **Nothing** festzulegen (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="ccc5b-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

