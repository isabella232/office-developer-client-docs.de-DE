---
title: RecordCount-Eigenschaft (ADO)
TOCTitle: RecordCount property (ADO)
ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15)
ms:contentKeyID: 48548304
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d5ab01c419f703c1c17b1bf2b2cca2fb3844655d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300770"
---
# <a name="recordcount-property-ado"></a>RecordCount-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt die Anzahl von Datensätzen in einem [Recordset](recordset-object-ado.md)-Objekt an.

## <a name="return-value"></a>Rückgabewert

Gibt einen **Long**-Wert zurück, der die Anzahl von Datensätzen im **Recordset**-Objekt angibt.

## <a name="remarks"></a>Bemerkungen

Ermitteln Sie mit der **RecordCount** -Eigenschaft die Anzahl von Datensätzen in einem **Recordset** -Objekt. Die Eigenschaft gibt -1 zurück, wenn ADO die Anzahl von Datensätzen nicht bestimmen kann oder wenn der Anbieter- oder Cursortyp **RecordCount** nicht unterstützt. Das Lesen der **RecordCount** -Eigenschaft für ein geschlossenes **Recordset** -Objekt verursacht einen Fehler.

Wenn das **Recordset** -Objekt eine ungefähre Positionierung von Textmarken zulässt (d. h. **Supports (adApproxPosition)** oder **Supports (adBookmark)** geben jeweils **True** zurück), entspricht dieser Wert genau der Anzahl von Datensätzen im **Recordset** -Objekt, unabhängig davon, ob es vollständig gefüllt ist. Unterstützt das **Recordset** -Objekt keine ungefähre Positionierung, kann diese Eigenschaften die Ressourcen erheblich beeinträchtigen. Denn es müssen alle Datensätze abgerufen und gezählt werden, damit einen präziser **RecordCount** -Wert zurückgegeben wird.

Der Cursortyp des **Recordset**-Objekts beeinflusst die Anzahl von Datensätzen, die ermittelt werden können. Die **RecordCount**-Eigenschaft gibt -1 für einen Vorwärtscursor zurück; die tatsächliche Anzahl für einen statischen oder einen Keyset-Cursor; und je nach Datenquelle entweder -1 oder die tatsächliche Anzahl für einen dynamischen Cursor.

