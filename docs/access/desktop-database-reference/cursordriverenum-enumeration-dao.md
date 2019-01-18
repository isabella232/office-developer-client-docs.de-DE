---
title: CursorDriverEnum (Aufzählung) (DAO)
TOCTitle: CursorDriverEnum enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f2bf52943a84d6f2e60891d63810bc0bbb6ecb3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710731"
---
# <a name="cursordriverenum-enumeration-dao"></a><span data-ttu-id="865e8-102">CursorDriverEnum (Aufzählung) (DAO)</span><span class="sxs-lookup"><span data-stu-id="865e8-102">CursorDriverEnum enumeration (DAO)</span></span>

<span data-ttu-id="865e8-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="865e8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="865e8-104">Gibt den Typ des Cursortreibers an.</span><span class="sxs-lookup"><span data-stu-id="865e8-104">Specifies the type of cursor driver.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="865e8-105">Name</span><span class="sxs-lookup"><span data-stu-id="865e8-105">Name</span></span></p></th>
<th><p><span data-ttu-id="865e8-106">Wert</span><span class="sxs-lookup"><span data-stu-id="865e8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="865e8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="865e8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="865e8-108">dbUseClientBatchCursor</span><span class="sxs-lookup"><span data-stu-id="865e8-108">dbUseClientBatchCursor</span></span></p></td>
<td><p><span data-ttu-id="865e8-109">3</span><span class="sxs-lookup"><span data-stu-id="865e8-109">3</span></span></p></td>
<td><p><span data-ttu-id="865e8-p101">Verwendet immer die FoxPro-Cursorbibliothek. Diese Option ist für Batchaktualisierungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="865e8-p101">Always uses the FoxPro Cursor Library. This option is required for performing batch updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="865e8-112">dbUseDefaultCursor</span><span class="sxs-lookup"><span data-stu-id="865e8-112">dbUseDefaultCursor</span></span></p></td>
<td><p><span data-ttu-id="865e8-113">-1</span><span class="sxs-lookup"><span data-stu-id="865e8-113">-1</span></span></p></td>
<td><p><span data-ttu-id="865e8-114">(Standard) Verwendet serverseitige Cursor, wenn diese vom Server unterstützt werden; andernfalls wird die ODBC-Cursorbibliothek verwendet.</span><span class="sxs-lookup"><span data-stu-id="865e8-114">(Default) Uses server-side cursors if the server supports them; otherwise uses the ODBC Cursor Library.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="865e8-115">dbUseNoCursor</span><span class="sxs-lookup"><span data-stu-id="865e8-115">dbUseNoCursor</span></span></p></td>
<td><p><span data-ttu-id="865e8-116">4</span><span class="sxs-lookup"><span data-stu-id="865e8-116">4</span></span></p></td>
<td><p><span data-ttu-id="865e8-117">Öffnet alle Cursor (d. h., <strong>Recordset</strong> -Objekte) als Vorwärtscursor Typ schreibgeschützt, mit der Größe eines Rowsets 1 an.</span><span class="sxs-lookup"><span data-stu-id="865e8-117">Opens all cursors (that is, <strong>Recordset</strong> objects) as forward-only type, read-only, with a rowset size of 1.</span></span> <span data-ttu-id="865e8-118">Auch bekannt als &quot;Abfragen ohne Cursor.&quot;</span><span class="sxs-lookup"><span data-stu-id="865e8-118">Also known as &quot;cursorless queries.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="865e8-119">dbUseODBCCursor</span><span class="sxs-lookup"><span data-stu-id="865e8-119">dbUseODBCCursor</span></span></p></td>
<td><p><span data-ttu-id="865e8-120">1</span><span class="sxs-lookup"><span data-stu-id="865e8-120">1</span></span></p></td>
<td><p><span data-ttu-id="865e8-p103">Verwendet immer die ODBC-Cursorbibliothek. Diese Option bietet für kleine Resultsets eine bessere Leistung, aber bei umfangreichen Resultsets wird die Leistung schnell beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="865e8-p103">Always uses the ODBC Cursor Library. This option provides better performance for small result sets, but degrades quickly for larger result sets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="865e8-123">dbUseServerCursor</span><span class="sxs-lookup"><span data-stu-id="865e8-123">dbUseServerCursor</span></span></p></td>
<td><p><span data-ttu-id="865e8-124">2</span><span class="sxs-lookup"><span data-stu-id="865e8-124">2</span></span></p></td>
<td><p><span data-ttu-id="865e8-p104">Verwendet immer serverseitige Cursor. Für die meisten umfangreichen Vorgänge bietet diese Option eine bessere Leistung; sie kann jedoch mehr Netzwerkverkehr verursachen.</span><span class="sxs-lookup"><span data-stu-id="865e8-p104">Always uses server-side cursors. For most large operations this option provides better performance, but might cause more network traffic.</span></span></p></td>
</tr>
</tbody>
</table>

