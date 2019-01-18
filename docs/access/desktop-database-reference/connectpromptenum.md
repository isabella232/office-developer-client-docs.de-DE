---
title: ConnectPromptEnum (Access PC-Datenbank-Referenz)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54643a66316d7f534553c20ecc3aafdf755fb857
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701109"
---
# <a name="connectpromptenum"></a><span data-ttu-id="557e9-102">ConnectPromptEnum</span><span class="sxs-lookup"><span data-stu-id="557e9-102">ConnectPromptEnum</span></span>

<span data-ttu-id="557e9-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="557e9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="557e9-104">Gibt an, ob ein Dialogfeld angezeigt werden soll, um beim Öffnen einer Verbindung mit einer Datenquelle fehlende Parameter anzufordern.</span><span class="sxs-lookup"><span data-stu-id="557e9-104">Specifies whether a dialog box should be displayed to prompt for missing parameters when opening a connection to a data source.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="557e9-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="557e9-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="557e9-106">Wert</span><span class="sxs-lookup"><span data-stu-id="557e9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="557e9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="557e9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="557e9-108"><strong>adPromptAlways</strong></span><span class="sxs-lookup"><span data-stu-id="557e9-108"><strong>adPromptAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="557e9-109">1</span><span class="sxs-lookup"><span data-stu-id="557e9-109">1</span></span></p></td>
<td><p><span data-ttu-id="557e9-110">Fordert immer auf.</span><span class="sxs-lookup"><span data-stu-id="557e9-110">Prompts always.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="557e9-111"><strong>adPromptComplete</strong></span><span class="sxs-lookup"><span data-stu-id="557e9-111"><strong>adPromptComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="557e9-112">2</span><span class="sxs-lookup"><span data-stu-id="557e9-112">2</span></span></p></td>
<td><p><span data-ttu-id="557e9-113">Fordert auf, wenn weitere Informationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="557e9-113">Prompts if more information is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="557e9-114"><strong>adPromptCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="557e9-114"><strong>adPromptCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="557e9-115">3</span><span class="sxs-lookup"><span data-stu-id="557e9-115">3</span></span></p></td>
<td><p><span data-ttu-id="557e9-116">Fordert auf, wenn weitere Informationen erforderlich sind, optionale Parameter jedoch nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="557e9-116">Prompts if more information is required but optional parameters are not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="557e9-117"><strong>adPromptNever</strong></span><span class="sxs-lookup"><span data-stu-id="557e9-117"><strong>adPromptNever</strong></span></span></p></td>
<td><p><span data-ttu-id="557e9-118">4</span><span class="sxs-lookup"><span data-stu-id="557e9-118">4</span></span></p></td>
<td><p><span data-ttu-id="557e9-119">Fordert nie auf.</span><span class="sxs-lookup"><span data-stu-id="557e9-119">Never prompts.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="557e9-120">ADO/WFC-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="557e9-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="557e9-121">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="557e9-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="557e9-122">Konstante</span><span class="sxs-lookup"><span data-stu-id="557e9-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="557e9-123">AdoEnums.ConnectPrompt.ALWAYS</span><span class="sxs-lookup"><span data-stu-id="557e9-123">AdoEnums.ConnectPrompt.ALWAYS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="557e9-124">AdoEnums.ConnectPrompt.COMPLETE</span><span class="sxs-lookup"><span data-stu-id="557e9-124">AdoEnums.ConnectPrompt.COMPLETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="557e9-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span><span class="sxs-lookup"><span data-stu-id="557e9-125">AdoEnums.ConnectPrompt.COMPLETEREQUIRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="557e9-126">AdoEnums.ConnectPrompt.NEVER</span><span class="sxs-lookup"><span data-stu-id="557e9-126">AdoEnums.ConnectPrompt.NEVER</span></span></p></td>
</tr>
</tbody>
</table>

