---
title: Source-Eigenschaft (ADO-Recordset)
TOCTitle: Source property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a58ac3c5315daef040ba6a999753a19f76504087
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947570"
---
# <a name="source-property-ado-recordset"></a>Source-Eigenschaft (ADO-Recordset)


**Betrifft**: Access 2013, Office 2013

Gibt die Datenquelle für ein [Recordset](recordset-object-ado.md)-Objekt an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **String** -Wert oder einen [Command](command-object-ado.md)-Objektverweis fest; gibt nur einen **String** -Wert zurück, der die Quelle des **Recordset** -Objekts angibt.

## <a name="remarks"></a>Hinweise

Geben Sie mit der **Source** -Eigenschaft die Datenquelle für ein **Recordset** -Objekt an, und verwenden Sie dazu Folgendes: eine **Command** -Objektvariable, eine SQL-Anweisung, eine gespeicherte Prozedur oder einen Tabellennamen.

Wenn Sie die **Source** -Eigenschaft für ein **Command** -Objekt festlegen, erbt die [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft des **Recordset** -Objekts den Wert der **ActiveConnection** -Eigenschaft, die für das **Command** -Objekt angegeben wurde. Beim Lesen der **Source** -Eigenschaft wird jedoch kein **Command** -Objekt zurückgegeben. Stattdessen wird die [CommandText](commandtext-property-ado.md)-Eigenschaft des **Command** -Objekts zurückgegeben, für die Sie die **Source** -Eigenschaft festgelegt haben.

Wenn die **Source** -Eigenschaft eine SQL-Anweisung, eine gespeicherte Prozedur oder ein Tabellenname ist, können Sie Leistung zu optimieren, indem Sie das entsprechende Argument *Options* durch den Aufruf der [Open](open-method-ado-recordset.md) -Methode übergeben.

Die **Source** -Eigenschaft ist bei geschlossenen **Recordset** -Objekten nicht schreibgeschützt und bei geöffneten **Recordset** -Objekten schreibgeschützt.

