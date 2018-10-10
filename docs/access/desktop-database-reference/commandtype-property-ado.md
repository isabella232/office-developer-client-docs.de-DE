---
title: CommandType-Eigenschaft (ADO)
TOCTitle: CommandType Property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3cff3c3540208b142fc13cd79eb83bd218814873
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476115"
---
# <a name="commandtype-property-ado"></a>CommandType-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt den Typ eines [Command](command-object-ado.md)-Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird mindestens ein [CommandTypeEnum](commandtypeenum.md)-Wert festgelegt oder zurückgegeben.


> [!NOTE]
> <P>[!HINWEIS] Verwenden Sie die <STRONG>CommandTypeEnum</STRONG> -Werte von <STRONG>adCmdFile</STRONG> oder <STRONG>adCmdTableDirect</STRONG> nicht zusammen mit <STRONG>CommandType</STRONG>. Diese Werte können nur als Optionen für die Methoden <A href="open-method-ado-recordset.md">Open</A> und <A href="requery-method-ado.md">Requery</A> eines <A href="recordset-object-ado.md">Recordset</A>-Objekts verwendet werden.</P>



## <a name="remarks"></a>Hinweise

Verwenden Sie die **CommandType** -Eigenschaft zum Optimieren der Evaluierung der [CommandText](commandtext-property-ado.md)-Eigenschaft.

Wenn der Wert der **CommandType** -Eigenschaft gleich **adCmdUnknown** ist (Standardwert), kann die Leistung beeinträchtigt sein. ADO muss dann nämlich den Anbieter aufrufen, um zu ermitteln, ob es sich bei der **CommandText** -Eigenschaft um eine SQL-Anweisung, eine gespeicherte Prozedur oder einen Tabellennamen handelt. Falls Sie wissen, welchen Befehlstyp Sie verwenden, wird ADO durch Festlegen der **CommandType** -Eigenschaft angewiesen, direkt zum entsprechenden Code zu wechseln. Wenn die **CommandType** -Eigenschaft nicht mit dem Befehlstyp in der **CommandText** -Eigenschaft übereinstimmt, tritt beim Aufrufen der [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\))-Methode ein Fehler auf.

