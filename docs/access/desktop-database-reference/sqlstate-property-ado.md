---
title: SQLState-Eigenschaft (ADO)
TOCTitle: SQLState property (ADO)
ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15)
ms:contentKeyID: 48547806
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6fb45342a56a003856192a353270778b44654de
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872179"
---
# <a name="sqlstate-property-ado"></a>SQLState-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt den SQL-Status für ein bestimmtes [Error](error-object-ado.md)-Objekt an.

## <a name="return-value"></a>Rückgabewert

Gibt einen aus fünf Zeichen bestehenden **String** -Wert zurück, der dem ANSI SQL-Standard entspricht und einen Fehlercode angibt.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **SQLState** -Eigenschaft, um den aus fünf Zeichen bestehenden Fehlercode zu lesen, der vom Anbieter im Falle eines Fehlers bei der Verarbeitung einer SQL-Anweisung zurückgegeben wird. Wenn Sie z. B. den Microsoft OLE DB-Anbieter für ODBC mit einer Microsoft SQL Server-Datenbank verwenden, stammen SQL-Statusfehlercodes von ODBC. Die Codes basieren entweder auf Fehlern, die nur für ODBC gelten, oder auf Fehlern, die von Microsoft SQL Server stammen und dann ODBC-Fehlern zugeordnet wurden. Dieses Fehlercodes sind im ANSI SQL-Standard dokumentiert, sind jedoch in verschiedenen Datenquellen möglicherweise unterschiedlich implementiert.

