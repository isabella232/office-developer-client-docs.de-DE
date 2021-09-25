---
title: ActiveCommand-Eigenschaft (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ab0bee62d55b11ce9a35e08cecf814cb4d75d5a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586320"
---
# <a name="activecommand-property-ado"></a>ActiveCommand-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Gibt das [Command](command-object-ado.md)-Objekt an, mit dem das zugeordnete [Recordset](recordset-object-ado.md)-Objekt erstellt wurde.

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert vom Datentyp **Variant** zurück, der ein **Command**-Objekt enthält. Der Standard ist ein nullwertiger Objektverweis.

## <a name="remarks"></a>HinwBemerkungeneise

Die **ActiveCommand**-Eigenschaft ist schreibgeschützt.

Wenn zum Erstellen des aktuellen **Recordset-Objekts** kein **Command-Objekt** verwendet wurde, wird ein **Null-Objektverweis** zurückgegeben.

Suchen Sie mit dieser Eigenschaft das zugeordnete **Command**-Objekt, wenn nur das resultierende **Recordset**-Objekt angegeben ist.

