---
title: OriginalValue-Eigenschaft (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0724320e1aaa1e7bfd3ceab8cf54afd5921c7425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288182"
---
# <a name="originalvalue-property-ado"></a>OriginalValue-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Gibt den Wert eines [Felds](field-object-ado.md) im Datensatz an, bevor Änderungen vorgenommen wurden.

## <a name="return-value"></a>Rückgabewert

Gibt einen **Variant**-Wert zurück, der den Wert eines Felds vor einer Änderung darstellt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **OriginalValue**-Eigenschaft, um den ursprünglichen Wert eines Felds aus dem aktuellen Datensatz zurückzugeben.

Im *sofortigen Aktualisierungsmodus* (in dem der Anbieter Änderungen an der zugrunde liegenden Datenquelle schreibt, nachdem Sie die [Update](update-method-ado.md) -Methode aufgerufen haben), gibt die **OriginalValue** -Eigenschaft den Feldwert zurück, der vor Änderungen vorhanden war (das heißt, da der Aufruf der letzten **Update** -Methode). Dabei handelt es sich um denselben Wert, der in der [CancelUpdate](cancelupdate-method-ado.md)-Methode dazu verwendet wird, den Wert der [Value](value-property-ado.md)-Eigenschaft zu ersetzen.

Im *Batchaktualisierungsmodus* (in dem der Anbieter mehrere Änderungen zwischenspeichert und erst in die zugrunde liegende Datenquelle schreibt, wenn Sie die [UpdateBatch](updatebatch-method-ado.md)-Methode aufrufen) gibt die **OriginalValue**-Eigenschaft den Feldwert zurück, der vor Änderungen vorhanden war (d. h. seit dem letzten Aufruf der **UpdateBatch**-Methode). Dabei handelt es sich um denselben Wert, der bei der [CancelBatch](cancelbatch-method-ado.md)-Methode zum Ersetzen der **Value**-Eigenschaft verwendet wird. Wenn Sie diese Eigenschaft in Verbindung mit der [OriginalValue](underlyingvalue-property-ado.md)-Eigenschaft verwenden, können Sie Konflikte lösen, die durch Batchaktualisierungen auftreten.

## <a name="record"></a>Aufzeichnen

Bei [Record](record-object-ado.md)-Objekten ist die **OriginalValue**-Eigenschaft für Felder leer, die vor dem Aufruf der [Update](update-method-ado.md)-Methode hinzugefügt wurden.

