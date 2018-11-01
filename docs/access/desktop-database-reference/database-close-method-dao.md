---
title: Database.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92b4075f09bb34eca465f49d30a9ba8777b3e583
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869652"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="132ea-102">Database.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="132ea-102">Database.Close Method (DAO)</span></span>


<span data-ttu-id="132ea-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="132ea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="132ea-104">Schließt ein geöffnetes **Database**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="132ea-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="132ea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="132ea-105">Syntax</span></span>

<span data-ttu-id="132ea-106">*Ausdruck* . Schließen Sie</span><span class="sxs-lookup"><span data-stu-id="132ea-106">*expression* .Close</span></span>

<span data-ttu-id="132ea-107">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="132ea-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="132ea-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="132ea-108">Remarks</span></span>

<span data-ttu-id="132ea-109">Ist das **Database**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="132ea-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="132ea-110">Eine Alternative für die **Close** -Methode den Wert einer Objektvariable auf **Nothing** festgelegt ist (Set DbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="132ea-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

