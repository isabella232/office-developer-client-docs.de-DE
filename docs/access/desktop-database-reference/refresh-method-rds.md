---
title: Refresh-Methode (RDS)
TOCTitle: Refresh Method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9d7d1ecb009f61933328695ccbfbea06ac9d7b0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473221"
---
# <a name="refresh-method-rds"></a>Refresh-Methode (RDS)


**Betrifft**: Access 2013 | Office 2013

Fragt die in der [Connect](connect-property-rds.md)-Eigenschaft angegebene Datenquelle erneut ab und aktualisiert die Abfrageergebnisse.

## <a name="syntax"></a>Syntax

*DataControl*. Aktualisieren

## <a name="parameters"></a>Parameter

  - *DataControl*

  - Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.

## <a name="remarks"></a>Hinweise

Bevor Sie die [Refresh](connect-property-rds.md) -Methode verwenden, müssen Sie die Eigenschaften [Connect](server-property-rds.md), [Server](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) und **SQL** festlegen. Alle datengebundenen Steuerelemente auf dem Formular, das einem **RDS.DataControl** -Objekt zugeordnet ist, geben die neue Datensatzgruppe wieder. Ein bereits vorhandenes [Recordset](recordset-object-ado.md)-Objekt wird freigegeben, und alle nicht gespeicherten Änderungen werden verworfen. Mithilfe der **Refresh** -Methode wird der erste Datensatz automatisch zum aktuellen Datensatz.

Es wird empfohlen, die **Refresh** -Methode regelmäßig aufzurufen, wenn Sie mit Daten arbeiten. Wenn Sie Daten abrufen und diese eine Weile auf dem Clientcomputer speichern, sind diese wahrscheinlich nach kurzer Zeit nicht mehr aktuell. Es kann vorkommen, dass von Ihnen vorgenommene Änderungen fehlschlagen, da der Datensatz möglicherweise von einer anderen Person geändert und vor Ihnen übermittelt wurde.

