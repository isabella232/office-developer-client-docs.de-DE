---
title: Database.Synchronize-Methode (DAO)
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
ms.openlocfilehash: 65611960044ea62e42be1ea9d6c6a54d5d42d5a8
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949768"
---
# <a name="databasesynchronize-method-dao"></a><span data-ttu-id="0ce47-102">Database.Synchronize-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="0ce47-102">Database.Synchronize method (DAO)</span></span>


<span data-ttu-id="0ce47-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ce47-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0ce47-p101">Synchronisiert zwei Replikate (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="0ce47-p101">Synchronizes two replicas. (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ce47-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ce47-106">Syntax</span></span>

<span data-ttu-id="0ce47-107">*Ausdruck* . Synchronisieren Sie (***DbPathName***, ***ExchangeType***)</span><span class="sxs-lookup"><span data-stu-id="0ce47-107">*expression* .Synchronize(***DbPathName***, ***ExchangeType***)</span></span>

<span data-ttu-id="0ce47-108">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="0ce47-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ce47-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ce47-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ce47-110">Name</span><span class="sxs-lookup"><span data-stu-id="0ce47-110">Name</span></span></p></th>
<th><p><span data-ttu-id="0ce47-111">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="0ce47-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="0ce47-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0ce47-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="0ce47-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ce47-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ce47-114"><em>DbPathName</em></span><span class="sxs-lookup"><span data-stu-id="0ce47-114"><em>DbPathName</em></span></span></p></td>
<td><p><span data-ttu-id="0ce47-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0ce47-115">Required</span></span></p></td>
<td><p><span data-ttu-id="0ce47-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="0ce47-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="0ce47-117">Der Pfad zum Zielreplikat, mit dem die Datenbank synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="0ce47-117">The path to the target replica with which database will be synchronized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ce47-118"><em>ExchangeType</em></span><span class="sxs-lookup"><span data-stu-id="0ce47-118"><em>ExchangeType</em></span></span></p></td>
<td><p><span data-ttu-id="0ce47-119">Optional</span><span class="sxs-lookup"><span data-stu-id="0ce47-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="0ce47-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0ce47-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0ce47-121">Eine <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong>-Konstante, die angibt, in welche Richtung Änderungen zwischen den beiden Datenbanken synchronisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0ce47-121">A <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> constant indicating which direction to synchronize changes between the two databases.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0ce47-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ce47-122">Remarks</span></span>

<span data-ttu-id="0ce47-123">Mit **Synchronize** können Sie Daten und Entwurfsänderungen zwischen zwei Datenbanken austauschen.</span><span class="sxs-lookup"><span data-stu-id="0ce47-123">You use **Synchronize** to exchange data and design changes between two databases.</span></span> <span data-ttu-id="0ce47-124">Entwurfsänderungen werden grundsätzlich zuerst vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="0ce47-124">Design changes always happen first.</span></span> <span data-ttu-id="0ce47-125">Beide Datenbanken müssen sich auf derselben Entwurfsebene befinden, damit Daten ausgetauscht werden können.</span><span class="sxs-lookup"><span data-stu-id="0ce47-125">Both databases must be at the same design level before they can exchange data.</span></span> <span data-ttu-id="0ce47-126">Beispielsweise möglicherweise ein Austausch von Typ **DbRepExportChanges** Designänderungen bei einem Replikat, obwohl die Daten in DbPathName Fluss nur aus der Datenbank ändert.</span><span class="sxs-lookup"><span data-stu-id="0ce47-126">For example, an exchange of type **dbRepExportChanges** might cause design changes at a replica even though data changes flow only from the database to DbPathName.</span></span>

<span data-ttu-id="0ce47-127">DbPathName angegebene Replikat muss Teil derselben Replikatgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="0ce47-127">The replica identified in DbPathName must be part of the same replica set.</span></span> <span data-ttu-id="0ce47-128">Wenn beide Replikate über dieselbe **ReplicaID**-Eigenschafteneinstellung verfügen oder Designmaster für zwei verschiedene Replikatgruppen sind, schlägt die Synchronisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="0ce47-128">If both replicas have the same **ReplicaID** property setting or are Design Masters for two different replica sets, the synchronization fails.</span></span>

<span data-ttu-id="0ce47-129">Verwenden Sie die **dbRepSyncInternet**-Konstante, um zwei Replikate über das Internet zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="0ce47-129">When you synchronize two replicas over the Internet, you must use the **dbRepSyncInternet** constant.</span></span> <span data-ttu-id="0ce47-130">In diesem Fall geben Sie eine Adresse Uniform Resource Locator (URL) für das Argument DbPathName anstelle von angeben eines Pfads lokales Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0ce47-130">In this case, you specify a Uniform Resource Locator (URL) address for the DbPathName argument instead of specifying a local area network path.</span></span>


> [!NOTE]
> <span data-ttu-id="0ce47-p105">[!HINWEIS] Es ist nicht möglich, Teilreplikate mit anderen Teilreplikaten zu synchronisieren. Weitere Informationen erhalten Sie im Thema zur [PopulatePartial](database-populatepartial-method-dao.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0ce47-p105">You can't synchronize partial replicas with other partial replicas. See the [PopulatePartial](database-populatepartial-method-dao.md) method for more information.</span></span>


