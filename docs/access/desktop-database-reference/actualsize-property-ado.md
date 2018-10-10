---
title: ActualSize-Eigenschaft (ADO)
TOCTitle: ActualSize Property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d0fa7b4f5fe27c25db51338dd1dfd1a68a936364
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472654"
---
# <a name="actualsize-property-ado"></a>ActualSize-Eigenschaft (ADO)

**Betrifft**: Access 2013 | Office 2013

Gibt die tatsächliche Länge des Werts eines Felds an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Gibt einen Wert vom Datentyp Long zurück. Für einige Anbieter kann diese Eigenschaft festgelegt werden, um Speicherplatz für BLOB-Daten zu reservieren. In diesem Fall lautet der Standardwert 0.

## <a name="remarks"></a>Hinweise

Mithilfe der **ActualSize** -Eigenschaft geben Sie die tatsächliche Länge des Werts eines [Field](field-object-ado.md)-Objekts zurück. Die **ActualSize** -Eigenschaft ist für alle Felder schreibgeschützt. Falls ADO die Länge des Werts für das **Field** -Objekt nicht bestimmen kann, wird **adUnknown** von der **ActualSize** -Eigenschaft zurückgegeben.

Die Eigenschaften ActualSize und DefinedSize unterscheiden sich, wie im folgenden Beispiel A dargestellt. Ein Field-Objekt mit dem deklarierten Typ adVarChar und einer maximalen Länge von 50 Zeichen gibt den Wert 50 für die DefinedSize-Eigenschaft zurück, aber der für die ActualSize-Eigenschaft zurückgegebene Wert ist die Länge der Daten, die im Feld für den aktuellen Datensatz gespeichert sind. Field-Objekte, deren DefinedSize-Eigenschaft größer als 255 Bytes ist, werden als Spalten mit variabler Länge behandelt.

