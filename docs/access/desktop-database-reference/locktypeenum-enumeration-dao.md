---
title: LockTypeEnum Enumeration (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 771ce7a5a7f0a6721703953029b7bc8de9f0f251
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936574"
---
# <a name="locktypeenum-enumeration-dao"></a><span data-ttu-id="3d689-102">LockTypeEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="3d689-102">LockTypeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="3d689-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d689-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d689-104">Gibt die Art der Datensatzsperrung an, die beim Öffnen eines Datensatzes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3d689-104">Specifies the type of record locking used when opening a recordset.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d689-105">Name</span><span class="sxs-lookup"><span data-stu-id="3d689-105">Name</span></span></p></th>
<th><p><span data-ttu-id="3d689-106">Wert</span><span class="sxs-lookup"><span data-stu-id="3d689-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3d689-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d689-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d689-108">dbOptimistic</span><span class="sxs-lookup"><span data-stu-id="3d689-108">dbOptimistic</span></span></p></td>
<td><p><span data-ttu-id="3d689-109">3</span><span class="sxs-lookup"><span data-stu-id="3d689-109">3</span></span></p></td>
<td><p><span data-ttu-id="3d689-p101">Vollständige Parallelität basierend auf der Datensatz-ID. Der Cursor vergleicht die Datensatz-ID in alten und neuen Datensätzen, um zu bestimmen, ob seit dem letzten Zugriff auf den Datensatz Änderungen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="3d689-p101">Optimistic concurrency based on record ID. Cursor compares record ID in old and new records to determine if changes have been made since the record was last accessed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d689-112">dbOptimisticBatch</span><span class="sxs-lookup"><span data-stu-id="3d689-112">dbOptimisticBatch</span></span></p></td>
<td><p><span data-ttu-id="3d689-113">5</span><span class="sxs-lookup"><span data-stu-id="3d689-113">5</span></span></p></td>
<td><p><span data-ttu-id="3d689-114">Aktiviert vollständige Batchaktualisierungen (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="3d689-114">Enables batch optimistic updates (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d689-115">dbOptimisticValue</span><span class="sxs-lookup"><span data-stu-id="3d689-115">dbOptimisticValue</span></span></p></td>
<td><p><span data-ttu-id="3d689-116">1</span><span class="sxs-lookup"><span data-stu-id="3d689-116">1</span></span></p></td>
<td><p><span data-ttu-id="3d689-p102">Vollständige Parallelität basierend auf Datensatzwerten. Der Cursor vergleicht Datenwerte in alten und neuen Datensätzen, um zu bestimmen, ob seit dem letzten Zugriff auf den Datensatz Änderungen vorgenommen wurden (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="3d689-p102">Optimistic concurrency based on record values. Cursor compares data values in old and new records to determine if changes have been made since the record was last accessed (ODBCDirect workspaces only).</span></span></p>

> [!NOTE]
> <span data-ttu-id="3d689-p103">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d689-p103">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d689-121">dbPessimistic</span><span class="sxs-lookup"><span data-stu-id="3d689-121">dbPessimistic</span></span></p></td>
<td><p><span data-ttu-id="3d689-122">2</span><span class="sxs-lookup"><span data-stu-id="3d689-122">2</span></span></p></td>
<td><p><span data-ttu-id="3d689-p104">Eingeschränkte Parallelität. Der Cursor verwendet die niedrigste Sperrebene, mit der sichergestellt ist, dass der Datensatz aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3d689-p104">Pessimistic concurrency. Cursor uses the lowest level of locking sufficient to ensure that the record can be updated.</span></span></p></td>
</tr>
</tbody>
</table>

