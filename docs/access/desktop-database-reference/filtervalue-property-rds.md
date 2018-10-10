---
title: FilterValue-Eigenschaft (RDS)
TOCTitle: FilterValue Property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39152be2c53dc0de9bc1bcb21fee505fcb9106dc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473820"
---
# <a name="filtervalue-property-rds"></a>FilterValue-Eigenschaft (RDS)


**Betrifft**: Access 2013 | Office 2013


Gibt den Wert an, mit dem Datensätze gefiltert werden sollen.

## <a name="syntax"></a>Syntax

*DataControl*. FilterValue = *Zeichenfolge*

## <a name="parameters"></a>Parameter

  - *DataControl*

  - Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.

  - *String*

  - Ein **String** -Wert, der stellt ein der Datenwert mit dem gefiltert (z. B. 'Programmierer' oder 125) aufgezeichnet.

## <a name="remarks"></a>Hinweise

Die Eigenschaften [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md) und [FilterColumn](filtercolumn-property-rds.md) ermöglichen die Sortier- und Filterfunktionalität für den clientseitigen Cache. Mit der Sortierfunktionalität werden Datensätze nach den Werten einer Spalte angeordnet. Mit der Filterfunktionalität werden Teilmengen von Datensätzen anhand von Suchkriterien angezeigt, während das vollständige [Recordset](recordset-object-ado.md)-Objekt im Cache bleibt. Die [Reset](reset-method-rds.md)-Methode führt die Kriterien aus und ersetzt das aktuelle **Recordset** -Objekt durch ein aktualisierbares **Recordset** -Objekt.

Nullwerte führen zu Konflikten der Datentypen.

