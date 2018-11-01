---
title: CursorDriverEnum Enumeration (DAO)
TOCTitle: CursorDriverEnum Enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25d264c1e91982231e025f17c00db79e47a1d5c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880740"
---
# <a name="cursordriverenum-enumeration-dao"></a><span data-ttu-id="31cad-102">CursorDriverEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="31cad-102">CursorDriverEnum Enumeration (DAO)</span></span>


<span data-ttu-id="31cad-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="31cad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31cad-104">Gibt den Typ des Cursortreibers an.</span><span class="sxs-lookup"><span data-stu-id="31cad-104">Specifies the type of cursor driver.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31cad-105">Name</span><span class="sxs-lookup"><span data-stu-id="31cad-105">Name</span></span></p></th>
<th><p><span data-ttu-id="31cad-106">Wert</span><span class="sxs-lookup"><span data-stu-id="31cad-106">Value</span></span></p></th>
<th><p><span data-ttu-id="31cad-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31cad-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31cad-108">dbUseClientBatchCursor</span><span class="sxs-lookup"><span data-stu-id="31cad-108">dbUseClientBatchCursor</span></span></p></td>
<td><p><span data-ttu-id="31cad-109">3</span><span class="sxs-lookup"><span data-stu-id="31cad-109">3</span></span></p></td>
<td><p><span data-ttu-id="31cad-p101">Verwendet immer die FoxPro-Cursorbibliothek. Diese Option ist für Batchaktualisierungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="31cad-p101">Always uses the FoxPro Cursor Library. This option is required for performing batch updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31cad-112">dbUseDefaultCursor</span><span class="sxs-lookup"><span data-stu-id="31cad-112">dbUseDefaultCursor</span></span></p></td>
<td><p><span data-ttu-id="31cad-113">-1</span><span class="sxs-lookup"><span data-stu-id="31cad-113">-1</span></span></p></td>
<td><p><span data-ttu-id="31cad-114">(Standard) Verwendet serverseitige Cursor, wenn diese vom Server unterstützt werden; andernfalls wird die ODBC-Cursorbibliothek verwendet.</span><span class="sxs-lookup"><span data-stu-id="31cad-114">(Default) Uses server-side cursors if the server supports them; otherwise uses the ODBC Cursor Library.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31cad-115">dbUseNoCursor</span><span class="sxs-lookup"><span data-stu-id="31cad-115">dbUseNoCursor</span></span></p></td>
<td><p><span data-ttu-id="31cad-116">4</span><span class="sxs-lookup"><span data-stu-id="31cad-116">4</span></span></p></td>
<td><p><span data-ttu-id="31cad-117">Öffnet alle Cursor (d. h., <strong>Recordset</strong> -Objekte) als Vorwärtscursor Typ schreibgeschützt, mit der Größe eines Rowsets 1 an.</span><span class="sxs-lookup"><span data-stu-id="31cad-117">Opens all cursors (that is, <strong>Recordset</strong> objects) as forward-only type, read-only, with a rowset size of 1.</span></span> <span data-ttu-id="31cad-118">Auch bekannt als &quot;Abfragen ohne Cursor.&quot;</span><span class="sxs-lookup"><span data-stu-id="31cad-118">Also known as &quot;cursorless queries.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31cad-119">dbUseODBCCursor</span><span class="sxs-lookup"><span data-stu-id="31cad-119">dbUseODBCCursor</span></span></p></td>
<td><p><span data-ttu-id="31cad-120">1</span><span class="sxs-lookup"><span data-stu-id="31cad-120">1</span></span></p></td>
<td><p><span data-ttu-id="31cad-p103">Verwendet immer die ODBC-Cursorbibliothek. Diese Option bietet für kleine Resultsets eine bessere Leistung, aber bei umfangreichen Resultsets wird die Leistung schnell beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="31cad-p103">Always uses the ODBC Cursor Library. This option provides better performance for small result sets, but degrades quickly for larger result sets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31cad-123">dbUseServerCursor</span><span class="sxs-lookup"><span data-stu-id="31cad-123">dbUseServerCursor</span></span></p></td>
<td><p><span data-ttu-id="31cad-124">2</span><span class="sxs-lookup"><span data-stu-id="31cad-124">2</span></span></p></td>
<td><p><span data-ttu-id="31cad-p104">Verwendet immer serverseitige Cursor. Für die meisten umfangreichen Vorgänge bietet diese Option eine bessere Leistung; sie kann jedoch mehr Netzwerkverkehr verursachen.</span><span class="sxs-lookup"><span data-stu-id="31cad-p104">Always uses server-side cursors. For most large operations this option provides better performance, but might cause more network traffic.</span></span></p></td>
</tr>
</tbody>
</table>

