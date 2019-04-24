---
title: XactAttributeEnum (Access Desktop Database Reference)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e79a6143c65637660b2d59b7c7efb6a21e8935bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302569"
---
# <a name="xactattributeenum"></a><span data-ttu-id="64f78-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="64f78-102">XactAttributeEnum</span></span>

<span data-ttu-id="64f78-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64f78-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64f78-104">Gibt die Transaktionsattribute eines [Connection](connection-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="64f78-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64f78-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="64f78-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="64f78-106">Wert</span><span class="sxs-lookup"><span data-stu-id="64f78-106">Value</span></span></p></th>
<th><p><span data-ttu-id="64f78-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64f78-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64f78-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="64f78-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="64f78-109">262144</span><span class="sxs-lookup"><span data-stu-id="64f78-109">262144</span></span></p></td>
<td><p><span data-ttu-id="64f78-110">Führt Beibehaltungs Unterbrechungen aus; Das heißt, das Aufrufen von <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> startet automatisch eine neue Transaktion.</span><span class="sxs-lookup"><span data-stu-id="64f78-110">Performs retaining aborts; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="64f78-111">Nicht alle Anbieter unterstützen dies.</span><span class="sxs-lookup"><span data-stu-id="64f78-111">Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64f78-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="64f78-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="64f78-113">131072</span><span class="sxs-lookup"><span data-stu-id="64f78-113">131072</span></span></p></td>
<td><p><span data-ttu-id="64f78-114">Führt Aufbewahrungspflichten aus; Das heißt, das Aufrufen von <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> startet automatisch eine neue Transaktion.</span><span class="sxs-lookup"><span data-stu-id="64f78-114">Performs retaining commits; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="64f78-115">Nicht alle Anbieter unterstützen dies.</span><span class="sxs-lookup"><span data-stu-id="64f78-115">Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="64f78-116">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="64f78-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="64f78-117">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="64f78-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64f78-118">Konstante</span><span class="sxs-lookup"><span data-stu-id="64f78-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64f78-119">AdoEnums. XactAttribute. ABORTRETAINING</span><span class="sxs-lookup"><span data-stu-id="64f78-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64f78-120">AdoEnums. XactAttribute. COMMITRETAINING</span><span class="sxs-lookup"><span data-stu-id="64f78-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

