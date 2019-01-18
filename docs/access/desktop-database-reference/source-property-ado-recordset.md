---
title: Source-Eigenschaft (ADO-Recordset)
TOCTitle: Source property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26f41181f1233931f24ff091b3009dfa7a5d6ff3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708102"
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

