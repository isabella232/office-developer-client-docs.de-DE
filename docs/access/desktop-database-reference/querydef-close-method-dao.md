---
title: QueryDef.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: b2b63462-453d-9e2b-0bb3-69a4a7a6ecef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822031(v=office.15)
ms:contentKeyID: 48547179
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052976
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e17936286a4bd661d0a210c905cf0b63b70cf936
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474482"
---
# <a name="querydefclose-method-dao"></a><span data-ttu-id="00567-102">QueryDef.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="00567-102">QueryDef.Close Method (DAO)</span></span>


<span data-ttu-id="00567-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="00567-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="00567-104">Schließt ein geöffnetes **QueryDef**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="00567-104">Closes an open **QueryDef**.</span></span>

## <a name="syntax"></a><span data-ttu-id="00567-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="00567-105">Syntax</span></span>

<span data-ttu-id="00567-106">*Ausdruck* . Schließen Sie</span><span class="sxs-lookup"><span data-stu-id="00567-106">*expression* .Close</span></span>

<span data-ttu-id="00567-107">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="00567-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="00567-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00567-108">Remarks</span></span>

<span data-ttu-id="00567-109">Ist das **QueryDef**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="00567-109">If the **QueryDef** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="00567-110">Eine Alternative für die **Close** -Methode den Wert einer Objektvariable auf **Nothing** festgelegt ist (Set DbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="00567-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

