---
title: ConnectOptionEnum (Access PC-Datenbank-Referenz)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 37420ab37b350f0f852305958edbf414d9aecdb3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867314"
---
# <a name="connectoptionenum"></a><span data-ttu-id="bf01d-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="bf01d-102">ConnectOptionEnum</span></span>

<span data-ttu-id="bf01d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf01d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bf01d-104">Gibt an, ob die [Open](open-method-ado-connection.md)-Methode eines [Connection](connection-object-ado.md)-Objekts zurückgegeben werden soll, nachdem (synchron) oder bevor (asynchron) die Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bf01d-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf01d-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="bf01d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="bf01d-106">Wert</span><span class="sxs-lookup"><span data-stu-id="bf01d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="bf01d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf01d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf01d-108"><strong>adAsyncConnect</strong></span><span class="sxs-lookup"><span data-stu-id="bf01d-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="bf01d-109">16</span><span class="sxs-lookup"><span data-stu-id="bf01d-109">16</span></span></p></td>
<td><p><span data-ttu-id="bf01d-p101">Öffnet die Verbindung asynchron. Das <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a>-Ereignis kann verwendet werden, um zu bestimmen, wann die Verbindung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="bf01d-p101">Opens the connection asynchronously. The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf01d-112"><strong>adConnectUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="bf01d-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="bf01d-113">-1</span><span class="sxs-lookup"><span data-stu-id="bf01d-113">-1</span></span></p></td>
<td><p><span data-ttu-id="bf01d-p102">Standardwert. Öffnet die Verbindung synchron.</span><span class="sxs-lookup"><span data-stu-id="bf01d-p102">Default. Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="bf01d-116">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="bf01d-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="bf01d-117">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="bf01d-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf01d-118">Konstante</span><span class="sxs-lookup"><span data-stu-id="bf01d-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf01d-119">AdoEnums.ConnectOption.ASYNCCONNECT</span><span class="sxs-lookup"><span data-stu-id="bf01d-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf01d-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="bf01d-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

