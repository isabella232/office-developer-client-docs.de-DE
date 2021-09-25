---
title: SubmitChanges-Methode (RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f1464bce8cbaed5e33c40d90a246c6302e5d85e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562188"
---
# <a name="submitchanges-method-rds"></a>SubmitChanges-Methode (RDS)

**Gilt für**: Access 2013, Office 2013

Sendet ausstehende Änderungen des lokal zwischengespeicherten und aktualisierbaren [Recordset](recordset-object-ado.md)-Objekts an die in der [Connect](connect-property-rds.md)-Eigenschaft oder der [URL](url-property-rds.md)-Eigenschaft angegebene Datenquelle.

## <a name="syntax"></a>Syntax

*DataControl*. Submitchanges

*DataFactory*. *SubmitChanges-Verbindung*, *Recordset*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DataControl* |Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|
|*DataFactory* |Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt darstellt.|
|*Connection* |Ein **String** -Wert, der die mit der **Connect** -Eigenschaft des **RDS.DataControl** -Objekts erstellte Verbindung darstellt.|
|*Recordset* |Eine Objektvariable, die ein **Recordset**-Objekt darstellt.|

## <a name="remarks"></a>HinwBemerkungeneise

Die Eigenschaften [Connect](connect-property-rds.md), [Server](server-property-rds.md) und [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) müssen festgelegt sein, bevor Sie die **SubmitChanges**-Methode für das **RDS.DataControl**-Objekt verwenden können.

Wenn Sie die [CancelUpdate](cancelupdate-method-rds.md)-Methode aufrufen, nachdem Sie die **SubmitChanges**-Methode für dasselbe **Recordset**-Objekt aufgerufen haben, schlägt der Aufruf von **CancelUpdate** fehl, da die Änderungen bereits übernommen wurden.

Es werden nur die geänderten Objekte zur Änderung gesendet. Die Änderungen werden entweder alle erfolgreich vorgenommen oder sie schlagen alle fehl.

Sie können **SubmitChanges** nur mit dem *standardmäßigen* **RDSServer.DataFactory-Objekt** verwenden. Diese Methode kann nicht für benutzerdefinierte Geschäftsobjekte verwendet werden.

Wenn die **URL** -Eigenschaft festgelegt wurde, sendet **SubmitChanges** Änderungen an den durch die URL angegebenen Speicherort.

