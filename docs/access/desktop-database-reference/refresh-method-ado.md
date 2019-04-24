---
title: Refresh-Methode (ADO)
TOCTitle: Refresh method (ADO)
ms:assetid: f1c8829f-9c7d-12b6-7470-727ff38d663e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250227(v=office.15)
ms:contentKeyID: 48548631
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bd7c47e7c3e41a7b42571043cfafc9e4e909a9f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309256"
---
# <a name="refresh-method-ado"></a>Refresh-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Die Objekte in einer Auflistung werden aktualisiert, um Objekte widerzuspiegeln, die vom Anbieter verfügbar sind und spezifisch für diesen sind.

## <a name="syntax"></a>Syntax

*Sammlung*. Aktualisieren

## <a name="remarks"></a>Bemerkungen

Abhängig von der Auflistung, aus der Sie die **Refresh**-Methode aufrufen, werden unterschiedliche Tasks ausgeführt.

## <a name="parameters"></a>Parameter

Durch Verwenden der **Refresh**-Methode für die [Parameters](parameters-collection-ado.md)-Auflistung eines [Command](command-object-ado.md)-Objekts werden anbieterseitige Parameterinformationen für die im **Command**-Objekt angegebene gespeicherte Prozedur oder parametrisierte Abfrage abgerufen. Für Anbieter, die Aufrufe gespeicherter Prozeduren oder parametrisierte Abfragen nicht unterstützen, ist die Auflistung leer.

Legen Sie die [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft des **Command** -Objekts auf ein gültiges [Connection](connection-object-ado.md)-Objekt, die [CommandText](commandtext-property-ado.md)-Eigenschaft auf einen gültigen Befehl und die [CommandType](commandtype-property-ado.md)-Eigenschaft auf **adCmdStoredProc** fest, bevor Sie die **Refresh** -Methode aufrufen.

Wenn Sie vor dem Aufrufen der **Refresh**-Methode auf die **Parameters**-Auflistung zugreifen, wird die Methode automatisch von ADO aufgerufen, und die Auflistung wird aufgefüllt.

> [!NOTE]
> If you use the **Refresh** method to obtain parameter information from the provider and it returns one or more variable-length data type [Parameter](parameter-object-ado.md) objects, ADO may allocate memory for the parameters based on their maximum potential size, which will cause an error during execution. You should explicitly set the [Size](size-property-ado.md) property for these parameters before calling the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method to prevent errors.

### <a name="fields"></a>Fields

Das Verwenden der **Refresh**-Methode für die **Fields**-Auflistung hat keine sichtbare Auswirkung. Zum Abrufen von Änderungen aus der zugrunde liegenden Datenbankstruktur müssen Sie entweder die [Requery](requery-method-ado.md)-Methode oder, wenn Textmarken vom [Recordset](recordset-object-ado.md)-Objekt nicht unterstützt werden, die [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Methode verwenden.

### <a name="properties"></a>Eigenschaften

Durch Verwenden der **Refresh**-Methode für eine **Properties**-Auflistung mancher Objekte wird die Auflistung mit den vom Anbieter verfügbar gemachten dynamischen Eigenschaften aufgefüllt. Durch diese Eigenschaften werden Informationen zu anbieterspezifischer Funktionalität bereitgestellt, die über die von ADO unterstützten integrierten Eigenschaften hinausgeht.

