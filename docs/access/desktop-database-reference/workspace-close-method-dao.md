---
title: Workspace. Schließ-Methode (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0049fb335c869a050a2c20d5740c487413c76786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305957"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="c0927-102">Workspace. Schließ-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="c0927-102">Workspace.Close method (DAO)</span></span>


<span data-ttu-id="c0927-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0927-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c0927-104">Schließt ein geöffnetes **Workspace**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c0927-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0927-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0927-105">Syntax</span></span>

<span data-ttu-id="c0927-106">*Ausdruck* . Schließen</span><span class="sxs-lookup"><span data-stu-id="c0927-106">*expression* .Close</span></span>

<span data-ttu-id="c0927-107">*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c0927-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0927-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0927-108">Remarks</span></span>

<span data-ttu-id="c0927-109">Ist das **Workspace**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="c0927-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="c0927-110">Eine Alternative zur **Schließ** -Methode besteht darin, den Wert einer Objektvariable auf **Nothing** festzulegen (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="c0927-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

