---
title: LockTypeEnum Enumeration (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 82a09db7baff93ba7fd51de593bc4d1dfff41dc1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474194"
---
# <a name="locktypeenum-enumeration-dao"></a><span data-ttu-id="b859a-102">LockTypeEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="b859a-102">LockTypeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="b859a-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b859a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b859a-104">Gibt die Art der Datensatzsperrung an, die beim Öffnen eines Datensatzes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b859a-104">Specifies the type of record locking used when opening a recordset.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b859a-105">Name</span><span class="sxs-lookup"><span data-stu-id="b859a-105">Name</span></span></p></th>
<th><p><span data-ttu-id="b859a-106">Wert</span><span class="sxs-lookup"><span data-stu-id="b859a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b859a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b859a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b859a-108">dbOptimistic</span><span class="sxs-lookup"><span data-stu-id="b859a-108">dbOptimistic</span></span></p></td>
<td><p><span data-ttu-id="b859a-109">3</span><span class="sxs-lookup"><span data-stu-id="b859a-109">3</span></span></p></td>
<td><p><span data-ttu-id="b859a-p101">Vollständige Parallelität basierend auf der Datensatz-ID. Der Cursor vergleicht die Datensatz-ID in alten und neuen Datensätzen, um zu bestimmen, ob seit dem letzten Zugriff auf den Datensatz Änderungen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="b859a-p101">Optimistic concurrency based on record ID. Cursor compares record ID in old and new records to determine if changes have been made since the record was last accessed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b859a-112">dbOptimisticBatch</span><span class="sxs-lookup"><span data-stu-id="b859a-112">dbOptimisticBatch</span></span></p></td>
<td><p><span data-ttu-id="b859a-113">5</span><span class="sxs-lookup"><span data-stu-id="b859a-113">5</span></span></p></td>
<td><p><span data-ttu-id="b859a-114">Aktiviert vollständige Batchaktualisierungen (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="b859a-114">Enables batch optimistic updates (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b859a-115">dbOptimisticValue</span><span class="sxs-lookup"><span data-stu-id="b859a-115">dbOptimisticValue</span></span></p></td>
<td><p><span data-ttu-id="b859a-116">1</span><span class="sxs-lookup"><span data-stu-id="b859a-116">1</span></span></p></td>
<td><p><span data-ttu-id="b859a-p102">Vollständige Parallelität basierend auf Datensatzwerten. Der Cursor vergleicht Datenwerte in alten und neuen Datensätzen, um zu bestimmen, ob seit dem letzten Zugriff auf den Datensatz Änderungen vorgenommen wurden (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="b859a-p102">Optimistic concurrency based on record values. Cursor compares data values in old and new records to determine if changes have been made since the record was last accessed (ODBCDirect workspaces only).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="b859a-p103">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b859a-p103">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b859a-121">dbPessimistic</span><span class="sxs-lookup"><span data-stu-id="b859a-121">dbPessimistic</span></span></p></td>
<td><p><span data-ttu-id="b859a-122">2</span><span class="sxs-lookup"><span data-stu-id="b859a-122">2</span></span></p></td>
<td><p><span data-ttu-id="b859a-p104">Eingeschränkte Parallelität. Der Cursor verwendet die niedrigste Sperrebene, mit der sichergestellt ist, dass der Datensatz aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b859a-p104">Pessimistic concurrency. Cursor uses the lowest level of locking sufficient to ensure that the record can be updated.</span></span></p></td>
</tr>
</tbody>
</table>

