---
title: SubmitChanges-Methode (RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ea7f3e27a75b4483cb8cf46e27d4492f831cff33
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714444"
---
# <a name="submitchanges-method-rds"></a>SubmitChanges-Methode (RDS)

**Betrifft**: Access 2013, Office 2013

Sendet ausstehende Änderungen des lokal zwischengespeicherten und aktualisierbaren [Recordset](recordset-object-ado.md)-Objekts an die in der [Connect](connect-property-rds.md)-Eigenschaft oder der [URL](url-property-rds.md)-Eigenschaft angegebene Datenquelle.

## <a name="syntax"></a>Syntax

*DataControl*. SubmitChanges

*DataFactory*. SubmitChanges*Connection*, *Recordset-Objekt*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DataControl* |Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|
|*DataFactory* |Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt darstellt.|
|*Connection* |Ein **String** -Wert, der die mit der **Connect** -Eigenschaft des **RDS.DataControl** -Objekts erstellte Verbindung darstellt.|
|*Recordset* |Eine Objektvariable, die ein **Recordset** -Objekt darstellt.|

## <a name="remarks"></a>Hinweise

Die Eigenschaften [Connect](connect-property-rds.md), [Server](server-property-rds.md) und [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) müssen festgelegt sein, bevor Sie die **SubmitChanges** -Methode für das **RDS.DataControl** -Objekt verwenden können.

Wenn Sie die [CancelUpdate](cancelupdate-method-rds.md)-Methode aufrufen, nachdem Sie die **SubmitChanges** -Methode für dasselbe **Recordset** -Objekt aufgerufen haben, schlägt der Aufruf von **CancelUpdate** fehl, da die Änderungen bereits übernommen wurden.

Es werden nur die geänderten Objekte zur Änderung gesendet. Die Änderungen werden entweder alle erfolgreich vorgenommen oder sie schlagen alle fehl.

Sie können nur mit dem *standardmäßigen* **RDSServer.DataFactory** -Objekt **SubmitChanges** verwenden. Diese Methode kann nicht für benutzerdefinierte Geschäftsobjekte verwendet werden.

Wenn die **URL** -Eigenschaft festgelegt wurde, sendet **SubmitChanges** Änderungen an den durch die URL angegebenen Speicherort.

