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
ms.localizationpriority: medium
ms.openlocfilehash: e95e92405d1eac52d7815897f9fe52ceea0b223a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606835"
---
# <a name="dbenginesetoption-method-dao"></a>DBEngine.SetOption-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Werte für die Schlüssel des Microsoft Access-Datenbankmoduls werden in der Windows-Registrierung temporär überschrieben (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . SetOption(***Option** _, _*_Value_**)

*expression* Ein Ausdruck, der ein **DBEngine**-Objekt zurückgibt.

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
<td><p>Der Wert, auf den Sie die Option festlegen möchten.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>HinwBemerkungeneise

Jede Konstante verweist auf den entsprechenden Registrierungsschlüssel im Pfad HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Office \_ \\ \\ \\ \\ 12.0 \\ Access Connectivity Engine Engines ACE \\ \\ (d. h. **dbSharedAsyncDelay** entspricht dem Schlüssel HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Office \_ \\ \\ \\ \\ 12.0 \\ Access Connectivity Engine Engines ACE \\ \\ \\ SharedAsyncDelay usw. on).

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

