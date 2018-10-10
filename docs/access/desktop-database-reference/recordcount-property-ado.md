---
title: RecordCount-Eigenschaft (ADO)
TOCTitle: RecordCount Property (ADO)
ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15)
ms:contentKeyID: 48548304
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a619570264973fc70b7cc5bd581437a4002b00be
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475481"
---
# <a name="recordcount-property-ado"></a>RecordCount-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt die Anzahl von Datensätzen in einem [Recordset](recordset-object-ado.md)-Objekt an.

## <a name="return-value"></a>Rückgabewert

Gibt einen **Long** -Wert zurück, der die Anzahl von Datensätzen im **Recordset** -Objekt angibt.

## <a name="remarks"></a>Hinweise

Ermitteln Sie mit der **RecordCount** -Eigenschaft die Anzahl von Datensätzen in einem **Recordset** -Objekt. Die Eigenschaft gibt -1 zurück, wenn ADO die Anzahl von Datensätzen nicht bestimmen kann oder wenn der Anbieter- oder Cursortyp **RecordCount** nicht unterstützt. Das Lesen der **RecordCount** -Eigenschaft für ein geschlossenes **Recordset** -Objekt verursacht einen Fehler.

Wenn das **Recordset** -Objekt eine ungefähre Positionierung von Textmarken zulässt (d. h. **Supports (adApproxPosition)** oder **Supports (adBookmark)** geben jeweils **True** zurück), entspricht dieser Wert genau der Anzahl von Datensätzen im **Recordset** -Objekt, unabhängig davon, ob es vollständig gefüllt ist. Unterstützt das **Recordset** -Objekt keine ungefähre Positionierung, kann diese Eigenschaften die Ressourcen erheblich beeinträchtigen. Denn es müssen alle Datensätze abgerufen und gezählt werden, damit einen präziser **RecordCount** -Wert zurückgegeben wird.

Der Cursortyp des **Recordset** -Objekts beeinflusst die Anzahl von Datensätzen, die ermittelt werden können. Die **RecordCount** -Eigenschaft gibt -1 für einen Vorwärtscursor zurück; die tatsächliche Anzahl für einen statischen oder einen Keyset-Cursor; und je nach Datenquelle entweder -1 oder die tatsächliche Anzahl für einen dynamischen Cursor.

