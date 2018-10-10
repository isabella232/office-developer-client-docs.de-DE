---
title: ConnectOptionEnum (Access PC-Datenbank-Referenz)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e2e8439099732cd3e1e9aa7531f5ae3be25d7ebe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472987"
---
# <a name="connectoptionenum"></a><span data-ttu-id="ba021-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="ba021-102">ConnectOptionEnum</span></span>


<span data-ttu-id="ba021-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba021-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ba021-104">Gibt an, ob die [Open](open-method-ado-connection.md)-Methode eines [Connection](connection-object-ado.md)-Objekts zurückgegeben werden soll, nachdem (synchron) oder bevor (asynchron) die Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ba021-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ba021-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="ba021-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ba021-106">Wert</span><span class="sxs-lookup"><span data-stu-id="ba021-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ba021-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba021-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba021-108"><strong>adAsyncConnect</strong></span><span class="sxs-lookup"><span data-stu-id="ba021-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="ba021-109">16</span><span class="sxs-lookup"><span data-stu-id="ba021-109">16</span></span></p></td>
<td><p><span data-ttu-id="ba021-p101">Öffnet die Verbindung asynchron. Das <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a>-Ereignis kann verwendet werden, um zu bestimmen, wann die Verbindung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ba021-p101">Opens the connection asynchronously. The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba021-112"><strong>adConnectUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="ba021-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="ba021-113">-1</span><span class="sxs-lookup"><span data-stu-id="ba021-113">-1</span></span></p></td>
<td><p><span data-ttu-id="ba021-p102">Standardwert. Öffnet die Verbindung synchron.</span><span class="sxs-lookup"><span data-stu-id="ba021-p102">Default. Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ba021-116">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="ba021-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="ba021-117">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="ba021-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ba021-118">Konstante</span><span class="sxs-lookup"><span data-stu-id="ba021-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba021-119">AdoEnums.ConnectOption.ASYNCCONNECT</span><span class="sxs-lookup"><span data-stu-id="ba021-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba021-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="ba021-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

