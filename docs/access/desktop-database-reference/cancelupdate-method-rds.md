---
title: CancelUpdate-Methode (RDS)
TOCTitle: CancelUpdate method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b0c02a9ca72add763e1d3ccf62d5ede8adaecc6b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718616"
---
# <a name="cancelupdate-method-rds"></a>CancelUpdate-Methode (RDS)

**Betrifft**: Access 2013, Office 2013

Verwirft alle an der aktuellen oder neuen Zeile eines [Recordset](recordset-object-ado.md)-Objekts vorgenommenen Änderungen.

## <a name="syntax"></a>Syntax

*DataControl*. CancelUpdate

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DataControl* |Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|

## <a name="remarks"></a>Hinweise

Der Cursordienst für OLE DB behält eine Kopie der ursprünglichen Werte bei und speichert die Änderungen zwischen. Wenn Sie **CancelUpdate** aufrufen, wird der Cache auf den leeren Zustand zurückgesetzt, und alle gebundenen Steuerelemente werden auf die ursprünglichen Daten aktualisiert.

