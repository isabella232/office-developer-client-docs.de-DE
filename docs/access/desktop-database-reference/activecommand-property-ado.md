---
title: ActiveCommand-Eigenschaft (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 473a0b99310d2eb5e050ed50f1e331cb65174ae8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869561"
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

