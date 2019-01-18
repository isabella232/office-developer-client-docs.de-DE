---
title: Workspace.Close-Methode (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0049fb335c869a050a2c20d5740c487413c76786
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708627"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="6b859-102">Workspace.Close-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="6b859-102">Workspace.Close method (DAO)</span></span>


<span data-ttu-id="6b859-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b859-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6b859-104">Schließt ein geöffnetes **Workspace**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6b859-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b859-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b859-105">Syntax</span></span>

<span data-ttu-id="6b859-106">*Ausdruck* . Schließen Sie</span><span class="sxs-lookup"><span data-stu-id="6b859-106">*expression* .Close</span></span>

<span data-ttu-id="6b859-107">*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6b859-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b859-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b859-108">Remarks</span></span>

<span data-ttu-id="6b859-109">Ist das **Workspace**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="6b859-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="6b859-110">Eine Alternative für die **Close** -Methode den Wert einer Objektvariable auf **Nothing** festgelegt ist (Set DbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="6b859-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

