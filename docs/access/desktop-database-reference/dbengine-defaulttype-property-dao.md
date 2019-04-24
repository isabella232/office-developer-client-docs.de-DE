---
title: DbEngine. DefaultType-Eigenschaft (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 23f6c87ede6da2cc5b2f3203bfa13cb17bf93e82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294379"
---
# <a name="dbenginedefaulttype-property-dao"></a><span data-ttu-id="da308-102">DbEngine. DefaultType-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="da308-102">DBEngine.DefaultType property (DAO)</span></span>


<span data-ttu-id="da308-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="da308-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="da308-104">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der den beim Erstellen des nächsten **[Workspace](workspace-object-dao.md)** -Objekts verwendeten Typ des Arbeitsbereichs angibt.</span><span class="sxs-lookup"><span data-stu-id="da308-104">Sets or returns a value that indicates what type of workspace will be used by the next **[Workspace](workspace-object-dao.md)** object created.</span></span>

## <a name="syntax"></a><span data-ttu-id="da308-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da308-105">Syntax</span></span>

<span data-ttu-id="da308-106">*Ausdruck* . DefaultType</span><span class="sxs-lookup"><span data-stu-id="da308-106">*expression* .DefaultType</span></span>

<span data-ttu-id="da308-107">*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="da308-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="da308-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da308-108">Remarks</span></span>

<span data-ttu-id="da308-109">Die Einstellung oder der Rückgabewert kann eine der **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** -Konstanten sein.</span><span class="sxs-lookup"><span data-stu-id="da308-109">The setting or return value can be one of the of the **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** constants.</span></span>


> [!NOTE]
> <span data-ttu-id="da308-p101">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="da308-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="da308-112">Die Einstellung kann für einen einzelnen **Arbeitsbereich** außer Kraft gesetzt werden, indem das Argument **[](dbengine-createworkspace-method-dao.md)** Type auf die CreateWorkspace-Methode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="da308-112">The setting can be overridden for a single **Workspace** by setting the type argument to the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method.</span></span>

