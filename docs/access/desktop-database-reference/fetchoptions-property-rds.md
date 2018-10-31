---
title: FetchOptions-Eigenschaft (RDS)
TOCTitle: FetchOptions Property (RDS)
ms:assetid: 0d86c5e4-9abc-5c0e-dc04-4183f4c278cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248856(v=office.15)
ms:contentKeyID: 48543221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3e7251ba50b003b37cdeb0dd70fe4a98821d4c9
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861932"
---
# <a name="fetchoptions-property-rds"></a>FetchOptions-Eigenschaft (RDS)


**Betrifft**: Access 2013 | Office 2013

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
> Jede mithilfe der clientseitigen ausführbare Datei, die die folgenden Konstanten verwendet, muss Deklarationen bereitstellen. Sie können Ausschneiden und Einfügen aus der Datei Datei Adcvbs.inc, befindet sich im Ordner C:\Program Files\Common Dateien\System\MSADC gewünschten Konstantendeklarationen.



## <a name="remarks"></a>Hinweise

<<<<<<< HEAD In a Web Application, Sie werden in der Regel **AdcFetchAsync** (Standardwert) verwenden möchten, da es sich um eine bessere Leistung bietet. In einer kompilierten Clientanwendung wird meist **adcFetchBackground** verwendet.
=== In einer Webanwendung werden Sie in der Regel **AdcFetchAsync** (Standardwert) verwenden möchten, da es sich um eine bessere Leistung bietet. In einer kompilierten Clientanwendung wird meist **adcFetchBackground** verwendet.
>>>>>>> master

