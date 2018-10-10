---
title: MoveFirst-, MoveLast-, MoveNext- und MovePrevious-Methoden (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4671e57e3edb44bc1c927ca11f2cf79e70c2699
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474533"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a>MoveFirst-, MoveLast-, MoveNext- und MovePrevious-Methoden (RDS)


**Betrifft**: Access 2013 | Office 2013

Wechselt zum ersten, letzten, nächsten oder vorherigen Datensatz in einem angegebenen [Recordset](recordset-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*DataControl*. Recordset-Objekt. { MoveFirst | MoveLast | MoveNext | MovePrevious}

## <a name="parameters"></a>Parameter

  - *DataControl*

  - Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.

## <a name="remarks"></a>Hinweise

Sie können die Move-Methoden für das RDS.DataControl-Objekt verwenden, um zwischen den Datensätzen in den datengebundenen Steuerelementen auf einer Webseite zu navigieren. Angenommen, Sie zeigen ein Recordset-Objekt durch Bindung an ein RDS.DataControl-Objekt in einem Raster an. Sie können anschließend die Schaltflächen Erster, Letzter, Nächster und Vorheriger einfügen, auf die die Benutzer klicken können, um zum ersten, letzten, nächsten oder vorherigen im Recordset-Objekt angezeigten Datensatz zu wechseln. Rufen Sie dazu in den onClick-Prozeduren die Methoden MoveFirst, MoveLast, MoveNext und MovePrevious des RDS.DataControl-Objekts für die Schaltflächen Erster, Letzter, Nächster bzw. Vorheriger auf. Die entsprechende Vorgehensweise wird im Beispiel zum Adressbuch erläutert.

