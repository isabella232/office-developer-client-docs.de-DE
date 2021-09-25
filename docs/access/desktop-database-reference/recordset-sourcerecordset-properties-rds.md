---
title: Recordset-, SourceRecordset-Eigenschaft (RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7bd0518334f17b29a835412f95e8911887dd4e73
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585382"
---
# <a name="recordset-sourcerecordset-properties-rds"></a>Recordset-, SourceRecordset-Eigenschaft (RDS)

**Gilt für**: Access 2013, Office 2013

Gibt das **Recordset**-Objekt an, das von einem benutzerdefinierten Geschäftsobjekt zurückgegeben wird.

## <a name="syntax"></a>Syntax

*DataControl*. SourceRecordset = *Recordset*

*Recordset*  =  *DataControl*. Recordset

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DataControl* |Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|
|*Recordset* |Eine Objektvariable, die ein **Recordset**-Objekt darstellt.|

## <a name="remarks"></a>HinwBemerkungeneise

Sie können die **SourceRecordset** -Eigenschaft auf ein [Recordset](recordset-object-ado.md) festlegen, das von einem benutzerdefinierten Geschäftsobjekt zurückgegeben wird.

Diese Eigenschaften ermöglichen es einer Anwendung, den Bindungsprozess anhand eines benutzerdefinierten Prozesses zu verarbeiten. Die Eigenschafen empfangen ein Rowset, das in ein **Recordset** -Objekt eingebunden ist, sodass Sie das **Recordset** -Objekt direkt verarbeiten können, z. B. mit Aktionen wie dem Festlegen von Eigenschaften oder Iteration durch das **Recordset** -Objekt.

Sie können zur Laufzeit im Skriptcode die **SourceRecordset** -Eigenschaft festlegen oder die **Recordset** -Eigenschaft lesen.

**SourceRecordset** ist eine lesegeschützte Eigenschaft im Gegensatz zur **Recordset** -Eigenschaft, die schreibgeschützt ist.

