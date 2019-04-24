---
title: FilterCriterion-Eigenschaft (RDS)
TOCTitle: FilterCriterion property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 65541e8f64c5a019679252246edbe8027130c4ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292426"
---
# <a name="filtercriterion-property-rds"></a>FilterCriterion-Eigenschaft (RDS)

**Gilt für**: Access 2013, Office 2013

Gibt den im Filterwert zu verwendenden Auswertungsoperator an.

## <a name="syntax"></a>Syntax

*DataControl*. FilterCriterion = *Zeichenfolge*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DataControl* |Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|
|*String* |Ein **String** -Wert, der den Auswertungsoperator für [FilterValue](filtervalue-property-rds.md) zu den Datensätzen angibt. Kann \<eine der folgenden sein:, \<=, \>, \>=, =, oder. \< \>|

## <a name="remarks"></a>Bemerkungen

Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion** und [FilterColumn](filtercolumn-property-rds.md) ermöglichen die Sortier- und Filterfunktionalität für den clientbasierten Cache. Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet. Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt. Die [Reset](reset-method-rds.md)-Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset**-Objekt durch ein aktualisierbares **Recordset**-Objekt.

Der Operator\!"=" ist für **FilterCriterion**ungültig; Verwenden Sie stattdessen "\<\>".

Wenn Sie die Filter- und Sortiereigenschaften festgelegt haben und die **Reset** -Methode aufrufen, wird das Rowset zuerst gefiltert und dann sortiert. Bei aufsteigender Sortierung befinden sich die NULL-Werte oben, bei absteigender Sortierung befinden sich die NULL-Werte unten (aufsteigend ist das Standardverhalten).

