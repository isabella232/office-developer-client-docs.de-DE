---
title: CommandType-Eigenschaft (ADO)
TOCTitle: CommandType property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 89264889281070b8a477c3a04b8f6f5735efdf3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880236"
---
# <a name="commandtype-property-ado"></a>CommandType-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt den Typ eines [Command](command-object-ado.md)-Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird mindestens ein [CommandTypeEnum](commandtypeenum.md)-Wert festgelegt oder zurückgegeben.

> [!NOTE]
> [!HINWEIS] Verwenden Sie die **CommandTypeEnum** -Werte von **adCmdFile** oder **adCmdTableDirect** nicht zusammen mit **CommandType**. Diese Werte können nur als Optionen für die Methoden [Open](open-method-ado-recordset.md) und [Requery](requery-method-ado.md) eines [Recordset](recordset-object-ado.md)-Objekts verwendet werden.


## <a name="remarks"></a>Hinweise

Verwenden Sie die **CommandType** -Eigenschaft zum Optimieren der Evaluierung der [CommandText](commandtext-property-ado.md)-Eigenschaft.

Wenn der Wert der **CommandType** -Eigenschaft gleich **adCmdUnknown** ist (Standardwert), kann die Leistung beeinträchtigt sein. ADO muss dann nämlich den Anbieter aufrufen, um zu ermitteln, ob es sich bei der **CommandText** -Eigenschaft um eine SQL-Anweisung, eine gespeicherte Prozedur oder einen Tabellennamen handelt. Falls Sie wissen, welchen Befehlstyp Sie verwenden, wird ADO durch Festlegen der **CommandType** -Eigenschaft angewiesen, direkt zum entsprechenden Code zu wechseln. Wenn die **CommandType** -Eigenschaft nicht mit dem Befehlstyp in der **CommandText** -Eigenschaft übereinstimmt, tritt beim Aufrufen der [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)-Methode ein Fehler auf.

