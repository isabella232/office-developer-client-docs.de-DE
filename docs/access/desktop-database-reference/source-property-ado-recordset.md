---
title: Source-Eigenschaft (ADO-Recordset)
TOCTitle: Source property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: aa6ef3bb28fbd9a4c44d45f1e503ab14021c8b9f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568404"
---
# <a name="source-property-ado-recordset"></a>Source-Eigenschaft (ADO-Recordset)


**Gilt für**: Access 2013, Office 2013

Gibt die Datenquelle für ein [Recordset](recordset-object-ado.md)-Objekt an.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Legt einen **String**-Wert oder einen [Command](command-object-ado.md)-Objektverweis fest; gibt nur einen **String**-Wert zurück, der die Quelle des **Recordset**-Objekts angibt.

## <a name="remarks"></a>HinwBemerkungeneise

Geben Sie mit der **Source**-Eigenschaft die Datenquelle für ein **Recordset**-Objekt an, und verwenden Sie dazu Folgendes: eine **Command**-Objektvariable, eine SQL-Anweisung, eine gespeicherte Prozedur oder einen Tabellennamen.

Wenn Sie die **Source**-Eigenschaft für ein **Command**-Objekt festlegen, erbt die [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft des **Recordset**-Objekts den Wert der **ActiveConnection**-Eigenschaft, die für das **Command**-Objekt angegeben wurde. Beim Lesen der **Source**-Eigenschaft wird jedoch kein **Command**-Objekt zurückgegeben. Stattdessen wird die [CommandText](commandtext-property-ado.md)-Eigenschaft des **Command**-Objekts zurückgegeben, für die Sie die **Source**-Eigenschaft festgelegt haben.

Wenn die **Source**-Eigenschaft eine SQL-Anweisung, eine gespeicherte Prozedur oder ein Tabellenname ist, können Sie die Leistung optimieren, indem Sie das entsprechende Argument *Options* durch den [Open](open-method-ado-recordset.md)-Methodenaufruf übergeben.

Die **Source**-Eigenschaft ist bei geschlossenen **Recordset**-Objekten nicht schreibgeschützt und bei geöffneten **Recordset**-Objekten schreibgeschützt.

