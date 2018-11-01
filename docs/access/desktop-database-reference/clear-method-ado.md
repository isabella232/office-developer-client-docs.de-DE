---
title: "\"Clear\"-Methode - ActiveX Data Objects (ADO)"
TOCTitle: Clear Method (ADO)
ms:assetid: 5d51f42c-147b-1fcf-d05b-123e5714ecb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249329(v=office.15)
ms:contentKeyID: 48545110
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 864c31a75514b4e8c56383672b196a4e62c4ec8f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876785"
---
# <a name="clear-method-ado"></a>Clear-Methode (ADO)


**Betrifft**: Access 2013, Office 2013

Alle **Error** -Objekte werden aus der **Errors** -Auflistung entfernt.

## <a name="syntax"></a>Syntax

*Fehler*. Löschen

## <a name="remarks"></a>Hinweise

Verwenden Sie die **Clear** -Methode für die [Errors](errors-collection-ado.md)-Auflistung, um alle vorhandenen [Error](error-object-ado.md)-Objekte aus der Auflistung zu entfernen. Wenn ein Fehler auftritt, wird die **Errors** -Auflistung automatisch von ADO gelöscht und mit auf dem neuen Fehler basierenden **Error** -Objekten gefüllt.

Von manchen Eigenschaften und Methoden werden Warnungen zurückgegeben, die als **Error** -Objekte in der **Errors** -Auflistung angezeigt werden, ohne dass die Ausführung eines Programms angehalten wird. Rufen Sie vor dem Aufrufen der Methoden [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) oder [CancelBatch](cancelbatch-method-ado.md) für ein [Recordset](recordset-object-ado.md)-Objekt oder der [Open](open-method-ado-connection.md)-Methode für ein [Connection](connection-object-ado.md)-Objekt oder vor dem Festlegen der [Filter](filter-property-ado.md)-Eigenschaft für ein **Recordset** -Objekt die **Clear** -Methode für die **Errors** -Auflistung auf. Auf diese Weise können Sie die [Count](count-property-ado.md)-Eigenschaft der **Errors** -Auflistung lesen, um auf zurückgegebene Warnungen zu testen.

