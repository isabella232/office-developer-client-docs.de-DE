---
title: Workspace.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 87f72a58cd3e24838416ef4d19ec1a2cf91e7c1f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473235"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="7c604-102">Workspace.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="7c604-102">Workspace.Close Method (DAO)</span></span>


<span data-ttu-id="7c604-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c604-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7c604-104">Schließt ein geöffnetes **Workspace**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7c604-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c604-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c604-105">Syntax</span></span>

<span data-ttu-id="7c604-106">*Ausdruck* . Schließen Sie</span><span class="sxs-lookup"><span data-stu-id="7c604-106">*expression* .Close</span></span>

<span data-ttu-id="7c604-107">*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="7c604-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c604-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c604-108">Remarks</span></span>

<span data-ttu-id="7c604-109">Ist das **Workspace**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="7c604-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="7c604-110">Eine Alternative für die **Close** -Methode den Wert einer Objektvariable auf **Nothing** festgelegt ist (Set DbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="7c604-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

