---
title: ConnectPromptEnum (Access PC-Datenbank-Referenz)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e405b1eb3a1326d56a32c432fb212de417cf3469
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475792"
---
# <a name="connectpromptenum"></a><span data-ttu-id="bbd2d-102">ConnectPromptEnum</span><span class="sxs-lookup"><span data-stu-id="bbd2d-102">ConnectPromptEnum</span></span>


<span data-ttu-id="bbd2d-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bbd2d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bbd2d-104">Gibt an, ob ein Dialogfeld angezeigt werden soll, um beim Öffnen einer Verbindung mit einer Datenquelle fehlende Parameter anzufordern.</span><span class="sxs-lookup"><span data-stu-id="bbd2d-104">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to a data source.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbd2d-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="bbd2d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="bbd2d-106">Wert</span><span class="sxs-lookup"><span data-stu-id="bbd2d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="bbd2d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bbd2d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbd2d-108"><strong>adPromptAlways</strong></span><span class="sxs-lookup"><span data-stu-id="bbd2d-108"><strong>adPromptAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="bbd2d-109">1</span><span class="sxs-lookup"><span data-stu-id="bbd2d-109">1</span></span></p></td>
<td><p><span data-ttu-id="bbd2d-110">Fordert immer auf.</span><span class="sxs-lookup"><span data-stu-id="bbd2d-110">Prompts always.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd2d-111"><strong>adPromptComplete</strong></span><span class="sxs-lookup"><span data-stu-id="bbd2d-111"><strong>adPromptComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="bbd2d-112">2</span><span class="sxs-lookup"><span data-stu-id="bbd2d-112">2</span></span></p></td>
<td><p><span data-ttu-id="bbd2d-113">Fordert auf, wenn weitere Informationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="bbd2d-113">Prompts if more information is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbd2d-114"><strong>adPromptCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="bbd2d-114"><strong>adPromptCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="bbd2d-115">3</span><span class="sxs-lookup"><span data-stu-id="bbd2d-115">3</span></span></p></td>
<td><p><span data-ttu-id="bbd2d-116">Fordert auf, wenn weitere Informationen erforderlich sind, optionale Parameter jedoch nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="bbd2d-116">Prompts if more information is required but optional parameters are not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd2d-117"><strong>adPromptNever</strong></span><span class="sxs-lookup"><span data-stu-id="bbd2d-117"><strong>adPromptNever</strong></span></span></p></td>
<td><p><span data-ttu-id="bbd2d-118">4</span><span class="sxs-lookup"><span data-stu-id="bbd2d-118">4</span></span></p></td>
<td><p><span data-ttu-id="bbd2d-119">Fordert nie auf.</span><span class="sxs-lookup"><span data-stu-id="bbd2d-119">Never prompts.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bbd2d-120">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="bbd2d-120">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="bbd2d-121">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="bbd2d-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbd2d-122">Konstante</span><span class="sxs-lookup"><span data-stu-id="bbd2d-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbd2d-123">AdoEnums.ConnectPrompt.ALWAYS</span><span class="sxs-lookup"><span data-stu-id="bbd2d-123">AdoEnums.ConnectPrompt.ALWAYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd2d-124">AdoEnums.ConnectPrompt.COMPLETE</span><span class="sxs-lookup"><span data-stu-id="bbd2d-124">AdoEnums.ConnectPrompt.COMPLETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbd2d-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span><span class="sxs-lookup"><span data-stu-id="bbd2d-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbd2d-126">AdoEnums.ConnectPrompt.NEVER</span><span class="sxs-lookup"><span data-stu-id="bbd2d-126">AdoEnums.ConnectPrompt.NEVER</span></span></p></td>
</tr>
</tbody>
</table>

