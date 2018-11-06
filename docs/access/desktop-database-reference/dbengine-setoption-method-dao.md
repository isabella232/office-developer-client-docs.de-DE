---
title: DBEngine.SetOption-Methode (DAO)
TOCTitle: SetOption Method
ms:assetid: ea55c10c-2385-1b7e-0cba-32982c9b6643
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836236(v=office.15)
ms:contentKeyID: 48548461
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1088781
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 55baceac9523400c5e646fbc4c1e7bb411219697
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998588"
---
# <a name="dbenginesetoption-method-dao"></a><span data-ttu-id="4df06-102">DBEngine.SetOption-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="4df06-102">DBEngine.SetOption method (DAO)</span></span>

<span data-ttu-id="4df06-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4df06-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4df06-104">Werte für die Schlüssel des Microsoft Access-Datenbankmoduls werden in der Windows-Registrierung temporär überschrieben (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="4df06-104">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="4df06-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4df06-105">Syntax</span></span>

<span data-ttu-id="4df06-106">*Ausdruck* . SetOption (***Option***, ***Wert***)</span><span class="sxs-lookup"><span data-stu-id="4df06-106">*expression* .SetOption(***Option***, ***Value***)</span></span>

<span data-ttu-id="4df06-107">*Ausdruck* Ein Ausdruck, der ein **DBEngine** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4df06-107">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="4df06-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4df06-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4df06-109">Name</span><span class="sxs-lookup"><span data-stu-id="4df06-109">Name</span></span></p></th>
<th><p><span data-ttu-id="4df06-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="4df06-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="4df06-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4df06-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="4df06-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4df06-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4df06-113"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="4df06-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="4df06-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4df06-114">Required</span></span></p></td>
<td><p><span data-ttu-id="4df06-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="4df06-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="4df06-116">Eine Konstante, wie unter "Hinweise" beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4df06-116">A constant as described in Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4df06-117"><em>Wert</em></span><span class="sxs-lookup"><span data-stu-id="4df06-117"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="4df06-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4df06-118">Required</span></span></p></td>
<td><p><span data-ttu-id="4df06-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4df06-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="4df06-120">Der Wert, den Sie Option festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="4df06-120">The value that you want to set option to.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4df06-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4df06-121">Remarks</span></span>

<span data-ttu-id="4df06-122">Jede Konstante bezieht sich auf den entsprechenden Registrierungsschlüssel im Pfad HKEY\_lokale\_Computer\\SOFTWARE\\Microsoft\\Office\\12.0\\Konnektivitätsmodul für Access\\Module\\(d. h., ACE **DbSharedAsyncDelay** entspricht dem Schlüssel HKEY\_lokale\_Computer\\SOFTWARE\\Microsoft\\Office\\12.0\\Konnektivitätsmodul für Access\\Module\\ACE \\SharedAsyncDelay, usw.).</span><span class="sxs-lookup"><span data-stu-id="4df06-122">Each constant refers to the corresponding registry key in the path HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE (that is, **dbSharedAsyncDelay** corresponds to the key HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE\\SharedAsyncDelay, and so on).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4df06-123">Konstante</span><span class="sxs-lookup"><span data-stu-id="4df06-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="4df06-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4df06-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4df06-125"><strong>dbPageTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="4df06-125"><strong>dbPageTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="4df06-126">Der Schlüssel PageTimeout</span><span class="sxs-lookup"><span data-stu-id="4df06-126">The PageTimeout key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4df06-127"><strong>dbSharedAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="4df06-127"><strong>dbSharedAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="4df06-128">Der Schlüssel SharedAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="4df06-128">The SharedAsyncDelay key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4df06-129"><strong>dbExclusiveAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="4df06-129"><strong>dbExclusiveAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="4df06-130">Der Schlüssel ExclusiveAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="4df06-130">The ExclusiveAsyncDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4df06-131"><strong>dbLockRetry</strong></span><span class="sxs-lookup"><span data-stu-id="4df06-131"><strong>dbLockRetry</strong></span></span></p></td>
<td><p><span data-ttu-id="4df06-132">Der Schlüssel LockRetry</span><span class="sxs-lookup"><span data-stu-id="4df06-132">The LockRetry key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4df06-133"><strong>dbUserCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="4df06-133"><strong>dbUserCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="4df06-134">Der Schlüssel UserCommitSync</span><span class="sxs-lookup"><span data-stu-id="4df06-134">The UserCommitSync key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4df06-135"><strong>dbImplicitCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="4df06-135"><strong>dbImplicitCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="4df06-136">Der Schlüssel ImplicitCommitSync</span><span class="sxs-lookup"><span data-stu-id="4df06-136">The ImplicitCommitSync key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4df06-137"><strong>dbMaxBufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="4df06-137"><strong>dbMaxBufferSize</strong></span></span></p></td>
<td><p><span data-ttu-id="4df06-138">Der Schlüssel MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="4df06-138">The MaxBufferSize key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4df06-139"><strong>dbMaxLocksPerFile</strong></span><span class="sxs-lookup"><span data-stu-id="4df06-139"><strong>dbMaxLocksPerFile</strong></span></span></p></td>
<td><p><span data-ttu-id="4df06-140">Der Schlüssel MaxLocksPerFile</span><span class="sxs-lookup"><span data-stu-id="4df06-140">The MaxLocksPerFile key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4df06-141"><strong>dbLockDelay</strong></span><span class="sxs-lookup"><span data-stu-id="4df06-141"><strong>dbLockDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="4df06-142">Der Schlüssel LockDelay</span><span class="sxs-lookup"><span data-stu-id="4df06-142">The LockDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4df06-143"><strong>dbRecycleLVs</strong></span><span class="sxs-lookup"><span data-stu-id="4df06-143"><strong>dbRecycleLVs</strong></span></span></p></td>
<td><p><span data-ttu-id="4df06-144">Der Schlüssel RecycleLVs</span><span class="sxs-lookup"><span data-stu-id="4df06-144">The RecycleLVs key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4df06-145"><strong>dbFlushTransactionTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="4df06-145"><strong>dbFlushTransactionTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="4df06-146">Der Schlüssel FlushTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="4df06-146">The FlushTransactionTimeout key</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4df06-p101">Mithilfe der **SetOption**-Methode können Sie Registrierungswerte zur Laufzeit überschreiben. Neue Werte, die mit der **SetOption**-Methode erstellt wurden, bleiben gültig, bis sie wieder von einem anderen **SetOption**-Aufruf geändert werden oder bis das **DBEngine**-Objekt geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="4df06-p101">Use the **SetOption** method to override registry values at run-time. New values established with the **SetOption** method remain in effect until changed again by another **SetOption** call, or until the **DBEngine** object is closed.</span></span>

