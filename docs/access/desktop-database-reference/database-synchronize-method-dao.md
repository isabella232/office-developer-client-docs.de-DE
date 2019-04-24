---
title: Database. Synchronize-Methode (DAO)
TOCTitle: Synchronize Method
ms:assetid: 5e716a4a-2430-8106-5c34-a02dd28bc4f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194659(v=office.15)
ms:contentKeyID: 48545137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053357
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 411948f3c0ac4d6c353cd2722136dffb6a25fb17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294708"
---
# <a name="databasesynchronize-method-dao"></a><span data-ttu-id="a9c84-102">Database. Synchronize-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="a9c84-102">Database.Synchronize method (DAO)</span></span>


<span data-ttu-id="a9c84-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9c84-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9c84-p101">Synchronisiert zwei Replikate (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="a9c84-p101">Synchronizes two replicas. (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9c84-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9c84-106">Syntax</span></span>

<span data-ttu-id="a9c84-107">*Ausdruck* . Synchronize (\*\*\*\*\*\* DbPathName, ***Exchanger***)</span><span class="sxs-lookup"><span data-stu-id="a9c84-107">*expression* .Synchronize(***DbPathName***, ***ExchangeType***)</span></span>

<span data-ttu-id="a9c84-108">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="a9c84-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="a9c84-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9c84-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9c84-110">Name</span><span class="sxs-lookup"><span data-stu-id="a9c84-110">Name</span></span></p></th>
<th><p><span data-ttu-id="a9c84-111">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="a9c84-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="a9c84-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a9c84-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="a9c84-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9c84-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9c84-114"><em>DbPathname</em></span><span class="sxs-lookup"><span data-stu-id="a9c84-114"><em>DbPathName</em></span></span></p></td>
<td><p><span data-ttu-id="a9c84-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a9c84-115">Required</span></span></p></td>
<td><p><span data-ttu-id="a9c84-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="a9c84-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="a9c84-117">Der Pfad zum Zielreplikat, mit dem die Datenbank synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a9c84-117">The path to the target replica with which database will be synchronized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9c84-118"><em>ExchangeType</em></span><span class="sxs-lookup"><span data-stu-id="a9c84-118"><em>ExchangeType</em></span></span></p></td>
<td><p><span data-ttu-id="a9c84-119">Optional</span><span class="sxs-lookup"><span data-stu-id="a9c84-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="a9c84-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a9c84-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a9c84-121">Eine <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> -Konstante, die angibt, in welche Richtung Änderungen zwischen den beiden Datenbanken synchronisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9c84-121">A <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> constant indicating which direction to synchronize changes between the two databases.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a9c84-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9c84-122">Remarks</span></span>

<span data-ttu-id="a9c84-123">Mit **Synchronize** können Sie Daten und Entwurfsänderungen zwischen zwei Datenbanken austauschen.</span><span class="sxs-lookup"><span data-stu-id="a9c84-123">You use **Synchronize** to exchange data and design changes between two databases.</span></span> <span data-ttu-id="a9c84-124">Entwurfsänderungen werden grundsätzlich zuerst vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="a9c84-124">Design changes always happen first.</span></span> <span data-ttu-id="a9c84-125">Beide Datenbanken müssen sich auf derselben Entwurfsebene befinden, damit Daten ausgetauscht werden können.</span><span class="sxs-lookup"><span data-stu-id="a9c84-125">Both databases must be at the same design level before they can exchange data.</span></span> <span data-ttu-id="a9c84-126">Ein Exchange vom Typ **dbRepExportChanges** kann beispielsweise Entwurfsänderungen an einem Replikat verursachen, obwohl Datenänderungen nur von der Datenbank zu DbPathName fließen.</span><span class="sxs-lookup"><span data-stu-id="a9c84-126">For example, an exchange of type **dbRepExportChanges** might cause design changes at a replica even though data changes flow only from the database to DbPathName.</span></span>

<span data-ttu-id="a9c84-127">Das in dbPathname angegebene Replikat muss Teil derselben Replikatgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="a9c84-127">The replica identified in DbPathName must be part of the same replica set.</span></span> <span data-ttu-id="a9c84-128">Wenn beide Replikate über dieselbe **ReplicaID**-Eigenschafteneinstellung verfügen oder Designmaster für zwei verschiedene Replikatgruppen sind, schlägt die Synchronisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="a9c84-128">If both replicas have the same **ReplicaID** property setting or are Design Masters for two different replica sets, the synchronization fails.</span></span>

<span data-ttu-id="a9c84-129">Verwenden Sie die **dbRepSyncInternet**-Konstante, um zwei Replikate über das Internet zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="a9c84-129">When you synchronize two replicas over the Internet, you must use the **dbRepSyncInternet** constant.</span></span> <span data-ttu-id="a9c84-130">In diesem Fall geben Sie eine URL-Adresse (Uniform Resource Locator) für das Argument dbPathname an, anstatt einen lokalen Netzwerkpfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a9c84-130">In this case, you specify a Uniform Resource Locator (URL) address for the DbPathName argument instead of specifying a local area network path.</span></span>


> [!NOTE]
> <span data-ttu-id="a9c84-131">[!HINWEIS] Es ist nicht möglich, Teilreplikate mit anderen Teilreplikaten zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="a9c84-131">You can't synchronize partial replicas with other partial replicas.</span></span> <span data-ttu-id="a9c84-132">Weitere Informationen erhalten Sie im Thema zur [PopulatePartial](database-populatepartial-method-dao.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a9c84-132">See the [PopulatePartial](database-populatepartial-method-dao.md) method for more information.</span></span>


