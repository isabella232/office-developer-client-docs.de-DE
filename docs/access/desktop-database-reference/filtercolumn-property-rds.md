---
title: FilterColumn-Eigenschaft (RDS)
TOCTitle: FilterColumn property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d29c591c88de4b53535c26430bf369cbd3f53284
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292440"
---
# <a name="filtercolumn-property-rds"></a>FilterColumn-Eigenschaft (RDS)

**Gilt für**: Access 2013, Office 2013

Zeigt die Spalte an, für die die Filterkriterien ausgewertet werden.

## <a name="syntax"></a>Syntax

*DataControl*. FilterColumn = *Zeichenfolge*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DataControl* |Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|
|*String* |Ein **String** -Wert, der die Spalte angibt, für die die Filterkriterien ausgewertet werden. Die Filterkriterien werden in der [FilterCriterion](filtercriterion-property-rds.md)-Eigenschaft angegeben.|

## <a name="remarks"></a>Bemerkungen

Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) und **FilterColumn** ermöglichen die Sortier- und Filterfunktionalität für den clientbasierten Cache. 

Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet. Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt. 

Die [Reset](reset-method-rds.md)-Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset**-Objekt durch ein aktualisierbares **Recordset**-Objekt.

