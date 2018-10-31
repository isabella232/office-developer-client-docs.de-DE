---
title: PersistFormatEnum (Access PC-Datenbank-Referenz)
TOCTitle: PersistFormatEnum
ms:assetid: 5aa99a63-d422-0812-5aba-19305a3ad405
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249313(v=office.15)
ms:contentKeyID: 48545050
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 65c33389bc7eb703fce6c44da3507a28bccb75eb
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862478"
---
# <a name="persistformatenum"></a><span data-ttu-id="89b4b-102">PersistFormatEnum</span><span class="sxs-lookup"><span data-stu-id="89b4b-102">PersistFormatEnum</span></span>

<span data-ttu-id="89b4b-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="89b4b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="89b4b-104">Gibt das Format an, in dem ein [Recordset](recordset-object-ado.md) gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="89b4b-104">Specifies the format in which to save a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89b4b-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="89b4b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="89b4b-106">Wert</span><span class="sxs-lookup"><span data-stu-id="89b4b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="89b4b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89b4b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89b4b-108"><strong>adPersistADTG</strong></span><span class="sxs-lookup"><span data-stu-id="89b4b-108"><strong>adPersistADTG</strong></span></span></p></td>
<td><p><span data-ttu-id="89b4b-109">0</span><span class="sxs-lookup"><span data-stu-id="89b4b-109">0</span></span></p></td>
<td><p><span data-ttu-id="89b4b-110">Gibt das Microsoft Advanced Data TableGram-Format (ADTG) an.</span><span class="sxs-lookup"><span data-stu-id="89b4b-110">Indicates Microsoft Advanced Data TableGram (ADTG) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89b4b-111"><strong>adPersistADO</strong></span><span class="sxs-lookup"><span data-stu-id="89b4b-111"><strong>adPersistADO</strong></span></span></p></td>
<td><p><span data-ttu-id="89b4b-112">1</span><span class="sxs-lookup"><span data-stu-id="89b4b-112">1</span></span></p></td>
<td><p><span data-ttu-id="89b4b-p101">Gibt an, dass das XML-Format von ADO verwendet wird. Dieser Wert entspricht AdPersistXML und ist zum Zwecke der Abwärtskompatibilität eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="89b4b-p101">Indicates that ADO's own Extensible Markup Language (XML) format will be used. This value is the same as adPersistXML and is included for backwards compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89b4b-115"><strong>adPersistXML</strong></span><span class="sxs-lookup"><span data-stu-id="89b4b-115"><strong>adPersistXML</strong></span></span></p></td>
<td><p><span data-ttu-id="89b4b-116">1</span><span class="sxs-lookup"><span data-stu-id="89b4b-116">1</span></span></p></td>
<td><p><span data-ttu-id="89b4b-117">Gibt das XML-Format an.</span><span class="sxs-lookup"><span data-stu-id="89b4b-117">Indicates Extensible Markup Language (XML) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89b4b-118"><strong>adPersistProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="89b4b-118"><strong>adPersistProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="89b4b-119">2</span><span class="sxs-lookup"><span data-stu-id="89b4b-119">2</span></span></p></td>
<td><p><span data-ttu-id="89b4b-120">Gibt an, dass der Anbieter das <strong>Recordset</strong> mit seinem eigenen Format beibehält.</span><span class="sxs-lookup"><span data-stu-id="89b4b-120">Indicates that the provider will persist the <strong>Recordset</strong> using its own format.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="89b4b-121">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="89b4b-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="89b4b-122">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="89b4b-122">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89b4b-123">Konstante</span><span class="sxs-lookup"><span data-stu-id="89b4b-123">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89b4b-124">AdoEnums.PersistFormat.ADTG</span><span class="sxs-lookup"><span data-stu-id="89b4b-124">AdoEnums.PersistFormat.ADTG</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89b4b-125">AdoEnums.PersistFormat.XML</span><span class="sxs-lookup"><span data-stu-id="89b4b-125">AdoEnums.PersistFormat.XML</span></span></p></td>
</tr>
</tbody>
</table>

