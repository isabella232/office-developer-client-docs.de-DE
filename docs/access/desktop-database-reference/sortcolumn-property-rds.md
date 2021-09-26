---
title: SortColumn-Eigenschaft (RDS)
TOCTitle: SortColumn property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f03189808c65f7f43da89b8194647cd8d571aa2a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611483"
---
# <a name="sortcolumn-property-rds"></a>SortColumn-Eigenschaft (RDS)

**Gilt für**: Access 2013, Office 2013

Gibt die Spalte an, nach der die Datensätze sortiert werden sollen.

## <a name="syntax"></a>Syntax

*DataControl*. SortColumn = *String*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DataControl* |Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|
|*String* |Ein **String** -Wert, der den Namen oder Alias der Spalte angibt, nach der die Datensätze sortiert werden sollen.|

## <a name="remarks"></a>HinwBemerkungeneise

Die Eigenschaften **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) und [FilterColumn](filtercolumn-property-rds.md) ermöglichen die Sortier- und Filterfunktionalität für den clientbasierten Cache. Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet. Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt. Die [Reset](reset-method-rds.md)-Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset**-Objekt durch ein aktualisierbares **Recordset**-Objekt.

To sort on a **Recordset**, you must first save any pending changes. If you are using the **RDS.DataControl**, you can use the [SubmitChanges](submitchanges-method-rds.md) method. Beispiel: **RDS. DataControl** heißt ADC1, Ihr Code wäre ADC1. Submitchanges. Bei einem ADO- **Recordset** -Objekt können Sie dessen [UpdateBatch](updatebatch-method-ado.md)-Methode verwenden. Die **UpdateBatch** -Methode wird für **Recordset** -Objekte empfohlen, die mit der [CreateRecordset](createrecordset-method-rds.md)-Methode erstellt wurden. Der Code kann z. B. "myRS.UpdateBatch" oder ". Bei einem ADO- **Recordset** -Objekt können Sie dessen [UpdateBatch](updatebatch-method-ado.md)-Methode verwenden. Die **UpdateBatch** -Methode wird für **Recordset** -Objekte empfohlen, die mit der [CreateRecordset](createrecordset-method-rds.md)-Methode erstellt wurden. Der Code kann z. B. "myRS.UpdateBatch" oder "ADC1" sein. Recordset.UpdateBatch .

