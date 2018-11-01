---
title: DBEngine.DefaultType Property (DAO)
TOCTitle: DefaultType Property
ms:assetid: b4371f3e-1ce0-1d0f-93a8-0c5329b510ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822060(v=office.15)
ms:contentKeyID: 48547217
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053580
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f0fa2fb5ba12b1537994a4d6df88406db38bfec4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870926"
---
# <a name="dbenginedefaulttype-property-dao"></a><span data-ttu-id="96fa4-102">DBEngine.DefaultType Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="96fa4-102">DBEngine.DefaultType Property (DAO)</span></span>


<span data-ttu-id="96fa4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="96fa4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="96fa4-104">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der den beim Erstellen des nächsten **[Workspace](workspace-object-dao.md)** -Objekts verwendeten Typ des Arbeitsbereichs angibt.</span><span class="sxs-lookup"><span data-stu-id="96fa4-104">Sets or returns a value that indicates what type of workspace will be used by the next **[Workspace](workspace-object-dao.md)** object created.</span></span>

## <a name="syntax"></a><span data-ttu-id="96fa4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="96fa4-105">Syntax</span></span>

<span data-ttu-id="96fa4-106">*Ausdruck* . DefaultType</span><span class="sxs-lookup"><span data-stu-id="96fa4-106">*expression* .DefaultType</span></span>

<span data-ttu-id="96fa4-107">*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="96fa4-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="96fa4-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96fa4-108">Remarks</span></span>

<span data-ttu-id="96fa4-109">Die Einstellung oder der Rückgabewert kann eine der **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** -Konstanten sein.</span><span class="sxs-lookup"><span data-stu-id="96fa4-109">The setting or return value can be one of the of the **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** constants.</span></span>


> [!NOTE]
> <span data-ttu-id="96fa4-p101">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="96fa4-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="96fa4-112">Die Einstellung kann für ein einzelnes **Workspace** überschrieben werden, indem das Argument Type auf die **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** -Methode.</span><span class="sxs-lookup"><span data-stu-id="96fa4-112">The setting can be overridden for a single **Workspace** by setting the type argument to the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method.</span></span>

