---
title: Index.Clustered-Eigenschaft (DAO)
TOCTitle: Clustered Property
ms:assetid: dd0876a9-b7fe-c8c8-e675-5ed758ce5bd3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835375(v=office.15)
ms:contentKeyID: 48548149
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052930
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 95b12df62fe47779c1867a291018726ada299390
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998931"
---
# <a name="indexclustered-property-dao"></a>Index.Clustered-Eigenschaft (DAO)

**Betrifft**: Access 2013, Office 2013

Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ab ein **Index**-Objekt einen gruppierten Index für eine Tabelle darstellt (gilt nur für Microsoft Access-Arbeitsbereiche). **Boolean**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . Gruppiert

*Ausdruck* Ein Ausdruck, der ein **Index** -Objekt zurückgibt.

## <a name="remarks"></a>Bemerkungen

Der festgelegte oder zurückgegebene Wert ist ein Boolean-Wert, der auf True festgelegt ist,  wenn das Index-Objekt einen gruppierten Index darstellt.

Einige IISAM-Desktop-Datenbankenformate verwenden gruppierte Indizes. Ein gruppierter Index besteht aus einem oder mehreren Nichtschlüsselfeldern, die (in Kombination) alle Datensätze einer Tabelle in einer vordefinierten Reihenfolge anordnen. Ein gruppierter Index ermöglicht einen effizienten Zugriff auf Datensätze in einer Tabelle, in der Indexwerte möglicherweise nicht eindeutig sind.

Bei einem neuen, noch keiner Auflistung angefügten **Index**-Objekt ist die **Clustered**-Eigenschaft nicht schreibgeschützt. Bei einem vorhandenen **Index**-Objekt in einer **Indexes**-Auflistung ist sie schreibgeschützt.

> [!NOTE]
> - Microsoft Access-Datenbanken ignorieren die **Clustered**-Eigenschaft, da das Microsoft Access-Datenbankmodul keine gruppierten Indizes unterstützt.
> - Bei ODBC-Datenquellen gibt die **Clustered** -Eigenschaft immer **False**zurück. Da nicht erkannt wird, ob die ODBC-Datenquelle einen gruppierten Index besitzt oder nicht.


