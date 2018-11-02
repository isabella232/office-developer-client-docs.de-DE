---
title: Workspace.Close-Methode (DAO)
TOCTitle: Close Method
ms:assetid: 9b3d28f9-5cde-0dd9-8a4a-d2efaec5fe5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198027(v=office.15)
ms:contentKeyID: 48546565
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63b935fa178eb4c55ce11724ec3fd5f62d056779
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919850"
---
# <a name="workspaceclose-method-dao"></a><span data-ttu-id="0751b-102">Workspace.Close-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="0751b-102">Workspace.Close method (DAO)</span></span>


<span data-ttu-id="0751b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0751b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0751b-104">Schließt ein geöffnetes **Workspace**-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0751b-104">Closes an open **Workspace**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0751b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0751b-105">Syntax</span></span>

<span data-ttu-id="0751b-106">*Ausdruck* . Schließen Sie</span><span class="sxs-lookup"><span data-stu-id="0751b-106">*expression* .Close</span></span>

<span data-ttu-id="0751b-107">*Ausdruck* Eine Variable, die ein **Workspace** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="0751b-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0751b-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0751b-108">Remarks</span></span>

<span data-ttu-id="0751b-109">Ist das **Workspace**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="0751b-109">If the **Workspace** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="0751b-110">Eine Alternative für die **Close** -Methode den Wert einer Objektvariable auf **Nothing** festgelegt ist (Set DbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="0751b-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

