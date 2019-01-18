---
title: QueryDefStateEnum (Aufzählung) (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ca9923b1604b17c1d7f64d2d968378fec4a8c24
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698659"
---
# <a name="querydefstateenum-enumeration-dao"></a><span data-ttu-id="51994-102">QueryDefStateEnum (Aufzählung) (DAO)</span><span class="sxs-lookup"><span data-stu-id="51994-102">QueryDefStateEnum enumeration (DAO)</span></span>


<span data-ttu-id="51994-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51994-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51994-104">Hiermit geben Sie zusammen mit der **Prepare**-Eigenschaft die Methode für die Vorbereitung einer Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="51994-104">Used with the **Prepare** property to specify the method used to specify how a query should be prepared.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51994-105">Name</span><span class="sxs-lookup"><span data-stu-id="51994-105">Name</span></span></p></th>
<th><p><span data-ttu-id="51994-106">Wert</span><span class="sxs-lookup"><span data-stu-id="51994-106">Value</span></span></p></th>
<th><p><span data-ttu-id="51994-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51994-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51994-108">dbQPrepare</span><span class="sxs-lookup"><span data-stu-id="51994-108">dbQPrepare</span></span></p></td>
<td><p><span data-ttu-id="51994-109">1</span><span class="sxs-lookup"><span data-stu-id="51994-109">1</span></span></p></td>
<td><p><span data-ttu-id="51994-110">(Standard) Die Anweisung wird vorbereitet (d. h. die ODBC-API SQLPrepare wird aufgerufen).</span><span class="sxs-lookup"><span data-stu-id="51994-110">(Default) The statement is prepared (that is, the ODBC SQLPrepare API is called).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51994-111">dbQUnprepare</span><span class="sxs-lookup"><span data-stu-id="51994-111">dbQUnprepare</span></span></p></td>
<td><p><span data-ttu-id="51994-112">2</span><span class="sxs-lookup"><span data-stu-id="51994-112">2</span></span></p></td>
<td><p><span data-ttu-id="51994-113">Die Anweisung wird nicht vorbereitet (d. h. die ODBC-API SQLExecDirect wird aufgerufen).</span><span class="sxs-lookup"><span data-stu-id="51994-113">The statement is not prepared (that is, the ODBC SQLExecDirect API is called).</span></span></p></td>
</tr>
</tbody>
</table>

