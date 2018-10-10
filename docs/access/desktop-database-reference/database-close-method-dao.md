---
title: Database.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 97246da6224ee04fa435638a0cb11d1bdac8859f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473364"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="ad337-102">Database.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="ad337-102">Database.Close Method (DAO)</span></span>


<span data-ttu-id="ad337-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad337-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ad337-104">Schließt ein geöffnetes **Database**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ad337-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad337-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad337-105">Syntax</span></span>

<span data-ttu-id="ad337-106">*Ausdruck* . Schließen Sie</span><span class="sxs-lookup"><span data-stu-id="ad337-106">*expression* .Close</span></span>

<span data-ttu-id="ad337-107">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="ad337-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad337-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad337-108">Remarks</span></span>

<span data-ttu-id="ad337-109">Ist das **Database**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="ad337-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="ad337-110">Eine Alternative für die **Close** -Methode den Wert einer Objektvariable auf **Nothing** festgelegt ist (Set DbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="ad337-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

