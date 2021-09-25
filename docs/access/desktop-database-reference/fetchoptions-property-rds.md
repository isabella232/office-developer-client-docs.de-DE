---
title: FetchOptions-Eigenschaft (RDS)
TOCTitle: FetchOptions property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: aa5bdd448cc46e2b665c85d8aff9b79d1c5e81e9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558338"
---
# <a name="fetchoptions-property-rds"></a>FetchOptions-Eigenschaft (RDS)


**Gilt für**: Access 2013, Office 2013

Gibt den Typ für asynchrone Abrufvorgänge an.

## <a name="setting-and-return-values"></a>Einstellung und Rückgabewert

Legt einen der folgenden Werte fest oder gibt ihn zurück.

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
<td><p><strong>adcFetchUpFront</strong></p></td>
<td><p>Alle Datensätze des <a href="recordset-object-ado.md">Recordsets</a> werden abgerufen, bevor die Steuerung an die Anwendung zurückgeht. Erst nachdem das vollständige <strong>Recordset</strong>-Objekt abgerufen wurde, kann es durch die Anwendung bearbeitet werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcFetchBackground</strong></p></td>
<td><p>Nachdem der erste Datensatzbatch abgerufen wurde, kann die Steuerung wieder an die Anwendung zurückgehen. Ein anschließender Lesevorgang des <strong>Recordsets</strong>, bei dem versucht wird, auf einen im ersten Batch noch nicht abgerufenen Datensatz zuzugreifen, wird verzögert, bis der gesuchte Datensatz tatsächlich abgerufen wurde. Dann geht die Steuerung wieder an die Anwendung zurück.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcFetchAsync</strong></p></td>
<td><p>Standard. Die Steuerung geht sofort an die Anwendung zurück, während Datensätze im Hintergrund abgerufen werden. Wenn von der Anwendung versucht wird, einen Datensatz zu lesen, der noch nicht abgerufen wurde, wird der Datensatz gelesen, der dem gesuchten Datensatz am nächsten liegt. Dabei geht die Steuerung sofort an die Anwendung zurück, und es wird angegeben, dass das aktuelle Ende des <strong>Recordsets</strong> erreicht ist. Beispielsweise wird bei einem Aufruf von <a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveLast</a> die aktuelle Datensatzposition zum tatsächlich zuletzt abgerufenen Datensatz verschoben, auch wenn das <strong>Recordset</strong>-Objekt mit weiteren Datensätzen gefüllt wird.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.



## <a name="remarks"></a>HinwBemerkungeneise

In einer Webanwendung sollten Sie in der Regel **adcFetchAsync** (Standardwert) verwenden, da es eine bessere Leistung bietet. In einer kompilierten Clientanwendung wird meist **adcFetchBackground** verwendet.

