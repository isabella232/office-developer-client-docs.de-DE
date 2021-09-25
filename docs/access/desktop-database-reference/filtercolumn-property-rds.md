---
title: FilterColumn-Eigenschaft (RDS)
TOCTitle: FilterColumn property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 23fbdbc8c546d99456a5e898ea835d3b157e7728
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602626"
---
# <a name="filtercolumn-property-rds"></a>FilterColumn-Eigenschaft (RDS)

**Gilt für**: Access 2013, Office 2013

Zeigt die Spalte an, für die die Filterkriterien ausgewertet werden.

## <a name="syntax"></a>Syntax

*DataControl*. FilterColumn = *String*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DataControl* |Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|
|*String* |Ein **String** -Wert, der die Spalte angibt, für die die Filterkriterien ausgewertet werden. Die Filterkriterien werden in der [FilterCriterion](filtercriterion-property-rds.md)-Eigenschaft angegeben.|

## <a name="remarks"></a>HinwBemerkungeneise

Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) und **FilterColumn** ermöglichen die Sortier- und Filterfunktionalität für den clientbasierten Cache. 

Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet. Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt. 

Die [Reset](reset-method-rds.md)-Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset**-Objekt durch ein aktualisierbares **Recordset**-Objekt.

