---
title: ActualSize-Eigenschaft (ADO)
TOCTitle: ActualSize property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c13cb41299ddaf786e6412e43a50b1414ad818b4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698204"
---
# <a name="actualsize-property-ado"></a>ActualSize-Eigenschaft (ADO)

**Betrifft**: Access 2013, Office 2013

Gibt die tatsächliche Länge des Werts eines Felds an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Gibt einen Wert vom Datentyp Long zurück. Für einige Anbieter kann diese Eigenschaft festgelegt werden, um Speicherplatz für BLOB-Daten zu reservieren. In diesem Fall lautet der Standardwert 0.

## <a name="remarks"></a>Hinweise

Mithilfe der **ActualSize** -Eigenschaft geben Sie die tatsächliche Länge des Werts eines [Field](field-object-ado.md)-Objekts zurück. Die **ActualSize** -Eigenschaft ist für alle Felder schreibgeschützt. Falls ADO die Länge des Werts für das **Field** -Objekt nicht bestimmen kann, wird **adUnknown** von der **ActualSize** -Eigenschaft zurückgegeben.

**ActualSize-** und [DefinedSize](definedsize-property-ado.md) -Eigenschaften sind unterschiedlich. Ein **Field** -Objekt mit dem deklarierten Typ **AdVarChar** und einer maximalen Länge von 50 Zeichen gibt zurück **DefinedSize** -Eigenschaft den Wert 50, aber des Werts der **ActualSize** -Eigenschaft gibt die Länge des Datenversion, die in das Feld für die Aktueller Datensatz. **Felder** mit einem **DefinedSize** größer als 255 Bytes als Spalten mit variabler Länge behandelt werden.

