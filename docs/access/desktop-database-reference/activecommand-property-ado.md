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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705295"
---
# <a name="activecommand-property-ado"></a>ActiveCommand-Eigenschaft (ADO)

**Betrifft**: Access 2013, Office 2013

Gibt das [Command](command-object-ado.md)-Objekt an, mit dem das zugeordnete [Recordset](recordset-object-ado.md)-Objekt erstellt wurde.

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert vom Datentyp **Variant** zurück, der ein **Command** -Objekt enthält. Der Standard ist ein nullwertiger Objektverweis.

## <a name="remarks"></a>Hinweise

Die **ActiveCommand** -Eigenschaft ist schreibgeschützt.

Wenn ein **Command** -Objekt zum Erstellen des aktuellen **Recordset-Objekt**nicht verwendet wurde, wird ein **Null** -Objektverweis zurückgegeben.

Suchen Sie mit dieser Eigenschaft das zugeordnete **Command** -Objekt, wenn nur das resultierende **Recordset** -Objekt angegeben ist.

