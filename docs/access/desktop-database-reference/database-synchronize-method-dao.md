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
ms.openlocfilehash: 19c9935b92e1b7f0b60efb3e00df22133c4d7658
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927305"
---
# <a name="databasesynchronize-method-dao"></a><span data-ttu-id="6c2c6-102">Database.Synchronize-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="6c2c6-102">Database.Synchronize method (DAO)</span></span>


<span data-ttu-id="6c2c6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c2c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c2c6-p101">Synchronisiert zwei Replikate (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="6c2c6-p101">Synchronizes two replicas. (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c2c6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c2c6-106">Syntax</span></span>

<span data-ttu-id="6c2c6-107">*Ausdruck* . Synchronisieren Sie (***DbPathName***, ***ExchangeType***)</span><span class="sxs-lookup"><span data-stu-id="6c2c6-107">*expression* .Synchronize(***DbPathName***, ***ExchangeType***)</span></span>

<span data-ttu-id="6c2c6-108">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6c2c6-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="6c2c6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c2c6-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c2c6-110">Name</span><span class="sxs-lookup"><span data-stu-id="6c2c6-110">Name</span></span></p></th>
<th><p><span data-ttu-id="6c2c6-111">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="6c2c6-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="6c2c6-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6c2c6-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="6c2c6-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c2c6-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c2c6-114">DbPathName</span><span class="sxs-lookup"><span data-stu-id="6c2c6-114">DbPathName</span></span></p></td>
<td><p><span data-ttu-id="6c2c6-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="6c2c6-115">Required</span></span></p></td>
<td><p><span data-ttu-id="6c2c6-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="6c2c6-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6c2c6-117">Der Pfad zum Zielreplikat, mit dem die Datenbank synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6c2c6-117">The path to the target replica with which database will be synchronized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c2c6-118">ExchangeType</span><span class="sxs-lookup"><span data-stu-id="6c2c6-118">ExchangeType</span></span></p></td>
<td><p><span data-ttu-id="6c2c6-119">Optional</span><span class="sxs-lookup"><span data-stu-id="6c2c6-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="6c2c6-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="6c2c6-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6c2c6-121">Eine <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong>-Konstante, die angibt, in welche Richtung Änderungen zwischen den beiden Datenbanken synchronisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c2c6-121">A <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> constant indicating which direction to synchronize changes between the two databases.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6c2c6-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c2c6-122">Remarks</span></span>

<span data-ttu-id="6c2c6-123">Mit **Synchronize** können Sie Daten und Entwurfsänderungen zwischen zwei Datenbanken austauschen.</span><span class="sxs-lookup"><span data-stu-id="6c2c6-123">You use **Synchronize** to exchange data and design changes between two databases.</span></span> <span data-ttu-id="6c2c6-124">Entwurfsänderungen werden grundsätzlich zuerst vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="6c2c6-124">Design changes always happen first.</span></span> <span data-ttu-id="6c2c6-125">Beide Datenbanken müssen sich auf derselben Entwurfsebene befinden, damit Daten ausgetauscht werden können.</span><span class="sxs-lookup"><span data-stu-id="6c2c6-125">Both databases must be at the same design level before they can exchange data.</span></span> <span data-ttu-id="6c2c6-126">Beispielsweise möglicherweise ein Austausch von Typ **DbRepExportChanges** Designänderungen bei einem Replikat, obwohl die Daten in DbPathName Fluss nur aus der Datenbank ändert.</span><span class="sxs-lookup"><span data-stu-id="6c2c6-126">For example, an exchange of type **dbRepExportChanges** might cause design changes at a replica even though data changes flow only from the database to DbPathName.</span></span>

<span data-ttu-id="6c2c6-127">DbPathName angegebene Replikat muss Teil derselben Replikatgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="6c2c6-127">The replica identified in DbPathName must be part of the same replica set.</span></span> <span data-ttu-id="6c2c6-128">Wenn beide Replikate über dieselbe **ReplicaID**-Eigenschafteneinstellung verfügen oder Designmaster für zwei verschiedene Replikatgruppen sind, schlägt die Synchronisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="6c2c6-128">If both replicas have the same **ReplicaID** property setting or are Design Masters for two different replica sets, the synchronization fails.</span></span>

<span data-ttu-id="6c2c6-129">Verwenden Sie die **dbRepSyncInternet**-Konstante, um zwei Replikate über das Internet zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="6c2c6-129">When you synchronize two replicas over the Internet, you must use the **dbRepSyncInternet** constant.</span></span> <span data-ttu-id="6c2c6-130">In diesem Fall geben Sie eine Adresse Uniform Resource Locator (URL) für das Argument DbPathName anstelle von angeben eines Pfads lokales Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="6c2c6-130">In this case, you specify a Uniform Resource Locator (URL) address for the DbPathName argument instead of specifying a local area network path.</span></span>


> [!NOTE]
> <span data-ttu-id="6c2c6-p105">[!HINWEIS] Es ist nicht möglich, Teilreplikate mit anderen Teilreplikaten zu synchronisieren. Weitere Informationen erhalten Sie im Thema zur [PopulatePartial](database-populatepartial-method-dao.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6c2c6-p105">You can't synchronize partial replicas with other partial replicas. See the [PopulatePartial](database-populatepartial-method-dao.md) method for more information.</span></span>


