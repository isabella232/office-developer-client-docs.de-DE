---
title: CancelUpdate-Methode (RDS)
TOCTitle: CancelUpdate method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 381d54f95e229ad38d1980746d4126a3cb654111
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606961"
---
# <a name="cancelupdate-method-rds"></a>CancelUpdate-Methode (RDS)

**Gilt für**: Access 2013, Office 2013

Verwirft alle an der aktuellen oder neuen Zeile eines [Recordset](recordset-object-ado.md)-Objekts vorgenommenen Änderungen.

## <a name="syntax"></a>Syntax

*DataControl*. CancelUpdate

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DataControl* |Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|

## <a name="remarks"></a>HinwBemerkungeneise

Der Cursordienst für OLE DB behält eine Kopie der ursprünglichen Werte bei und speichert die Änderungen zwischen. Wenn Sie **CancelUpdate** aufrufen, wird der Cache auf den leeren Zustand zurückgesetzt, und alle gebundenen Steuerelemente werden auf die ursprünglichen Daten aktualisiert.

