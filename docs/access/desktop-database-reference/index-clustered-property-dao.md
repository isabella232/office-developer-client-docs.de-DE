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
ms.localizationpriority: medium
ms.openlocfilehash: 5ef312233b77170f0f6b42c9aa8e133ff4851ab3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626407"
---
# <a name="indexclustered-property-dao"></a>Index.Clustered-Eigenschaft (DAO)

**Gilt für**: Access 2013, Office 2013

Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ab ein **Index**-Objekt einen gruppierten Index für eine Tabelle darstellt (gilt nur für Microsoft Access-Arbeitsbereiche). **Boolean**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . Gruppierten

*Ausdruck* Ein Ausdruck, der ein **Index-Objekt** zurückgibt.

## <a name="remarks"></a>Bemerkungen

The setting or return value is a Boolean data type that is **True** if the **Index** object represents a clustered index.

Einige IISAM-Desktop-Datenbankenformate verwenden gruppierte Indizes. Ein gruppierter Index besteht aus einem oder mehreren Nichtschlüsselfeldern, die (in Kombination) alle Datensätze einer Tabelle in einer vordefinierten Reihenfolge anordnen. Ein gruppierter Index ermöglicht einen effizienten Zugriff auf Datensätze in einer Tabelle, in der Indexwerte möglicherweise nicht eindeutig sind.

Bei einem neuen, noch keiner Auflistung angefügten **Index**-Objekt ist die **Clustered**-Eigenschaft nicht schreibgeschützt. Bei einem vorhandenen **Index**-Objekt in einer **Indexes**-Auflistung ist sie schreibgeschützt.

> [!NOTE]
> - Microsoft Access-Datenbanken ignorieren die **Clustered**-Eigenschaft, da das Microsoft Access-Datenbankmodul keine gruppierten Indizes unterstützt.
> - Für ODBC-Datenquellen gibt die **Clustered-Eigenschaft** immer **False zurück;** Es wird nicht erkannt, ob die ODBC-Datenquelle über einen gruppierten Index verfügt.


