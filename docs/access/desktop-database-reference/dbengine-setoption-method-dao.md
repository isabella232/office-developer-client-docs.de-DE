---
title: DbEngine. SetOption-Methode (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 5875a8935b1b44c3c36b29344af32df552f6e01c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294197"
---
# <a name="dbenginesetoption-method-dao"></a>DbEngine. SetOption-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Werte für die Schlüssel des Microsoft Access-Datenbankmoduls werden in der Windows-Registrierung temporär überschrieben (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . SetOption (***Option***, ***Wert***)

*Ausdruck* Ein Ausdruck, der ein **DBEngine** -Objekt zurückgibt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Option</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Eine Konstante, wie unter "Hinweise" beschrieben.</p></td>
</tr>
<tr class="even">
<td><p><em>Value</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Der Wert, auf den die Option festgelegt werden soll.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Jede Konstante bezieht sich auf den entsprechenden Registrierungsschlüssel im Pfad\_HKEY\_-\\lokale\\Computer\\Software\\Microsoft\\Office 12,0 Access\\Connectivity\\Engine Engines ACE (d. **dbSharedAsyncDelay** entspricht dem Schlüssel HKEY\_lokale\_Computer\\Software\\Microsoft\\Office\\12,0\\Access Connectivity Engine\\Engines\\ACE \\Schlüssel SharedAsyncDelay usw.).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbPageTimeout</strong></p></td>
<td><p>Der Schlüssel PageTimeout</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSharedAsyncDelay</strong></p></td>
<td><p>Der Schlüssel SharedAsyncDelay</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbExclusiveAsyncDelay</strong></p></td>
<td><p>Der Schlüssel ExclusiveAsyncDelay</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLockRetry</strong></p></td>
<td><p>Der Schlüssel LockRetry</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbUserCommitSync</strong></p></td>
<td><p>Der Schlüssel UserCommitSync</p></td>
</tr>
<tr class="even">
<td><p><strong>dbImplicitCommitSync</strong></p></td>
<td><p>Der Schlüssel ImplicitCommitSync</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbMaxBufferSize</strong></p></td>
<td><p>Der Schlüssel MaxBufferSize</p></td>
</tr>
<tr class="even">
<td><p><strong>dbMaxLocksPerFile</strong></p></td>
<td><p>Der Schlüssel MaxLocksPerFile</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLockDelay</strong></p></td>
<td><p>Der Schlüssel LockDelay</p></td>
</tr>
<tr class="even">
<td><p><strong>dbRecycleLVs</strong></p></td>
<td><p>Der Schlüssel RecycleLVs</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFlushTransactionTimeout</strong></p></td>
<td><p>Der Schlüssel FlushTransactionTimeout</p></td>
</tr>
</tbody>
</table>


Mithilfe der **SetOption**-Methode können Sie Registrierungswerte zur Laufzeit überschreiben. Neue Werte, die mit der **SetOption**-Methode erstellt wurden, bleiben gültig, bis sie wieder von einem anderen **SetOption**-Aufruf geändert werden oder bis das **DBEngine**-Objekt geschlossen wird.

