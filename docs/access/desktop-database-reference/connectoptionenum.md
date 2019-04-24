---
title: ConnectOptionEnum (Access Desktop Database Reference)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95b622d2216b085ffd0f76c8a26533187c17bd7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295681"
---
# <a name="connectoptionenum"></a><span data-ttu-id="2b4b0-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="2b4b0-102">ConnectOptionEnum</span></span>

<span data-ttu-id="2b4b0-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b4b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b4b0-104">Gibt an, ob die [Open](open-method-ado-connection.md)-Methode eines [Connection](connection-object-ado.md)-Objekts zurückgegeben werden soll, nachdem (synchron) oder bevor (asynchron) die Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2b4b0-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b4b0-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="2b4b0-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="2b4b0-106">Wert</span><span class="sxs-lookup"><span data-stu-id="2b4b0-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2b4b0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b4b0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b4b0-108"><strong>adAsyncConnect</strong></span><span class="sxs-lookup"><span data-stu-id="2b4b0-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="2b4b0-109">16</span><span class="sxs-lookup"><span data-stu-id="2b4b0-109">16</span></span></p></td>
<td><p><span data-ttu-id="2b4b0-p101">Öffnet die Verbindung asynchron. Das <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a>-Ereignis kann verwendet werden, um zu bestimmen, wann die Verbindung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="2b4b0-p101">Opens the connection asynchronously. The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b4b0-112"><strong>adConnectUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="2b4b0-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="2b4b0-113">-1</span><span class="sxs-lookup"><span data-stu-id="2b4b0-113">-1</span></span></p></td>
<td><p><span data-ttu-id="2b4b0-p102">Standardwert. Öffnet die Verbindung synchron.</span><span class="sxs-lookup"><span data-stu-id="2b4b0-p102">Default. Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2b4b0-116">ADO/WFC-Äquivalent</span><span class="sxs-lookup"><span data-stu-id="2b4b0-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="2b4b0-117">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="2b4b0-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b4b0-118">Konstante</span><span class="sxs-lookup"><span data-stu-id="2b4b0-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b4b0-119">AdoEnums. ConnectOption. ASYNCCONNECT</span><span class="sxs-lookup"><span data-stu-id="2b4b0-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b4b0-120">AdoEnums. ConnectOption. CONNECTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="2b4b0-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

