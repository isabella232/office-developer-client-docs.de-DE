---
title: XactAttributeEnum (Access PC-Datenbank-Referenz)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 28b81c45921120b8a3cd8768d22559355d8ff623
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870492"
---
# <a name="xactattributeenum"></a><span data-ttu-id="22339-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="22339-102">XactAttributeEnum</span></span>

<span data-ttu-id="22339-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="22339-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="22339-104">Gibt die Transaktionsattribute eines [Connection](connection-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="22339-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22339-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="22339-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="22339-106">Wert</span><span class="sxs-lookup"><span data-stu-id="22339-106">Value</span></span></p></th>
<th><p><span data-ttu-id="22339-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22339-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22339-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="22339-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="22339-109">262144</span><span class="sxs-lookup"><span data-stu-id="22339-109">262144</span></span></p></td>
<td><p><span data-ttu-id="22339-110">Führt beibehaltene abgebrochen. durch Aufrufen von <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatisch startet das heißt, eine neue Transaktion.</span><span class="sxs-lookup"><span data-stu-id="22339-110">Performs retaining aborts; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="22339-111">Nicht alle Anbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22339-111">Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22339-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="22339-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="22339-113">131072</span><span class="sxs-lookup"><span data-stu-id="22339-113">131072</span></span></p></td>
<td><p><span data-ttu-id="22339-114">Führt beibehaltene Commits durch. durch Aufrufen von <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatisch startet das heißt, eine neue Transaktion.</span><span class="sxs-lookup"><span data-stu-id="22339-114">Performs retaining commits; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="22339-115">Nicht alle Anbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="22339-115">Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="22339-116">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="22339-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="22339-117">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="22339-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22339-118">Konstante</span><span class="sxs-lookup"><span data-stu-id="22339-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22339-119">AdoEnums.XactAttribute.ABORTRETAINING</span><span class="sxs-lookup"><span data-stu-id="22339-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22339-120">AdoEnums.XactAttribute.COMMITRETAINING</span><span class="sxs-lookup"><span data-stu-id="22339-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

