---
title: LockTypeEnum Enumeration (DAO)
TOCTitle: LockTypeEnum Enumeration
ms:assetid: d40f984c-b37f-72f7-7b05-752f106b6029
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834802(v=office.15)
ms:contentKeyID: 48547925
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f0e12f8d60ee3147eb456df302122a5b7eac684d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879928"
---
# <a name="locktypeenum-enumeration-dao"></a><span data-ttu-id="bdcf3-102">LockTypeEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="bdcf3-102">LockTypeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="bdcf3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bdcf3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bdcf3-104">Gibt die Art der Datensatzsperrung an, die beim Öffnen eines Datensatzes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdcf3-104">Specifies the type of record locking used when opening a recordset.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bdcf3-105">Name</span><span class="sxs-lookup"><span data-stu-id="bdcf3-105">Name</span></span></p></th>
<th><p><span data-ttu-id="bdcf3-106">Wert</span><span class="sxs-lookup"><span data-stu-id="bdcf3-106">Value</span></span></p></th>
<th><p><span data-ttu-id="bdcf3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdcf3-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bdcf3-108">dbOptimistic</span><span class="sxs-lookup"><span data-stu-id="bdcf3-108">dbOptimistic</span></span></p></td>
<td><p><span data-ttu-id="bdcf3-109">3</span><span class="sxs-lookup"><span data-stu-id="bdcf3-109">3</span></span></p></td>
<td><p><span data-ttu-id="bdcf3-p101">Vollständige Parallelität basierend auf der Datensatz-ID. Der Cursor vergleicht die Datensatz-ID in alten und neuen Datensätzen, um zu bestimmen, ob seit dem letzten Zugriff auf den Datensatz Änderungen vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="bdcf3-p101">Optimistic concurrency based on record ID. Cursor compares record ID in old and new records to determine if changes have been made since the record was last accessed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdcf3-112">dbOptimisticBatch</span><span class="sxs-lookup"><span data-stu-id="bdcf3-112">dbOptimisticBatch</span></span></p></td>
<td><p><span data-ttu-id="bdcf3-113">5</span><span class="sxs-lookup"><span data-stu-id="bdcf3-113">5</span></span></p></td>
<td><p><span data-ttu-id="bdcf3-114">Aktiviert vollständige Batchaktualisierungen (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="bdcf3-114">Enables batch optimistic updates (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdcf3-115">dbOptimisticValue</span><span class="sxs-lookup"><span data-stu-id="bdcf3-115">dbOptimisticValue</span></span></p></td>
<td><p><span data-ttu-id="bdcf3-116">1</span><span class="sxs-lookup"><span data-stu-id="bdcf3-116">1</span></span></p></td>
<td><p><span data-ttu-id="bdcf3-p102">Vollständige Parallelität basierend auf Datensatzwerten. Der Cursor vergleicht Datenwerte in alten und neuen Datensätzen, um zu bestimmen, ob seit dem letzten Zugriff auf den Datensatz Änderungen vorgenommen wurden (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="bdcf3-p102">Optimistic concurrency based on record values. Cursor compares data values in old and new records to determine if changes have been made since the record was last accessed (ODBCDirect workspaces only).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="bdcf3-p103">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bdcf3-p103">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdcf3-121">dbPessimistic</span><span class="sxs-lookup"><span data-stu-id="bdcf3-121">dbPessimistic</span></span></p></td>
<td><p><span data-ttu-id="bdcf3-122">2</span><span class="sxs-lookup"><span data-stu-id="bdcf3-122">2</span></span></p></td>
<td><p><span data-ttu-id="bdcf3-p104">Eingeschränkte Parallelität. Der Cursor verwendet die niedrigste Sperrebene, mit der sichergestellt ist, dass der Datensatz aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bdcf3-p104">Pessimistic concurrency. Cursor uses the lowest level of locking sufficient to ensure that the record can be updated.</span></span></p></td>
</tr>
</tbody>
</table>

