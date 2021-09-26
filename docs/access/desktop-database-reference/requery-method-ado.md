---
title: Requery-Methode (ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 65b1b69bc8b8bbeb46cace80a810849a5e5b3401
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631769"
---
# <a name="requery-method-ado"></a>Requery-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Die Daten in einem [Recordset](recordset-object-ado.md)-Objekt werden aktualisiert durch erneutes Ausführen der Abfrage, auf der das Objekt basiert.

## <a name="syntax"></a>Syntax

*Recordset*. *Requery-Optionen*

## <a name="parameters"></a>Parameter

|Name |Beschreibung|
|:----|:----------|
|*Optionen* |Optional. Eine Bitmaske, die die Werte [ExecuteOptionEnum](executeoptionenum.md) und [CommandTypeEnum](commandtypeenum.md) enthält, die sich auf diese Operation auswirken.|

> [!NOTE]
> Wenn *Options* auf **adAsyncExecute** festgelegt ist, wird dieser Vorgang asynchron ausgeführt, und ein [RecordsetChangeComplete-Ereignis](willchangerecordset-and-recordsetchangecomplete-events-ado.md) wird ausgegeben, wenn er beendet wird.

Die **ExecuteOpenEnum**-Werte von **adExecuteNoRecords** oder **adExecuteStream** sollten nicht mit **Requery** verwendet werden.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Requery**-Methode zum Aktualisieren des gesamten Inhalts eines **Recordset**-Objekts über die Datenquelle, indem Sie den ursprünglichen Befehl erneut ausgeben und die Daten ein zweites Mal abrufen. Das Aufrufen dieser Methode entspricht dem aufeinander folgenden Aufrufen der Methoden [Close](close-method-ado.md) und [Open](open-method-ado-recordset.md). Wenn Sie den aktuellen Datensatz bearbeiten oder einen neuen Datensatz hinzufügen, tritt ein Fehler auf.

Während das **Recordset**-Objekt geöffnet ist, sind die Eigenschaften, durch die der Cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md) usw.) definiert wird, schreibgeschützt. Daher kann durch die **Requery**-Methode nur der aktuelle Cursor aktualisiert werden. Zum Ändern der Cursoreigenschaften und zum Anzeigen der Ergebnisse müssen Sie die [Close](close-method-ado.md)-Methode verwenden, damit wieder der Lese- und Schreibzugriff auf die Eigenschaften möglich ist. Dann können Sie die Eigenschaftseinstellungen ändern und die [Open](open-method-ado-recordset.md)-Methode aufrufen, um den Cursor erneut zu öffnen.

