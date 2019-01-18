---
title: ConnectOptionEnum (Access PC-Datenbank-Referenz)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95b622d2216b085ffd0f76c8a26533187c17bd7b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699960"
---
# <a name="connectoptionenum"></a><span data-ttu-id="b0448-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="b0448-102">ConnectOptionEnum</span></span>

<span data-ttu-id="b0448-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0448-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0448-104">Gibt an, ob die [Open](open-method-ado-connection.md)-Methode eines [Connection](connection-object-ado.md)-Objekts zurückgegeben werden soll, nachdem (synchron) oder bevor (asynchron) die Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b0448-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0448-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="b0448-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b0448-106">Wert</span><span class="sxs-lookup"><span data-stu-id="b0448-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b0448-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0448-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0448-108"><strong>adAsyncConnect</strong></span><span class="sxs-lookup"><span data-stu-id="b0448-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="b0448-109">16</span><span class="sxs-lookup"><span data-stu-id="b0448-109">16</span></span></p></td>
<td><p><span data-ttu-id="b0448-p101">Öffnet die Verbindung asynchron. Das <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a>-Ereignis kann verwendet werden, um zu bestimmen, wann die Verbindung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b0448-p101">Opens the connection asynchronously. The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0448-112"><strong>adConnectUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="b0448-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="b0448-113">-1</span><span class="sxs-lookup"><span data-stu-id="b0448-113">-1</span></span></p></td>
<td><p><span data-ttu-id="b0448-p102">Standardwert. Öffnet die Verbindung synchron.</span><span class="sxs-lookup"><span data-stu-id="b0448-p102">Default. Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="b0448-116">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="b0448-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="b0448-117">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="b0448-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0448-118">Konstante</span><span class="sxs-lookup"><span data-stu-id="b0448-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0448-119">AdoEnums.ConnectOption.ASYNCCONNECT</span><span class="sxs-lookup"><span data-stu-id="b0448-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0448-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="b0448-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

