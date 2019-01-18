---
title: Database.Close-Methode (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 190b47b59bd9781553912f91156c74a3fd09c2d5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699975"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="4ae6e-102">Database.Close-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="4ae6e-102">Database.Close method (DAO)</span></span>


<span data-ttu-id="4ae6e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ae6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4ae6e-104">Schließt ein geöffnetes **Database**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4ae6e-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ae6e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ae6e-105">Syntax</span></span>

<span data-ttu-id="4ae6e-106">*Ausdruck* . Schließen Sie</span><span class="sxs-lookup"><span data-stu-id="4ae6e-106">*expression* .Close</span></span>

<span data-ttu-id="4ae6e-107">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4ae6e-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ae6e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ae6e-108">Remarks</span></span>

<span data-ttu-id="4ae6e-109">Ist das **Database**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="4ae6e-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="4ae6e-110">Eine Alternative für die **Close** -Methode den Wert einer Objektvariable auf **Nothing** festgelegt ist (Set DbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="4ae6e-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

