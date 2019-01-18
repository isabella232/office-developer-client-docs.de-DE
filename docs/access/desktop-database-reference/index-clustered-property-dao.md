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
localization_priority: Normal
ms.openlocfilehash: 060963dc47c933fee903cd9b220adb45c7f63df6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706702"
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


