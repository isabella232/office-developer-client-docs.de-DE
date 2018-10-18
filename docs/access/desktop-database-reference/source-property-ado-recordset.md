---
title: Source-Eigenschaft (ADO-Recordset)
TOCTitle: Source Property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db44459bf3629f6cedfbee023b0be9161ed3bb14
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605261"
---
# <a name="source-property-ado-recordset"></a>Source-Eigenschaft (ADO-Recordset)


**Betrifft**: Access 2013 | Office 2013

Gibt die Datenquelle für ein [Recordset](recordset-object-ado.md)-Objekt an.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Legt einen **String** -Wert oder einen [Command](command-object-ado.md)-Objektverweis fest; gibt nur einen **String** -Wert zurück, der die Quelle des **Recordset** -Objekts angibt.

## <a name="remarks"></a>Hinweise

Geben Sie mit der **Source** -Eigenschaft die Datenquelle für ein **Recordset** -Objekt an, und verwenden Sie dazu Folgendes: eine **Command** -Objektvariable, eine SQL-Anweisung, eine gespeicherte Prozedur oder einen Tabellennamen.

Wenn Sie die **Source** -Eigenschaft für ein **Command** -Objekt festlegen, erbt die [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft des **Recordset** -Objekts den Wert der **ActiveConnection** -Eigenschaft, die für das **Command** -Objekt angegeben wurde. Beim Lesen der **Source** -Eigenschaft wird jedoch kein **Command** -Objekt zurückgegeben. Stattdessen wird die [CommandText](commandtext-property-ado.md)-Eigenschaft des **Command** -Objekts zurückgegeben, für die Sie die **Source** -Eigenschaft festgelegt haben.

Wenn die **Source** -Eigenschaft eine SQL-Anweisung, eine gespeicherte Prozedur oder ein Tabellenname ist, können Sie Leistung zu optimieren, indem Sie das entsprechende Argument *Options* durch den Aufruf der [Open](open-method-ado-recordset.md) -Methode übergeben.

Die **Source** -Eigenschaft ist bei geschlossenen **Recordset** -Objekten nicht schreibgeschützt und bei geöffneten **Recordset** -Objekten schreibgeschützt.

