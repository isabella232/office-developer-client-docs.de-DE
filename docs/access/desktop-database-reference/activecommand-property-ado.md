---
title: ActiveCommand-Eigenschaft (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18fa38176f7174f27b46604c6182dfbdaa422f06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281929"
---
# <a name="activecommand-property-ado"></a>ActiveCommand-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Gibt das [Command](command-object-ado.md)-Objekt an, mit dem das zugeordnete [Recordset](recordset-object-ado.md)-Objekt erstellt wurde.

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert vom Datentyp **Variant** zurück, der ein **Command**-Objekt enthält. Der Standard ist ein nullwertiger Objektverweis.

## <a name="remarks"></a>Bemerkungen

Die **ActiveCommand**-Eigenschaft ist schreibgeschützt.

Wenn kein **Command** -Objekt zum Erstellen des aktuellen **Recordset**-Objekts verwendet wurde, wird ein **null** -Objektverweis zurückgegeben.

Suchen Sie mit dieser Eigenschaft das zugeordnete **Command**-Objekt, wenn nur das resultierende **Recordset**-Objekt angegeben ist.

