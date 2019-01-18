---
title: SortColumn-Eigenschaft (RDS)
TOCTitle: SortColumn property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54e6df1f2a94bd59f1e4cf9f9c0be77d785a3048
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709264"
---
# <a name="sortcolumn-property-rds"></a>SortColumn-Eigenschaft (RDS)

**Betrifft**: Access 2013, Office 2013

Gibt die Spalte an, nach der die Datensätze sortiert werden sollen.

## <a name="syntax"></a>Syntax

*DataControl*. SortColumn = *Zeichenfolge*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DataControl* |Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|
|*String* |Ein **String** -Wert, der den Namen oder Alias der Spalte angibt, nach der die Datensätze sortiert werden sollen.|

## <a name="remarks"></a>Hinweise

Die Eigenschaften **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) und [FilterColumn](filtercolumn-property-rds.md) ermöglichen die Sortier- und Filterfunktionalität für den clientbasierten Cache. Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet. Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt. Die [Reset](reset-method-rds.md) -Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset** -Objekt durch ein aktualisierbares **Recordset** -Objekt.

Um ein **Recordset-Objekt**zu sortieren, müssen Sie zuerst alle ausstehenden Änderungen speichern. Bei Verwendung der **RDS. DataControl**, können Sie die [SubmitChanges](submitchanges-method-rds.md) -Methode verwenden. Beispielsweise, wenn Ihre **RDS. DataControl** ist mit dem Namen ADC1, würde der Code ADC1 werden. SubmitChanges. Bei einem ADO- **Recordset** -Objekt können Sie dessen [UpdateBatch](updatebatch-method-ado.md)-Methode verwenden. Die **UpdateBatch** -Methode wird für **Recordset** -Objekte empfohlen, die mit der [CreateRecordset](createrecordset-method-rds.md)-Methode erstellt wurden. Beispielsweise könnte der Code myRS.UpdateBatch oder. Bei einem ADO- **Recordset** -Objekt können Sie dessen [UpdateBatch](updatebatch-method-ado.md)-Methode verwenden. Die **UpdateBatch** -Methode wird für **Recordset** -Objekte empfohlen, die mit der [CreateRecordset](createrecordset-method-rds.md)-Methode erstellt wurden. Beispielsweise könnte der Code myRS.UpdateBatch oder ADC1. Recordset.UpdateBatch lauten.

