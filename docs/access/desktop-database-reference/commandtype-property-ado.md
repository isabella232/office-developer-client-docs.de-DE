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
ms.localizationpriority: medium
ms.openlocfilehash: d15a06aa1d979de14f01b7c47f4bb986572a9652
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569391"
---
# <a name="commandtype-property-ado"></a>CommandType-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt den Typ eines [Command](command-object-ado.md)-Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird mindestens ein [CommandTypeEnum](commandtypeenum.md)-Wert festgelegt oder zurückgegeben.

> [!NOTE]
> [!HINWEIS] Verwenden Sie die **CommandTypeEnum** -Werte von **adCmdFile** oder **adCmdTableDirect** nicht zusammen mit **CommandType**. Diese Werte können nur als Optionen für die Methoden [Open](open-method-ado-recordset.md) und [Requery](requery-method-ado.md) eines [Recordset](recordset-object-ado.md)-Objekts verwendet werden.


## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **CommandType** -Eigenschaft zum Optimieren der Evaluierung der [CommandText](commandtext-property-ado.md)-Eigenschaft.

Wenn der Wert der **CommandType** -Eigenschaft gleich **adCmdUnknown** ist (Standardwert), kann die Leistung beeinträchtigt sein. ADO muss dann nämlich den Anbieter aufrufen, um zu ermitteln, ob es sich bei der **CommandText** -Eigenschaft um eine SQL-Anweisung, eine gespeicherte Prozedur oder einen Tabellennamen handelt. Falls Sie wissen, welchen Befehlstyp Sie verwenden, wird ADO durch Festlegen der **CommandType** -Eigenschaft angewiesen, direkt zum entsprechenden Code zu wechseln. Wenn die **CommandType** -Eigenschaft nicht mit dem Befehlstyp in der **CommandText** -Eigenschaft übereinstimmt, tritt beim Aufrufen der [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)-Methode ein Fehler auf.

