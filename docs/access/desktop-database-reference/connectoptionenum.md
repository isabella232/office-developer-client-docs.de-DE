---
title: ConnectOptionEnum (Access PC-Datenbank-Referenz)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 76203f1406a3152488f6404b1a9eb47e541c3351
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864186"
---
# <a name="connectoptionenum"></a><span data-ttu-id="0ea3d-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="0ea3d-102">ConnectOptionEnum</span></span>

<span data-ttu-id="0ea3d-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ea3d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0ea3d-104">Gibt an, ob die [Open](open-method-ado-connection.md)-Methode eines [Connection](connection-object-ado.md)-Objekts zurückgegeben werden soll, nachdem (synchron) oder bevor (asynchron) die Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0ea3d-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ea3d-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="0ea3d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="0ea3d-106">Wert</span><span class="sxs-lookup"><span data-stu-id="0ea3d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0ea3d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ea3d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ea3d-108"><strong>adAsyncConnect</strong></span><span class="sxs-lookup"><span data-stu-id="0ea3d-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea3d-109">16</span><span class="sxs-lookup"><span data-stu-id="0ea3d-109">16</span></span></p></td>
<td><p><span data-ttu-id="0ea3d-p101">Öffnet die Verbindung asynchron. Das <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a>-Ereignis kann verwendet werden, um zu bestimmen, wann die Verbindung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0ea3d-p101">Opens the connection asynchronously. The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea3d-112"><strong>adConnectUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="0ea3d-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="0ea3d-113">-1</span><span class="sxs-lookup"><span data-stu-id="0ea3d-113">-1</span></span></p></td>
<td><p><span data-ttu-id="0ea3d-p102">Standardwert. Öffnet die Verbindung synchron.</span><span class="sxs-lookup"><span data-stu-id="0ea3d-p102">Default. Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="0ea3d-116">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="0ea3d-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="0ea3d-117">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="0ea3d-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ea3d-118">Konstante</span><span class="sxs-lookup"><span data-stu-id="0ea3d-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ea3d-119">AdoEnums.ConnectOption.ASYNCCONNECT</span><span class="sxs-lookup"><span data-stu-id="0ea3d-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea3d-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="0ea3d-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

