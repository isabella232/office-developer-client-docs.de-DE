---
title: ActiveCommand-Eigenschaft (ADO)
TOCTitle: ActiveCommand Property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f01ae4c821d8beb6c8de84c7ed671a373d7372c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475521"
---
# <a name="activecommand-property-ado"></a>ActiveCommand-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt das [Command](command-object-ado.md)-Objekt an, mit dem das zugeordnete [Recordset](recordset-object-ado.md)-Objekt erstellt wurde.

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert vom Datentyp **Variant** zurück, der ein **Command** -Objekt enthält. Der Standard ist ein nullwertiger Objektverweis.

## <a name="remarks"></a>Hinweise

Die **ActiveCommand** -Eigenschaft ist schreibgeschützt.

Wenn kein **Command** -Objekt zum Erstellen des aktuellen **Recordset** -Objekts verwendet wurde, wird ein **NULL** -Objektverweis zurückgegeben.

Suchen Sie mit dieser Eigenschaft das zugeordnete **Command** -Objekt, wenn nur das resultierende **Recordset** -Objekt angegeben ist.

