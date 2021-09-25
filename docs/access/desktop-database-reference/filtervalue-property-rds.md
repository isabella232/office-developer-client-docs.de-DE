---
title: FilterValue-Eigenschaft (RDS)
TOCTitle: FilterValue property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d9d63d4097d847af8fc5925e6f7b795d8a85921f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602549"
---
# <a name="filtervalue-property-rds"></a>FilterValue-Eigenschaft (RDS)

**Gilt für**: Access 2013, Office 2013

Gibt den Wert an, mit dem Datensätze gefiltert werden sollen.

## <a name="syntax"></a>Syntax

*DataControl*. FilterValue = *String*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DataControl* |Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|
|*String* |Ein **String -Wert,** der einen Datenwert darstellt, mit dem Datensätze gefiltert werden sollen (z. B. "Programmer" oder 125).|

## <a name="remarks"></a>HinwBemerkungeneise

Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md) und [FilterColumn](filtercolumn-property-rds.md) ermöglichen die Sortier- und Filterfunktionalität für den clientbasierten Cache. 

Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet. Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt. Die [Reset](reset-method-rds.md)-Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset**-Objekt durch ein aktualisierbares **Recordset**-Objekt.

Nullwerte führen zu Konflikten der Datentypen.

