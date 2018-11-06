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
# <a name="dbenginesetoption-method-dao"></a>DBEngine.SetOption-Methode (DAO)

**Betrifft**: Access 2013, Office 2013

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
<th><p>Erforderlich oder optional</p></th>
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
<td><p><em>Wert</em></p></td>
<td><p>Erforderlich</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Der Wert, den Sie Option festlegen möchten.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Jede Konstante bezieht sich auf den entsprechenden Registrierungsschlüssel im Pfad HKEY\_lokale\_Computer\\SOFTWARE\\Microsoft\\Office\\12.0\\Konnektivitätsmodul für Access\\Module\\(d. h., ACE **DbSharedAsyncDelay** entspricht dem Schlüssel HKEY\_lokale\_Computer\\SOFTWARE\\Microsoft\\Office\\12.0\\Konnektivitätsmodul für Access\\Module\\ACE \\SharedAsyncDelay, usw.).

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

